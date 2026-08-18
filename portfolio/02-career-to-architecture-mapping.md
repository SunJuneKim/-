# 본인 경력 ↔ 장비 SW 아키텍처 매핑

> 포트폴리오·면접에서 "이미 비슷한 걸 했다"고 말할 때 쓰는 대응표.

---

## 1. 전체 대응

| 아키텍처 개념 | 본인 실무 | 어필 한 줄 |
|---------------|-----------|------------|
| **Equipment Controller** | NSLR 운영제어 시스템 로직 오너 | 7구성품 시퀀스·모드 제어 |
| **State Machine** | 관측 / 지상보정 / 별보정 3모드 + 이벤트 타이머 | 모드별 전이·파라미터·시퀀스 |
| **Recipe / Sequence** | 관측 시퀀스, 20ms 루프, 스케줄러 연동 | 동기·비동기 조합 시퀀스 |
| **Device Abstraction** | 7구성품 TCP/UDP 인터페이스 (논리적 계약) | 구성품별 API·타이밍 분리 |
| **Driver ↔ App 경계** | IRST 호환 레이어 (tdrv → FPGA) | Application 무수정, Driver에서 흡수 |
| **Simulator / HIL** | C#/Python Test Tool, PC Mock-up | Real 없이 반복 검증·70h 시험 |
| **MVVM / GUI** | C# WPF/WinForms 운영제어, Cesium | 상태 표시·명령·모니터링 |
| **V&V / Fault** | ESF-CCS IEEE 검증, Simulated fault (IRST 예외) | 요구사항·증적·예외 시나리오 |

---

## 2. NSLR → Equipment Platform

### 이미 했던 것 (다른 이름)

| NSLR 실무 | 아키텍처 용어 |
|-----------|---------------|
| 관측·지상보정·별보정 모드 | **Equipment mode** (Calibration / Production 유사) |
| 모드별 구성품·시퀀스 다름 | **Mode-specific state / recipe** |
| 버튼 → 동기·비동기 시퀀스 | **Sequence engine** (sync point + parallel branch) |
| 7구성품 간섭 방지 | **Interlock** |
| NTP/GPS + 이벤트 타이머 | **Sync trigger** (절대시간) |
| RA/Dec → Az/El | **Coordinate transform** (setpoint 계산) |
| PostgreSQL 관측·보정 데이터 | **Recipe / log / traceability** |
| 거창 옆 신설·운영 SW 국산화 | **Greenfield platform** (legacy 옆 신규 OS) |

### 아직 명시적으로 안 했던 것 (개인 프로젝트에서 보완)

| 갭 | 개인 프로젝트에서 할 일 |
|----|------------------------|
| `IHeater` 같은 **명시적 interface** | 소형 장비 시뮬레이터에 도입 |
| ViewModel과 State Machine **코드 분리** | 리팩토링 전/후 비교 |
| **SimulatedHeater** fault injection | V&V 시나리오 데모 |
| Recipe **데이터 파일화** (XML/JSON) | 코드 밖 recipe 정의 |

---

## 3. IRST → Driver / Application 경계

| IRST 실무 | 아키텍처 용어 |
|-----------|---------------|
| Application 수정 0% | **Application layer frozen** |
| 호환 레이어 + Driver 수정 | **Adapter / Driver** behind stable contract |
| RS422/HDLC 예외를 Driver에서 처리 | **Protocol detail hidden from Application** |
| C#/Python Test Tool | **Simulator + HIL** |
| 70h 연속 시험 | **Soak test / stress validation** |

면접 연결:
> "IRST는 IHeater가 아니라 통신카드 contract였지만, **Application이 HW protocol을 모르게 경계를 그은 것**은 같습니다."

---

## 4. 에너시스 · ESF-CCS

| 경력 | 아키텍처 연결 |
|------|---------------|
| STM32 Calibration | **IDevice setpoint / feedback** |
| ATE 자동화 | **Automated V&V pipeline** |
| ESF-CCS V&V | **Requirements → test → evidence** |
| Qt 테스트 GUI | **Operator UI + device under test** |

---

## 5. 면접 30초 (아키텍처 관점)

> "NSLR에서는 ViewModel만이 아니라 **운영 모드·시퀀스·7구성품 간섭**을 Application 층에서 설계했습니다. IRST에서는 **Application을 건드리지 않고 Driver 쪽에서 contract를 맞췄고**, Test Tool로 HIL 검증했습니다. 개인 프로젝트로는 **State Machine을 ViewModel 밖으로 빼고 IHeater/IMotor abstraction + Simulator**까지 명시적으로 보여주려 합니다."

---

## 6. 포트폴리오에 넣을 Before / After 스토리

| Before (실무 당시) | After (개인 프로젝트 목표) |
|--------------------|---------------------------|
| WinForms에 로직 일부 혼재 | MVVM + Controller 분리 |
| 구성품별 클래스·통신 산재 | `IDevice` 계약 + DI |
| 현장에서만 통합 시험 | SimulatedHeater fault 시나리오 |
| 모드·시퀀스가 코드에 분산 | State Machine + Recipe 파일 |
