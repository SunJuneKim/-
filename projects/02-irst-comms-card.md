# 프로젝트: IRST (통신카드 대체)

> NSLR과 **별개**. 경력기술서 본문: `resume/career-technical-resume.md`

---

## 개요

| | |
|---|---|
| 기간 | **2026.01 – 2026.06** |
| 역할 | 호환 레이어 · Linux driver · 검증 앱 — **단독** |
| 병행 | **2026.01~** 저궤도 운영제어 **동시 진행** |

---

## 통신 사양

| ch | 프로토콜 | IF | payload | rate |
|----|----------|-----|---------|------|
| 7 | RS422 | tty | 200 B | 1 Hz |
| 1 | HDLC | ioctl | 50 B | 200 Hz |

**8ch 동시**, 이기종 주기.

---

## 타임라인

```
01–02월   맵핑·드라이버 분석
03월 중   HIL → 1차 납품
04–06월   앱 스펙 반영(8ch 동시) 재작업 → 재납품
          (중간 ~2개월 간격)
```

---

## 기술

- FIFO → **ring buffer**
- 0byte / split RX → driver **header parse** (app frozen)
- **70h+** soak test

---

## 이력서 한 줄

8ch RS422/HDLC Linux driver·compat layer, HIL·납품, spec change rework, 70h validation
