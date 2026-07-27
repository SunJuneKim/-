# 계양전기 — 직무별 갭 분석 · 보강 계획

---

## SW 설계 엔지니어 (지원 직무)

### JD 요구 vs 본인

| 요구 | 본인 | 갭 | 대응 |
|------|------|-----|------|
| 임베디드 C | Linux driver, C 실무 | MCU bare-metal 약함 | **C 포인터·비트연산·ISR** 복습 |
| BSW / AUTOSAR | 없음 | **★★★★★** | 개념 학습 + Mobilion/Vector 자료 |
| MBD / Simulink | 없음 | **★★★★☆** | 입사 후 학습 가능 — 면접에서 **의지** 표현 |
| 모터 제어 | 마운트 20ms (유사) | 도메인 | **BLDC/FOC** 개요만 |
| CAN/LIN | RS422/HDLC | **★★★☆☆** | CAN 2.0 튜토리얼 1주 |
| 통합·디버깅 | **강함** | — | 이력서 **메인** |
| Yocto/Embedded Linux | 있음 | — | 어필 |
| ISO 26262 / ASPICE | 없음 | **★★★☆☆** | 개요 4시간 |

### 이력서 전략 (갭 메우기 — 거짓 없이)

1. **AUTOSAR:** "Classic AUTOSAR 아키텍처(BSW/RTE/ASW) 학습 중" — 자소서/면접
2. **BSW 유사:** 호환 레이어 → **"legacy driver API abstraction, register-level integration"**
3. **MBD:** "모델 기반 개발은 신규 학습 예정, **실시간 제어 루프 C 구현** 경험 보유"
4. **모터:** 마운트 20ms, closed-loop calibration → **actuator real-time control**

### 4주 보강 (SW 설계 지원 후에도 유지)

| 주차 | 내용 |
|------|------|
| 1 | AUTOSAR Classic 구조 (BSW/RTE/ASW/CDD) 유튜브·문서 |
| 2 | CAN protocol + socketCAN 또는 시뮬 |
| 3 | C embedded kata (링버퍼, 상태머신, ISR mock) |
| 4 | ISO 26262 Part 6 개요, ASPICE V-Model 그림 암기 |

---

## 시스템 설계 엔지니어 (미지원)

| 요구 | 본인 | 갭 |
|------|------|-----|
| 요구사양 분석 | 통합 인터페이스 정의 (사수) | OEM 프로세스 |
| 상세 설계 | 7모듈 아키텍처 | ASPICE 산출물 |
| FMEA/FTA | timing 오차 구조 분석 | **공식 방법론** |
| 이슈 관리 | 현장 이슈 대응 | Jira/DOORS 등 |

**보강 (나중에):** FMEA 템플릿 1개 작성 연습, SyRS 샘플 읽기

---

## SW 검증 엔지니어 (미지원)

| 요구 | 본인 | 갭 |
|------|------|-----|
| 단위 테스트 | 시험 SW 제작 | Google Test / CUnit |
| 통합 테스트 | **현장 통합 강함** | 자동화 프레임워크 |
| 커버리지 | — | MC/DC 개념 |
| HIL | — | 장비 경험 없음 |

**참고:** 검증 지원 안 해도, SW 설계 이력서에 **"integration validation, field bring-up"** 으로 흡수

---

## 오늘 면접 전 최소 준비 (2시간)

- [ ] AUTOSAR 3계층 그림 그려보기
- [ ] BSW / RTE / ASW / CDD 한 줄씩 설명
- [ ] 본인 호환 레이어 → CDD 비유 스크립트 암기
- [ ] 계양전기 제품: 시트모터, EPB 한 줄
