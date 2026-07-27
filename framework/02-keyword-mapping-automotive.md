# 자동차 전장 키워드 매핑

> 방산/항공 경력 → **자동차 SW JD 언어**로 변환

---

## JD 빈출 키워드 (계양전기·Tier1 공통)

### SW 설계
`Embedded SW` · `AUTOSAR` · `BSW` · `CDD` · `RTE` · `MBD` · `Simulink` · `MCU` · `CAN` · `LIN` · `Motor control` · `ECU` · `ASPICE` · `ISO 26262` · `FuSa`

### 시스템 설계
`Requirements analysis` · `System design` · `FMEA` · `FTA` · `Safety concept` · `Change management` · `Issue tracking` · `V-Model` · `Traceability`

### SW 검증
`Unit test` · `Integration test` · `Dynamic verification` · `HIL` · `SIL` · `Test automation` · `Coverage` · `MC/DC` · `Regression`

---

## 본인 경력 ↔ 자동차 매핑표

| 본인 경험 | 자동차 이력서 표현 |
|-----------|-------------------|
| NSLR 7구성품 통합 | **Multi-subsystem real-time integration** (ECU/모듈 다수 연동) |
| NTP/GPS ns 동기화 | **Deterministic event timing** / time-triggered coordination |
| 이벤트 타이머 | **Event-driven control scheduling** (관측 시퀀스) |
| 별보정·50 arcsec | **Closed-loop calibration** / precision feedback control |
| 마운트 20ms 제어 | **Real-time actuator control loop** (20ms cycle) |
| 호환 레이어 (tdrv) | **Legacy SW abstraction** — API-compatible migration (CDD/BSW 유사 사고) |
| Linux driver modify | **Low-level embedded SW** / communication driver |
| RS422/HDLC 8ch | **Multi-channel serial protocol** stack |
| Yocto | **Embedded Linux** platform bring-up |
| 현장 연동·디버깅 | **ECU integration test** / field validation |
| 스케줄러 사수 | **Cross-module interface definition** / integration lead |
| OpenCV AGC/ROI | Signal preprocessing (자동차에서는 **후순위**) |
| C# 운영제어 | Application layer SW (자동차: **ASW** 또는 HMI/도구) |

---

## 쓰지 말 것 / 조심할 것

| 표현 | 이유 |
|------|------|
| "AUTOSAR 3년" | 사실 아님 → "AUTOSAR 아키텍처 학습·전환 준비" |
| "MBD 전문" | Simulink 경험 없으면 금지 |
| "우주물체", "SLR" | JD와 무관 — **정밀 실시간 시스템**으로 일반화 |
| "PostgreSQL", "Cesium" | 전장 SW JD와 거리 있음 |

---

## 이력서 Skills 섹션 (자동차용 정렬)

**우선 노출**
```
C, Embedded C, Linux, Device Driver, Real-time Systems
Multi-protocol Communication (RS422, HDLC, UDP, TCP/IP)
System Integration, Field Validation, Yocto
```

**보조 (있으면)**
```
Python (test automation), C# (application/tooling)
OpenCV (signal preprocessing)
```

**학습 중 (자소서·면접용, 이력서 맨 아래 소글자)**
```
AUTOSAR Classic (BSW/RTE 개념), CAN/LIN, ISO 26262 overview
```

---

## 자동차 도메인 빠른 암기 (면접용)

| 용어 | 한 줄 |
|------|-------|
| **AUTOSAR** | 차량 SW 표준 아키텍처 (BSW + RTE + ASW) |
| **BSW** | OS, COM, Diag 등 기본 SW (Mobilion/Vector/EB 등 플랫폼) |
| **CDD** | Complex Device Driver — BSW와 HW 사이 커스텀 드라이버 |
| **RTE** | SW 컴포넌트 간 통신 런타임 |
| **MBD** | Simulink 등 모델 기반 제어 SW 개발 |
| **ASPICE** | 자동차 SW 프로세스 품질 (V-Model) |
| **ISO 26262** | 기능안전 (FuSa) |
| **HIL** | Hardware-in-the-Loop 실차 대신 장비로 검증 |

---

## 계양전기 사업 맥락

- **제품:** 파워시트 모터, EPB 모터, 스티어링 컬럼 모터 등 **전장 모터**
- **SW 직무:** 모터 ECU용 임베디드 SW, AUTOSAR BSW 플랫폼(Mobilion), MBD 제어
- **본인 연결점:** 실시간 제어·다채널 통신·드라이버·통합 — **모터 ECU 개발의 인접 경험**
