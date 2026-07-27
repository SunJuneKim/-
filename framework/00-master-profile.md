# 마스터 프로필 (Canonical Source)

> **원칙:** 모든 회사별 이력서는 이 파일에서 **추출·변환**한다. 여기만 최신 유지.

---

## 기본

| 항목 | 값 |
|------|-----|
| 경력 | 7년차 (확인 필요) |
| 정체성 | **실시간 임베디드 · 시스템 통합 · 응용 SW** 풀스택 엔지니어 |
| 강점 축 | 로우레벨(드라이버/FW) + 시스템 통합 + 응용(운영제어) + 현장 검증 |

---

## 프로젝트 요약 (팩트)

### NSLR (2023.01–2025.10)
- 차세대 **SLR** 운영제어부 **시스템 로직 단독** (Scheduler 제외)
- Scheduler: 동료 개발, 본인 **사수**
- 7구성품 + 3카메라, NTP/GPS ns급 동기화, 별보정, 50 arcsec 기여
- 현장: 구현·연동·관측 병행

### XMC HDLC (2025.10–현재)
- 호환 레이어·응용 SW 단독 → 드라이버 로직 modify
- RS422 7ch + HDLC 1ch

### 저궤도 (2026.01–현재)
- 운영제어부 1인, UDP, Cesium/TLE/SGP4, WPF

### 지능형 조준경 (2025.10–2026.01)
- Yocto, 부팅·영상 (보류)

### 초기
- 펌웨어, Linux driver, 센서 시험 SW

---

## 기술 스택 (레벨)

| 기술 | 수준 | 비고 |
|------|------|------|
| C (Linux driver) | ★★★★ | 실무 |
| C# / WPF / WinForms | ★★★★★ | NSLR·저궤도 |
| C++ | ★★★ | 보강 필요 |
| Python | ★★★ | 테스트 |
| Yocto / Embedded Linux | ★★★ | 프로젝트 경험 |
| OpenCV / Vision | ★★★★ | NSLR |
| RS422 / HDLC / UDP / TCP | ★★★★ | |
| NTP/GPS / real-time sync | ★★★★★ | 차별화 |
| **AUTOSAR / BSW** | ★☆☆☆☆ | **학습 필요** |
| **MBD / Simulink** | ★☆☆☆☆ | **학습 필요** |
| **CAN / LIN** | ★★☆☆☆ | 유사 경험만 |
| **ISO 26262 / ASPICE** | ★☆☆☆☆ | 개념 수준 |
| ROS/ROS2 | ★☆☆☆☆ | 42dot용 |

---

## 어필 키워드 (업종 무관)

```
Real-time embedded | Multi-subsystem integration | Driver/HW abstraction
Field bring-up | System logic owner | Tech lead (integration)
Deterministic timing | Legacy compatibility layer | Platform porting
```

---

## 지원 전략

1. **1차 필터:** 연봉·전망·직무 적합도 (본인)
2. **2차:** 이 repo `companies/<회사>/` 폴더 생성
3. **3차:** `framework/02-keyword-mapping-<도메인>.md`로 키워드 변환
4. **4차:** `companies/<회사>/resume-<직무>.md` → PDF

---

## 업데이트 로그

| 날짜 | 내용 |
|------|------|
| 2026-07-27 | 계양전기 타겟 추가, 자동차 키워드 매핑 시작 |
