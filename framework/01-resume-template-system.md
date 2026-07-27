# 양산형 이력서 시스템

> 회사마다 처음부터 쓰지 않는다. **마스터 → 변환 → PDF**

---

## 디렉터리 규칙

```
framework/
  00-master-profile.md      ← 팩트 원본 (항상 최신)
  01-resume-template-system.md
  02-keyword-mapping-*.md   ← 도메인별 용어 변환

companies/
  <회사명>/
    01-company-analysis.md
    02-roles-comparison.md
    03-gap-analysis-by-role.md
    04-resume-<직무>.md     ← 제출용 초안
    05-prep-checklist.md
    status.md               ← 지원 상태 추적
```

---

## 5단계 워크플로 (회사 1곳당 ~2시간 목표)

| 단계 | 작업 | 산출물 |
|------|------|--------|
| 1 | 회사·공고 분석 | `01-company-analysis.md` |
| 2 | 직무 比교 + 추천 | `02-roles-comparison.md` |
| 3 | 갭 분석 + 보강 계획 | `03-gap-analysis-by-role.md` |
| 4 | 키워드 매핑 후 이력서 생성 | `04-resume-*.md` |
| 5 | 체크리스트·면접 준비 | `05-prep-checklist.md` |

---

## 이력서 섹션 템플릿 (복붙)

```markdown
# [이름] | [Headline — 직무별 변경]

## Summary (3문장)
[오너십] + [도메인 키워드] + [정량 성과 1개]

## Core Competencies (5 bullet)
- ...

## Experience
### [회사] | [직함]
#### [프로젝트] | [기간]
- [자동차 키워드로 변환된 bullet × 3~5]

## Technical Skills
[JD 순서로 재정렬]

## Education / Certs
```

---

## 직무별 Headline 프리셋

| 타입 | Headline 예시 |
|------|---------------|
| **임베디드 SW 설계** | Embedded SW Engineer \| Real-time \| Driver · Integration · Application |
| **시스템 설계** | System Design Engineer \| Requirements · Safety · Multi-subsystem Integration |
| **SW 검증** | SW Verification Engineer \| Integration Test · Field Validation · Real-time Systems |
| **자율주행/SDV** | Real-time Vision & Embedded Systems Engineer |
| **방산/항공 (원본)** | Real-time Sensor & Control Systems Engineer |

---

## 변환 규칙 (공통)

| 원본 (방산/항공) | 변환 (자동차 전장) |
|------------------|-------------------|
| 7구성품 연동 | Multi-subsystem / multi-ECU integration |
| NTP/GPS ns 동기화 | Deterministic timing / time sync |
| 호환 레이어 | Abstraction layer / legacy SW migration (CDD 유사) |
| 드라이버 modify | Low-level SW / communication stack |
| 현장 연동·관측 | ECU bring-up / integration validation |
| 50 arcsec | Closed-loop control precision (수치 유지 가능 시) |
| Yocto | Embedded Linux platform |
| RS422/HDLC | Serial communication protocol stack |

### 숨기거나 축소
- PostgreSQL, Cesium, 천문, 우주물체 세부
- 한화시스템 실명 (→ "대형 시스템 통합 협력사")
- 보안등급·군사 용어

### 강조
- C, 실시간, 드라이버, 통합, 현장, 정밀 제어, 사수(리드)

---

## status.md 템플릿

```markdown
# [회사명] 지원 현황
| 항목 | 내용 |
|------|------|
| 1차 필터 | ✅ 연봉/전망 |
| 지원 직무 | SW 설계 엔지니어 |
| 제출일 | |
| 전형 | |
| 결과 | |
```
