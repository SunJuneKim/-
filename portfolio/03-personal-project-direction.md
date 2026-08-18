# 개인 프로젝트 방향 초안 (미정)

> 프로젝트명·규모는 아직 없음. ChatGPT 피드백 기반 **최소 데모** 방향만 정리.

---

## 1. 프로젝트 목표 (한 줄)

**WPF MVVM + Equipment State Machine + IDevice abstraction + Simulator** 를 한 repo에서 보여주는 **미니 장비 Operating SW**.

면접관이 보게 할 것:
- Hardware / Driver / Application **경계**
- Real vs Simulator **교체** (DI)
- State 전이 + **fault injection** V&V

---

## 2. 최소 기능 (MVP)

| # | 기능 | 보여줄 것 |
|---|------|-----------|
| 1 | WPF MainWindow | MVVM, 상태 표시, Start/Stop/Reset |
| 2 | `EquipmentStateMachine` | Idle → Init → Ready → Running → Error → Recovering |
| 3 | `IHeater`, `IMotor`, `IPressureSensor` | Application contract |
| 4 | `RealHeaterDriver` (가짜 TCP/Serial) | Protocol in driver |
| 5 | `SimulatedHeater` | Delay, overshoot, timeout fault |
| 6 | 간단 Recipe 3 step | SetTemp → Wait stable → Run motor |
| 7 | README 아키텍처 다이어그램 | 레이어 그림 1장 |

**하지 않아도 되는 것 (1차):** SECS/GEM, 실제 HW, MFC, 3D UI

---

## 3. 기술 스택 (예상)

| 계층 | 스택 |
|------|------|
| UI | WPF, MVVM (CommunityToolkit.Mvvm 또는 자체 RelayCommand) |
| Application | C# .NET 8, EquipmentController, StateMachine |
| Device | Interface + Real(Mock) + Simulator |
| Test | xUnit or NUnit — Application + SimulatedHeater |
| DI | Microsoft.Extensions.DependencyInjection |

---

## 4. NSLR 경험 연결 (README용 서사)

| 데모 기능 | 실무 연결 (한 줄) |
|-----------|-------------------|
| 3모드 → EquipmentState | NSLR 관측·지상보정·별보정 |
| Recipe step | NSLR 관측 시퀀스 |
| SimulatedHeater fault | IRST HIL Test Tool |
| Driver behind interface | IRST tdrv 호환 레이어 |
| UTC/KST 표시 (선택) | NSLR 시간계 변환 |

---

## 5. repo 구조 (안)

```
equipment-os-demo/
├── README.md                 # 아키텍처 다이어그램 + 경력 연결
├── docs/
│   └── architecture.md
├── src/
│   ├── Equipment.App/        # WPF
│   ├── Equipment.Core/       # StateMachine, Controller, Recipe
│   ├── Equipment.Devices/    # IHeater, IMotor, Drivers, Simulators
│   └── Equipment.Tests/
└── recipes/
    └── sample-recipe.json
```

---

## 6. 진행 순서 (나중에 시작할 때)

1. `Equipment.Core` — State + Event + `IEquipmentController` (UI 없이)
2. `Equipment.Devices` — `SimulatedHeater` + unit test
3. `Equipment.App` — WPF ViewModel 연결
4. `RealHeaterDriver` — loopback TCP mock
5. README + architecture diagram
6. (선택) Recipe JSON 로드

---

## 7. 체크리스트 (시작 전)

- [ ] 프로젝트명 확정
- [ ] GitHub repo 생성 (Private → 면접용 Public 일부)
- [ ] `01-equipment-sw-architecture-reference.md` 다시 읽기
- [ ] NSLR 3모드 → EquipmentState 매핑표 작성
- [ ] 면접 2분 아키텍처 설명 연습

---

## 8. 관련 문서

- [`01-equipment-sw-architecture-reference.md`](01-equipment-sw-architecture-reference.md)
- [`02-career-to-architecture-mapping.md`](02-career-to-architecture-mapping.md)
- NSLR 프로젝트: [`projects/01-space-object-tracking.md`](../projects/01-space-object-tracking.md)
- IRST: [`projects/02-xmc-hdlc-comms-card.md`](../projects/02-xmc-hdlc-comms-card.md)
