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

펌웨어·Linux 디바이스 드라이버에서 운영제어·영상 파이프라인, 현장 통합·검증까지 **장비 시스템 전 스택**을 경험했습니다. 3년간 우주물체 추적·정밀측정 시스템 운영제어부를 개발·현장 운영하며, 다수 구성품·다채널 카메라의 **실시간 동기화(NTP/GPS)** 및 **ns급 타이밍 이슈** 대응 역량을 쌓았습니다. 현재는 상용 통신카드를 자체 FPGA 카드로 대체하는 **드라이버 호환 레이어** 및 **8채널 RS422/HDLC** 통신을 담당하고 있습니다.

**Core:** C/C++, Linux, Camera/Vision pipeline, Multi-sensor integration, Real-time control, Yocto, PostgreSQL, Field deployment

---

## 핵심 역량

- **실시간 시스템 통합**: 6~7개 구성품, 4PC 분산 아키텍처, TCP/UDP, NTP/GPS 동기화
- **영상 시스템**: MWIR/CCD/EMCCD acquisition, OpenCV (AGC, ROI, Mono8), overlay, thermal
- **임베디드**: Linux C driver, Yocto, FPGA 통신카드 레지스터 호환, SCC 리맵
- **보정·정밀도**: 별보정(calibration) 파라미터 분석·튜닝, 50 arcsec 이하 기여
- **현장·검증**: 2년+ 협력사 현장 상주, 설치·유지보수·디버깅

---

## 경력

### (주)_______ | 실시간 시스템 / 영상 / 임베디드 엔지니어
**20__ ~ 현재**

#### 프로젝트 A: 우주물체 추적·정밀측정 시스템 (NSLR) | 2023.01 – 2025.10
- NSLR 시스템 **운영제어부** 개발 (2명, 한화시스템 협업, 거창 현장)
- 3종 카메라(MWIR/CCD/EMCCD) acquisition·OpenCV 전처리(AGC/ROI)·전시
- 6개 구성품 실시간 통신·동기화, NTP/GPS 기반 시간 동기화, 마운트 20ms 제어, 위성 트래킹
- 별보정 라이브러리 파라미터 분석·최적화 → **50 arcsec 이하** 정밀도 기여
- 4PC(관측/전시/처리/관리) 분산 구조, PostgreSQL 운영 DB, 대기환경 센서 데이터 관리
- 아키텍처 제약 하 timing jitter 최소화 튜닝으로 운영 안정성 확보

#### 프로젝트 B: XMC 자체 HDLC/RS422 통신카드 | 2025.10 – 현재
- 상용 드라이버(tdrv009/002) → 자체 FPGA 카드 **Linux 호환 레이어** (2명)
- RS422 7ch + HDLC 1ch, HDLC 50B@200Hz / RS422 200B@1Hz
- 레거시 유저 앱 무수정 호환 (자체 앱); 업체 레거시 앱 HDLC stash/split 이슈 디버깅 중

#### 프로젝트 C: 저궤도 우주물체 운영제어부 | 2026.01 – 현재
- 운영제어부 **1인 개발**: 7구성품, 3카메라, Cesium 궤도 추적, 조이스틱 마운트 제어 (WPF/C#)

#### 프로젝트 D: 지능형 조준경 사내화 | 2025.10 – 2026.01
- Yocto 이미지 빌드, 부팅·영상 전시 (프로젝트 보류)

#### 기타
- 자이로 센서 등 다수 R&D **시험용 프로그램** 제작
- 펌웨어·HW, Linux driver 초기 경력

---

## 기술 스택

| 분류 | 기술 |
|------|------|
| Language | C, C++, C#, Python |
| OS/Embedded | Linux, Yocto, Device Driver |
| Vision | OpenCV, Camera SDK (MWIR/CCD/EMCCD) |
| DB | PostgreSQL |
| UI | WinForms, WPF, Cesium |
| Network | TCP/IP, UDP, RS422, HDLC, NTP/GPS |
| Domain | Real-time sync, Calibration, System integration |

---

## 학력
(작성 필요)

---

## 자격증 / 어학
(작성 필요 — 영어: 기술면접 준비 중)

---

## 포트폴리오 / 링크
- [ ] ROS2 mini project (예정)
- [ ] GitHub: (공개 가능 프로젝트)

---

## 작성 메모
- 42dot 제출: PDF 30MB↓, 사진·연봉·주민번호 제외
- 방산 세부 스펙 삭제, 성과 위주
