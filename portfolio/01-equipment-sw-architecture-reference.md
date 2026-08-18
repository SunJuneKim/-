# 장비 SW 아키텍처 참고 — MVVM · State Machine · Device Abstraction

> 출처: ChatGPT 피드백 (경력 소개 후 아키텍처 방향 논의)  
> 용도: 개인 프로젝트 설계·면접·포트폴리오 기획 참고

---

## 1. 핵심 원칙 (한 페이지 요약)

| 원칙 | 설명 |
|------|------|
| State Machine ≠ ViewModel 안에 넣기 | `enum + switch` 괴물 ViewModel 금지 |
| MVVM 역할 | State Machine **표현·조작** (Binding, Command) |
| Application 역할 | Recipe, Sequence, **EquipmentStateMachine**, Controller |
| Interface 역할 | Application이 필요한 **capability 계약** (IHeater, IMotor…) |
| Driver 역할 | Protocol, Register, CRC, Timeout — Application이 **모름** |
| Simulator | Real Driver와 **동일 contract** → HW-independent V&V |

---

## 2. 추천 레이어 구조

```
┌──────────────────────────────┐
│             View             │  WPF MainWindow
└──────────────┬───────────────┘
               │ Binding / Command
               ▼
┌──────────────────────────────┐
│          ViewModel           │  CurrentState, IsRunning, Commands
└──────────────┬───────────────┘
               │ uses (소유 X, 위임)
               ▼
┌──────────────────────────────┐
│     Equipment Controller     │
│  EquipmentStateMachine       │  Idle → Init → Ready → Running → Error…
│  Recipe / Sequence Engine    │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│     Device Abstraction       │  IDevice, IHeater, IMotor, IPressureSensor
└──────────────┬───────────────┘
               │
        ┌──────┴──────┐
        ▼             ▼
   Real Driver    Simulator / Mock
        │
        ▼
    Hardware
```

### 나쁜 예 (피하기)

```
View → MainViewModel
         ├── CurrentState
         ├── Start() / Stop() / ExecuteStep1…3()
         └── switch(CurrentState)   ← 여기서 모든 장비 로직
```

### 좋은 예

```csharp
public class MainViewModel : ObservableObject
{
    private readonly IEquipmentController _controller;

    public EquipmentState CurrentState => _controller.CurrentState;

    public ICommand StartCommand { get; }

    public MainViewModel(IEquipmentController controller)
    {
        _controller = controller;
        StartCommand = new RelayCommand(() => _controller.Start());
    }
}
```

View는 `CurrentState == Ready` → "READY" 표시만.

---

## 3. State Machine이 관리하는 4가지

단순 `enum`이 아니라 **State · Event · Transition · Action** 분리.

### State (예)

```csharp
public enum EquipmentState
{
    Offline,
    Initializing,
    Ready,
    Running,
    Stopping,
    Error,
    Recovering
}
```

### Event (예)

```
StartRequested, InitializationCompleted, RecipeStarted, RecipeCompleted,
StopRequested, DeviceFault, CommunicationTimeout, RecoveryCompleted
```

### Transition (예)

```
READY + StartRequested      → RUNNING
RUNNING + DeviceFault       → ERROR
ERROR + RecoveryCompleted   → READY
```

### Action (State 진입/이탈 시)

```
RUNNING 진입 → Recipe 실행, Heater setpoint, Motor start, Pressure check
ERROR 진입   → Motor stop, Heater safe state, Valve close, Alarm
```

---

## 4. Device Abstraction — 경계가 생기는 지점

### Interface만 있다고 경계가 아님

```csharp
// 약함 — "인터페이스 썼다" 수준
public interface IHeater { void SetTemperature(double t); }
```

### Application이 알아야 할 것 vs 몰라야 할 것

| Application (알아야 함) | Driver (숨겨야 함) |
|--------------------------|-------------------|
| `SetTemperatureAsync(350)` | Serial packet, Register 0x0214 |
| `GetTemperatureAsync()` | CRC, Retry, Timeout |
| `GetStatus()` | Modbus function code |

**나쁜 예 (Application이 HW를 앎):**

```csharp
serialPort.Write("02 04 FF 01");  // RecipeController 안에서 직접
```

**좋은 예:**

```csharp
await _heater.SetTemperatureAsync(350);  // Application
// RealHeaterDriver 내부: protocol, register, CRC, timeout
```

### 환경별 구현 교체 (DI)

```
IHeater ─┬─ RealHeaterDriver  → Hardware (Production)
         ├─ SimulatedHeater     → Fault injection (V&V)
         └─ MockHeater          → Unit test
```

Application 코드는 **동일**.

---

## 5. Interface 설계 — 한 단계 더

```csharp
public interface IDevice
{
    string Id { get; }
    DeviceState State { get; }
    Task InitializeAsync();
    Task StartAsync();
    Task StopAsync();
    Task ResetAsync();
}

public interface IHeater : IDevice
{
    double Temperature { get; }
    double SetPoint { get; }
    Task SetTemperatureAsync(double temperature);
}

public interface IPressureSensor : IDevice
{
    double Pressure { get; }
    Task<double> GetPressureAsync();
}
```

**주의:** `IHeater` = Driver의 low-level API (`WriteRegister`)를 그대로 노출하면 **추상화 실패**.

---

## 6. Recipe + State Machine + Device 합체

예시 Recipe:

```
Step 1: Heater 350°C, Pressure 2 Torr, Wait stable
Step 2: Motor 1000 RPM, Gas 100 sccm
Step 3: Process 120 sec
```

Application:

```csharp
await _heater.SetTemperatureAsync(350);
var p = await _pressureSensor.GetPressureAsync();
await _motor.SetRpmAsync(1000);
```

장애 시 (RUNNING 중 Pressure timeout):

```
RUNNING → (SensorTimeout) → FAULT
  → Stop Motor, Heater safe, Close valve, Alarm
FAULT → (Reset) → RECOVERING → READY
```

---

## 7. V&V 관점 (본인 경력과 연결)

Simulator에서 주입 가능:

- Temperature overshoot / timeout
- Communication failure
- Sensor stuck
- Random noise

```
V&V Test → Equipment Application → IHeater → SimulatedHeater
                                              ├── Normal
                                              ├── Timeout
                                              └── OverTemp
```

"Mock 썼습니다"보다 **Hardware-independent V&V + fault injection**이 설득력 있음.

---

## 8. 면접 답변 템플릿

**Q. 왜 IHeater를 Application 쪽에 두었나요?**

> Application은 히터의 물리 구현이나 통신 프로토콜을 알 필요가 없고, 온도 설정·상태 조회 capability만 필요합니다. 실제 장비는 TCP/Serial driver가 구현하고, 동일 contract를 Simulator가 구현해 Application과 Hardware dependency를 분리했습니다. Hardware-independent V&V와 fault injection이 가능합니다.

**Q. State Machine을 MVVM에서 어떻게 쓰나요?**

> State Machine은 ViewModel이 아니라 Equipment Controller(Application layer)에 둡니다. ViewModel은 CurrentState 표시와 Start/Stop Command만 위임합니다. WPF/MVVM은 표현·조작, State Machine은 장비 상태 전이 결정입니다.

---

## 9. 참고 — 안 쓸 것 / 조심할 것

| 피하기 | 이유 |
|--------|------|
| ViewModel에 모든 시퀀스 로직 | 장비 복잡도↑ 시 유지보수 불가 |
| IHeater = Register API | Application이 HW에 결합 |
| "인터페이스 패턴 사용"만 언급 | **경계와 책임**까지 설명해야 함 |
| BSW/AUTOSAR 용어 (장비 SW 면접) | 도메인 불일치 — Equipment Platform 용어 사용 |
