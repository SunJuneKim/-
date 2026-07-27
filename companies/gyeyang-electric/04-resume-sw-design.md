# 계양전기 — SW 설계 엔지니어 이력서 (제출용 초안)

> **지원 직무:** 전장 SW 설계 엔지니어 (임베디드 SW · MBD · BSW / Mobilion AUTOSAR)  
> PDF 변환 전 최종 확인. 민감정보·방산 세부 삭제.

---

## [이름]

**Embedded / Real-time Systems Engineer**  
7년+ | Low-level SW · Multi-subsystem Integration · Field Validation

---

## Summary

**실시간 임베디드·시스템 통합 엔지니어 (7년)**

Linux 디바이스 드라이버·통신 스택에서 **다수 서브시스템 실시간 통합·응용 SW**까지 end-to-end 개발 경험을 보유했습니다. 정밀 실시간 시스템에서 **7개 모듈·다채널 센서/액추에이터 연동**, **ns급 시간 동기화**, **20ms급 제어 루프**, **레거시 SW 호환 추상화 레이어**를 설계·구현·현장 검증했습니다. 상용 드라이버를 자체 HW로 대체하는 **저수준 SW 수정** 및 **8채널 시리얼 통신(RS422/HDLC)** 스택을 담당하고 있으며, **Embedded Linux(Yocto)** 플랫폼 경험이 있습니다. 자동차 전장 ECU SW 분야로 경력을 확장하며 **AUTOSAR Classic(BSW/RTE) 및 임베디드 C 기반 ECU 개발**에 기여하고자 합니다.

---

## Core Competencies

- **Embedded / Low-level SW:** Linux C driver, register-level integration, communication protocol stack (RS422, HDLC, UDP/TCP)
- **Real-time Systems:** Multi-subsystem integration (7 modules), event-driven control, deterministic timing (NTP/GPS sync, 20ms control cycle)
- **SW Abstraction / Migration:** Legacy commercial driver → custom HW **API-compatible layer** (BSW/CDD 유사 구조)
- **Application SW:** Real-time control & monitoring application (C#, operation logic owner)
- **Integration & Validation:** Field bring-up, hardware-in-the-loop style integration debug, 2+ years on-site
- **Technical Leadership:** Interface & integration guide for scheduler module (tech lead)
- **Platform:** Embedded Linux (Yocto), Python/C# test & verification tools

---

## Experience

### (주)___________ | Embedded / Real-time Systems Engineer
**20__ – Present**

#### Project A — Real-time Precision Control Platform (Operational Control SW) | 2023.01 – 2025.10
*정밀 실시간 다모듈 통합 시스템 (7 subsystems + multi-sensor)*

- **System logic owner** (except scheduler module): design, implementation, and **2-year field deployment**
- Integrated **7 subsystems** (event timer, optoelectronics, laser, mount, detection, environment, external network) with **multi-channel sensors/actuators**
- Implemented **deterministic time synchronization** (NTP/GPS), **event-timer control**, and **20ms real-time actuator control loop**
- Developed **closed-loop calibration** logic and tuning → contributed to **≤50 arcsec** system precision
- Built **multi-protocol real-time communication** and operational monitoring application
- **On-site:** concurrent **SW development, HW integration debug, and operational validation** (not maintenance-only)
- **Tech lead:** defined interfaces & timing for **scheduler module** (teammate implementation) — cross-module integration

#### Project B — Communication Card Migration (FPGA / SBC) | 2025.10 – Present

- Replaced commercial communication card with in-house FPGA: **compatibility layer & test applications (sole owner)**
- **8-channel** serial comms: RS422 ×7 + HDLC ×1 (50B@200Hz / 200B@1Hz)
- **Low-level driver logic modification** for legacy third-party application compatibility (HDLC framing)
- Pre-integration **mock testing** with PC-side requirements → reduced requirement change cycle

#### Project C — LEO Tracking Control Application | 2026.01 – Present

- **Solo development:** 7-subsystem **UDP** integration, multi-camera display/control, real-time UI (WPF)

#### Project D — Embedded Platform Bring-up | 2025.10 – 2026.01

- **Yocto** image build, boot validation, video pipeline (project paused)

#### Earlier

- Firmware, Linux device driver, sensor **R&D test program** development

---

## Technical Skills

| Category | Skills |
|----------|--------|
| **Language** | **C** (driver, embedded), C#, Python, C++ |
| **Embedded** | Linux device driver, Yocto, register map / HW abstraction, RS422, HDLC |
| **Real-time** | Multi-subsystem integration, time sync, event scheduling, control loop |
| **Communication** | TCP/UDP, serial protocols, multi-channel I/O |
| **Tools** | Git, test automation (Python, C#) |
| **Learning** | AUTOSAR Classic (BSW/RTE/ASW), CAN/LIN, ISO 26262 overview |

---

## Education / Certificates
(작성 필요)

---

## 자기소개 (지원 동기 — 500자 내외 초안)

자동차 전장은 제가 7년간 해온 **실시간 임베디드·다모듈 통합**과 가장 가까운 산업입니다. 정밀 실시간 시스템에서 7개 모듈을 연동하고, ns급 시간 동기화와 20ms 제어 루프를 구현하며, 2년간 현장에서 **개발과 통합 검증을 병행**했습니다. 상용 드라이버를 자체 HW로 대체하는 과정에서 **API 호환 추상화 레이어**와 **드라이버 로직 수정**을 수행했으며, 이는 AUTOSAR 환경의 **CDD/BSW 통합**과 같은 문제 구조라고 이해하고 있습니다.

계양전기의 **모터 ECU SW(임베디드·BSW·MBD)** 는 제가 강점을 가진 **로우레벨~응용** 스펙트럼에서 성장할 수 있는 직무라 판단했습니다. AUTOSAR BSW(Mobilion)와 MBD는 입사 후 집중 학습할 영역이며, 이미 보유한 **통합·드라이버·현장 검증** 역량으로 빠르게 기여하겠습니다.

---

## 이력서 작성 메모 (본인용, 제출 X)

### 강조한 것
- C, driver, real-time, integration, field
- 7 modules → automotive multi-ECU narrative
- compat layer → BSW/CDD analogy (면접에서만 깊게)

### 줄인 것
- PostgreSQL, Cesium, 천문, SLR, 우주
- OpenCV (한 줄도 없음 — 전장 SW JD 무관)
- C# 비중 (application으로만)

### 면접 예상 질문
1. AUTOSAR 경험? → 솔직히 학습 중 + CDD 유사 경험
2. CAN? → RS422/HDLC 다채널 경험, CAN 학습 중
3. MBD? → 제어 루프 C 구현 경험, Simulink 학습 의지
4. 왜 계양전기? → 모터 ECU = 실시간 embedded, 안정적 전장 Tier

---

## PDF 변환 체크리스트

- [ ] 이름·연락처·학력 입력
- [ ] 회사명 (공개 가능 범위)
- [ ] 2페이지 이내 권장
- [ ] 사진·연봉·주민번호 **미포함**
- [ ] 파일명: `이름_계양전기_SW설계_경력.pdf`
