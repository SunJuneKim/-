# 경력기술서 초안 (포티투닷 Software Engineer AD 타겟)

> PDF 변환 전 초안. 민감정보·보안등급·고객 실명은 최종 전 확인.

---

## 인적사항 (placeholder)

| 항목 | 내용 |
|------|------|
| 이름 | (작성 필요) |
| 경력 | 7년 |
| 학력 | (작성 필요) |
| 연락처 | (작성 필요) |
| 희망직무 | Software Engineer (Autonomous Driving) |

---

## Professional Summary

**실시간 영상·센서 통합 / 임베디드 시스템 엔지니어 (7년)**

펌웨어·Linux 드라이버에서 운영제어·영상 파이프라인, **현장 구현·실장비 연동·관측 운영**까지 장비 시스템 전 스택을 경험했습니다. 약 3년간 **차세대 SLR(NSLR)** 운영제어부 **시스템 로직(스케줄러 제외)을 단독** 설계·구현·운영했으며, 관측 스케줄러 모듈은 동료 개발에 **사수(기술 리드)** 로 인터페이스·통합을 가이드했습니다. 7개 구성품·3종 카메라의 **NTP/GPS ns급 시간동기화**, 별보정·위성 트래킹 로직을 담당했습니다. 현재는 상용 통신카드 대체 프로젝트에서 **호환 레이어·응용 SW**를 구축하고 **드라이버 로직**을 직접 수정 중입니다.

**Core:** C/C++, Linux/Driver, Camera/Vision pipeline, Multi-sensor integration, Real-time sync, Yocto, PostgreSQL, Field deployment

---

## 핵심 역량

- **운영제어부 단독 개발**: 7구성품 + 3카메라, 4PC 분산, NTP/GPS ns급 동기화, 별보정·트래킹 로직
- **현장 풀스택**: 거창 2년 — 구현·실장비 디버깅·관측 운영 병행 (한화시스템 협업)
- **영상**: MWIR/CCD/EMCCD, OpenCV (AGC, ROI), thermal pipeline
- **임베디드**: Linux C driver modify, 호환 레이어, Yocto, RS422/HDLC 8ch
- **궤도 UI**: Cesium, TLE/SGP4 (저궤도 프로젝트)

---

## 경력

### (주)_______ | 실시간 시스템 / 영상 / 임베디드 엔지니어
**20__ ~ 현재**

#### 프로젝트 A: 차세대 SLR(NSLR) 운영제어부 | 2023.01 – 2025.10
- **NSLR** 운영제어부 **시스템 로직 단독** (스케줄러 제외) — GitHub 소스 기준 담당 범위
- **7구성품** + **3카메라** 실시간 연동; 시간동기화·별보정·트래킹·영상·DB·타과제 외부망
- 관측 **스케줄러**: 동료 개발, 본인 **사수** — 인터페이스·통합·아키텍처 가이드
- NTP/GPS **ns급** 동기화, **50 arcsec 이하** 기여; 현장 **구현·연동·관측** 2년

#### 프로젝트 B: XMC HDLC/RS422 통신카드 | 2025.10 – 현재
- 상용(tdrv009/002) → 자체 FPGA: **호환 레이어·응용 SW 단독** 개발
- RS422 7ch + HDLC 1ch (50B@200Hz / 200B@1Hz)
- 레거시 업체 앱 호환: **드라이버 로직 직접 modify** (HDLC stash/split)

#### 프로젝트 C: 저궤도 우주물체 운영제어부 | 2026.01 – 현재
- **1인 개발**: 7구성품 **UDP**, 3카메라, **Cesium·TLE/SGP4**, 조이스틱 (WPF)

#### 프로젝트 D: 지능형 조준경 사내화 | 2025.10 – 2026.01
- Yocto 빌드, 부팅·영상전시 (보류)

#### 기타
- 자이로 센서 등 R&D 시험 프로그램, 펌웨어·Linux driver 초기 경력

---

## 기술 스택

| 분류 | 기술 |
|------|------|
| Language | C, C++, C#, Python |
| OS/Embedded | Linux, Driver, Yocto, FPGA comms |
| Vision | OpenCV, MWIR/CCD/EMCCD SDK |
| DB | PostgreSQL |
| UI | WinForms, WPF, Cesium (TLE/SGP4) |
| Network | TCP/UDP, RS422, HDLC, NTP/GPS |
| Domain | SLR, Real-time sync, Calibration, System integration |

---

## 학력 / 어학 / 포트폴리오
(작성 필요)

- [ ] ROS2 mini project (예정)

---

## 작성 메모
- "현장 상주" → **구현·연동·관측 병행** 강조 (유지보수만 X)
- 마운트 **엔코더 정밀도**는 본인 영역 아님 — 과장 금지
- 42dot: PDF 30MB↓, 금지정보 제외
