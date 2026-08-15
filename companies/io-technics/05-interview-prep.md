# 이오테크닉스 — 면접 준비

> 직무: 장비 SW · 면접 전 체크리스트

---

## 면접 전 필수 (30분)

- [ ] 1분 자기소개 암기 (`07-cover-letter.md` 하단)
- [ ] IRST STAR 2분 (Situation→Task→Action→Result)
- [ ] NSLR Timing Jitter STAR 2분
- [ ] 왜 이오테크닉스? 30초
- [ ] 경력 공백 60초 (`resume/career-gap-2021-2023.md`)

---

## 예상 질문 & 답변 요지

### 지원 동기

Q. 왜 이오테크닉스인가요?

> 반도체·디스플레이 레이저 장비는 HW 제어와 SW 안정성이 제품 경쟁력과 직결됩니다. 저는 다수 장비 통합 GUI, Driver·HIL 검증, 현장 통합 시험을 해 왔고, 장비가 실제로 돌아가는 구조를 이해한 상태에서 SW를 만드는 쪽이 강점입니다. 레이저 응용 장비 분야에서 그 역량을 쓰고 싶어 지원했습니다.

### 직무 역량

Q. 장비 SW 경험이 있나요?

> C# WPF·WinForms로 7개 장비 UDP/TCP 통합 제어 GUI를 단독·핵심 개발했습니다. 단순 UI가 아니라 NTP/GPS 동기화, 20ms 제어 루프 상태 모니터링, PostgreSQL 데이터 연동, Cesium 3D 시각화까지 포함된 운영제어 SW입니다. Qt GUI(대피구), C#/Python HIL Test Tool(IRST) 경험도 있습니다.

Q. MFC/C++는요?

> 주력은 C# WPF·WinForms입니다. MFC 직접 실무는 제한적이지만, 장비 SW에서 중요한 건 HW 인터페이스 이해·멀티스레드·실시간 통신 처리이고 이 부분은 NSLR·IRST·에너시스에서 해 왔습니다. MFC는 유지보수·신규 기능 관점에서 빠르게 적응할 자신 있습니다.

Q. Driver를 왜 알아야 하나요?

> IRST에서 Application 수정 없이 FPGA 카드 호환을 Driver에서 맞췄습니다. 장비 SW 담당자가 Driver·통신 예외를 이해해야 현장 이슈를 SW·HW 중 어디서 볼지 판단할 수 있고, Test Tool·HIL 설계도 정확해집니다.

### 기술 심화

Q. UI 지연 없이 실시간 모니터링은 어떻게?

> NSLR에서 20ms 제어 상태를 UI에 반영할 때 비동기 아키텍처로 통신·처리·UI 스레드를 분리했습니다. UI는 최신 상태 스냅샷만 받고, 무거운 처리는 백그라운드에서 돌렸습니다.

Q. TCP/UDP·Serial 경험?

> TCP/UDP: NSLR 7장비, 저궤도 UDP 7장비. Serial: RS422 7ch, HDLC, RS485 Modbus RTU, SPI/UART(I2C). 프로토콜마다 주기·패킷 구조가 달라 동시 수신 설계가 필요했습니다.

Q. HIL이 뭔지, 왜 만들었나요?

> Hardware-In-the-Loop. IRST에서 실제 FPGA 카드와 PC Application을 붙여 Driver를 검증했습니다. Test Tool을 직접 만든 이유는 Split RX·Zero-length 같은 예외를 반복 재현하고 70시간 연속 로그를 봐야 했기 때문입니다.

### 약점·갭

Q. 반도체 장비/SECS-GEM 경험?

> 직접 SECS/GEM 구현 경험은 없습니다. 다만 다수 장비 인터페이스 정의·통합 시험·요구사항 기반 검증(ESF-CCS)은 해 왔고, 표준 통신은 입사 후 빠르게 학습하겠습니다.

Q. 레이저·모션 제어?

> 레이저 제어 직접 경험은 없습니다. 20ms 실시간 루프, Calibration, Timing Jitter 튜닝 경험으로 정밀 제어 환경에는 익숙합니다.

### 인성·현장

Q. 출장·야근 가능?

> NSLR 2년 이상 현장 상주(거창), 평일 장시간 운영·연동 경험 있습니다. 장비 SW는 현장 검증이 필수라고 봅니다.

Q. 혼자 일한 경험?

> 저궤도 운영제어 1인 개발, IRST Driver·Test Tool 단독, NSLR 시스템 로직 단독(스케줄러 제외). 협업 시에는 인터페이스 규격 문서화·통합 가이드로 맞춥니다.

---

## STAR — IRST (2분)

| | 내용 |
|---|------|
| S | 상용 통신카드→FPGA 교체, Application 무수정 |
| T | Driver Layer 완전 호환, RS422 7ch+HDLC 동시 |
| A | Register Map 분석, 순환 Queue, 예외 처리, C#/Python Test Tool, HIL 70h |
| R | 2차 납품 완료, Application 수정 0% 유지 |

## STAR — NSLR Timing (2분)

| | 내용 |
|---|------|
| S | 7장비 실시간 연동, 현장 Timing Jitter로 정밀도 저하 |
| T | 구조 변경 불가, 운영 안정화 필요 |
| A | Python Timing 분석 도구 제작, NTP/GPS·20ms Loop 튜닝 |
| R | 50 arcsec 이하 안정화, TRR·납품 기여 |

---

## 역질문 (2~3개)

1. 장비 SW팀에서 신규 개발과 레거시(MFC) 유지보수 비중이 어떻게 되나요?
2. 장비 SW 개발자가 HW·시스템제어팀과 협업하는 방식이 궁금합니다.
3. 해외 지사·고객사 대응 시 SW 엔지니어의 역할이 있나요?

---

## 주의 (면접에서)

| 하지 말 것 | 이유 |
|------------|------|
| BSW·AUTOSAR 언급 | 자동차 용어, 이 회사와 무관 |
| 우주·SLR·방산 용어 과다 | 장비 SW 관점으로 일반화 |
| MFC 숙련자인 척 | C# 중심이 사실 |
| SECS/GEM 경험 있다고 | 사실 아님 |

| 강조할 것 |
|-----------|
| 장비 통합 GUI + Driver 이해 + HIL |
| 현장 2년, TRR, 실장비 연동 |
| Test Tool 자체 개발 |
| ESF-CCS 품질·검증 마인드 |
