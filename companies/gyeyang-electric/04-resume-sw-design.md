# 김선준 — 계양전기 SW 설계 엔지니어 (제출용)

> **지원:** 전장 SW 설계 (임베디드 SW · MBD · BSW / Mobilion AUTOSAR)  
> PDF 변환용 · 2페이지 목표 · 사진·연봉·주민번호 미포함

---

## 김선준

**Embedded / Real-time Systems Engineer** · 7년 3개월  
fly881004@naver.com · 010-4377-1920 · 경기 성남시 분당구

---

## Summary

MCU 기반 **임베디드 제어**에서 **다모듈 실시간 시스템 통합·저수준 SW**까지 7년 이상 경험한 선임 연구원입니다. STM32/MSP430 펌웨어·**Calibration**·통신(SPI/UART/Modbus) 개발로 시작해, 현재는 **7개 서브시스템 실시간 연동**, **NTP/GPS ns급 동기화**, **20ms 제어 루프**, **Linux 통신 드라이버 수정** 및 **레거시 SW 호환 추상화 레이어**를 담당합니다. 2년 이상 **현장 ECU급 통합·검증(TRR·납품)** 을 병행했으며, 자동차 전장 **모터 ECU SW(임베디드·BSW)** 분야로 경력을 확장합니다.

---

## Core Skills

**Language:** C (MCU, Linux driver), C#, Python, C++  
**Embedded:** STM32, MSP430, Linux device driver, Yocto, register-level HW integration  
**Communication:** TCP/UDP, RS422, HDLC, SPI, UART, Modbus RTU, RS232  
**Real-time:** Multi-subsystem integration, event scheduling, deterministic timing, closed-loop calibration  
**Tools:** ATE sequence, PostgreSQL, Git, test automation (Python/C#)  
**Learning:** AUTOSAR Classic (BSW/RTE/ASW), CAN/LIN, ISO 26262 overview

---

## Experience

### ㈜신보 · 소프트웨어팀 · 선임연구원 | 2023.01 – Present

#### NSLR — Satellite Laser Ranging 운영제어 SW | 2023.01 – Present
*Multi-subsystem real-time control platform (7 modules + multi-sensor)*

- **System logic owner** (except scheduler): design, implementation, **2+ years field deployment** (TRR, delivery)
- Integrated **7 subsystems** via Ethernet (TCP/UDP): event timer, optoelectronics, laser, mount, detection, environment, external network
- **Deterministic time sync** (NTP/GPS), **20ms real-time control loop**, closed-loop calibration → **≤50 arcsec** precision contribution
- Application & operation logic (C#, WinForms); Python/PostgreSQL **data analysis**; external **.dll library** integration
- **Tech lead:** scheduler module (teammate dev) — interface, timing, integration guide
- **Leadership:** 4× customer PM changes — requirements analysis, stabilization; voluntary **Python analysis tool** during blocked test windows
- On-site: **SW development + HW integration debug + operational validation** (not maintenance-only)

#### XMC Communication Card Migration | 2025.10 – Present
- Commercial → in-house FPGA card: **compatibility layer & apps (sole owner)**
- RS422 ×7 + HDLC ×1; **low-level driver logic modification** (legacy app HDLC framing)

#### LEO Tracking Control SW | 2026.01 – Present
- Solo: 7-subsystem UDP integration, multi-camera, WPF/Cesium orbit UI

#### Embedded Platform (Yocto) | 2025.10 – 2026.01
- Image build, boot, video pipeline (project paused)

---

### ㈜아트랩소프트 · SE부서 · 주임 | 2019.06 – 2021.03

#### Nuclear ESF-CCS System — SW Verification | 2019.06 – 2020.06
- Verification planning, test case design, unit/integration/system test execution
- *Quality & V-model mindset — applied to current integration validation*

---

### 에너시스㈜ · 부설연구소 · 연구원 | 2017.06 – 2019.03

#### Voltage/Current I/O Card | 2017.06 – 2017.11
- **STM32** firmware: SPI/UART, Median/Moving-Avg filter, **calibration** (4-20mA, lookup table, temp compensation)
- Precision tuning, PCB assembly support, chamber test

#### Apartment Shelter System | 2017.12 – 2018.04
- **MSP430**: Modbus RTU, RS232, multi-SPI/I2C, ADC, GUI
- Sensor circuit tuning, **EMI certification** support

#### SSILS Electronic Card Module | 2018.06 – 2018.11
- **ATE (Auto Test Environment)** sequence design & implementation
- **160 hours** investment → test time reduced to **1/10**; annual 100-unit production test support

---

## Education

**서울과학기술대학교** · 전자미디어IT공학과 · 학사 (2008–2015, 3.2/4.5)  
**MDS아카데미** · 임베디드 시스템 개발자 양성과정 (2016.07–2016.11)

---

## 자기소개 (지원 동기 — 약 400자)

저는 **MCU 펌웨어(Calibration·통신)** 로 시작해 **대규모 실시간 통합 시스템**까지 경험한 임베디드 엔지니어입니다. 현재 NSLR 운영제어에서 7개 모듈 연동·ns급 동기화·현장 TRR/납품을 수행했고, 통신카드 프로젝트에서는 **드라이버 호환 레이어·저수준 수정**을 담당하고 있습니다. 에너시스 시절 **STM32 제어·보정**과 **ATE 자동화(시험시간 1/10)** 경험은 계양전기 **모터 ECU·전장 SW**와 직결됩니다. AUTOSAR BSW(Mobilion)와 MBD는 입사 후 집중 학습할 영역이며, **통합·드라이버·현장 검증** 역량으로 빠르게 기여하겠습니다.

---

## 제출 체크

- [x] 인적사항 반영
- [ ] 공고별 희망연봉·주소 생략 확인
- [ ] PDF 2페이지 압축 (필요 시 아트랩 1줄로 축소)
- [ ] 파일명: `김선준_계양전기_SW설계_경력.pdf`
