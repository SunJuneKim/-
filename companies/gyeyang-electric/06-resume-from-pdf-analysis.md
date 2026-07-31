# 기존 PDF 이력서 분석 · 계양전기용 개선점

> 원본: [`resume/pdf/이력서_20260731.pdf`](../../resume/pdf/이력서_20260731.pdf) (2026-07-31 웍스피어 형식)  
> 개선본: [`04-resume-sw-design.md`](04-resume-sw-design.md) + [`resume/career-technical-resume.md`](../../resume/career-technical-resume.md)

---

## 원본 강점 (유지)

| 항목 | 내용 |
|------|------|
| **임베디드 뿌리** | 에너시스 STM32/MSP430, Calibration, EMI — **자동차 SW에 필수** |
| **ATE 자동화** | 160h → 시험 1/10 — **정량 성과** |
| **에너시스 프로젝트 상세** | 전압전류카드·대피구·SSILS — 경력기술서 형식 우수 |
| **승진** | 선임연구원 |
| **분당 거주** | 계양전기 분당 사무소와 **근접** |

---

## 원본 약점 → 개선 완료 (2026-07-31)

| 문제 (원본 PDF) | 개선 |
|-----------------|------|
| 신보 "경력기술서 참조"만, bullet 파편 | **IRST·NSLR 상세 bullet** 추가 |
| 자기소개 "임베디드 2년 + V&V 2년" (구식) | **7년 3개월·드라이버·통합** 기준 갱신 |
| 희망분야 **반도체** (오지원) | **전장 SW 설계** 로 변경 |
| IRST/XMC 상세 없음 | RS422 7ch + HDLC, HIL, 70h+, 납품 |
| NSLR 기간·역할 불명확 | 2023.01–2025.10, 시스템 로직 오너 |
| 계양전기 키워드 없음 | Embedded, driver, HIL, calibration, AUTOSAR 학습 |
| C#/WinForms만 앞세움 | **C, driver, MCU, 통합** 균형 |

---

## PDF → 개선본 파일 매핑

| PDF 섹션 | 개선본 위치 |
|----------|-------------|
| 1페이지 인적·경력 요약 | `04-resume-sw-design.md` |
| 에너시스 프로젝트 상세 | `career-technical-resume.md` §4 |
| 자기소개·성과 STAR | `career-technical-resume.md` §7 + `07-cover-letter.md` |
| 희망근무조건 | `04-resume-sw-design.md` 하단 (반도체 삭제) |

---

## 제출 파일명 (권장)

1. `김선준_계양전기_SW설계_이력서.pdf` ← `04-resume-sw-design.md`
2. `김선준_계양전기_SW설계_경력기술서.pdf` ← `career-technical-resume.md`
3. (선택) 지원동기 ← `07-cover-letter.md`

---

## 경력 공백 (2021.03 – 2023.01)

- **이력서:** 항목 추가 **안 함**
- **면접:** `resume/career-gap-2021-2023.md` 참고
