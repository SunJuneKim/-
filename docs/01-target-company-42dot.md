# 타겟 기업 분석: 포티투닷 (42dot)

## 기업 개요

| 항목 | 내용 |
|------|------|
| **정식명** | (주)포티투닷 / 42dot |
| **소속** | 현대자동차그룹 글로벌 소프트웨어 센터 |
| **미션** | SDV(Software-Defined Vehicle) · 모빌리티 AI |
| **핵심 기술** | Atria AI (E2E 자율주행), Gleo AI (LLM) |
| **근무지** | 경기 성남시 수정구 (판교) |
| **채용 페이지** | https://42dot.ai/careers/openroles |

2026년 1월 기준, Atria AI 고도화를 위해 자율주행 분야 경력 개발자 **50여 명** 규모 채용 진행 중.

---

## 채용 전형 (일반)

```
서류전형 → 코딩테스트 → 화상면접(1h) → 대면/화상면접(3h) → 최종합격
```

- 직무별로 절차·코딩테스트 유무 상이
- 이력서: **PDF 30MB 이하**, 주민번호·사진·연봉 등 법정 금지정보 제외
- 문제 시: `recruit@42dot.ai` + 지원 포지션 URL

---

## 지원 가능 직무 매트릭스 (본인 경력 기준)

| 직무 | 적합도 | 이유 |
|------|--------|------|
| **Software Engineer (Autonomous Driving)** | ★★★★☆ | C/C++, Linux, Yocto, 임베디드, 카메라·센서, 현장 통합 — **가장 현실적** |
| **Software Engineer (AD Framework)** | ★★★★☆ | 미들웨어·호환 레이어(HDLC), TCP/IP, 분산 시스템 경험 부합 |
| **Test Engineer (Autonomous Driving)** | ★★★☆☆ | 검증·현장 운영 강점. 다만 개발 역량 대비 포지셔닝이 약해질 수 있음 |
| **Vehicle System Integration Engineer** | ★★★☆☆ | 시스템 통합·다수 구성품 제어. ASPICE/ISO26262 경험 보강 필요 |
| **Senior IVI OS Engineer (Camera System)** | ★★☆☆☆ | 카메라 경험은 있으나 IVI/Android 스택과 거리 있음 |
| **Senior Computer Vision Engineer** | ★☆☆☆☆ | ML/CV 이론·석사+, CUDA, SLAM 논문급 — **현 단계 비추천** |
| **ML Platform / AI Engineer** | ★☆☆☆☆ | 딥러닝·MLOps 중심 — 경력 방향과 불일치 |

---

## 1순위: Software Engineer (Autonomous Driving)

**공고 요약** (Remember / 42dot 채용 페이지 기준)

### 주요 업무
- 자율주행 관련 사용자 경험 기능 구현
- 차량 상태 확인 및 안전 경험 제공
- 차량 내 SW 통합 및 품질 개선
- 임베디드 가속기 포함 SW 프로파일링·최적화

### 자격 요건
- 학사 이상 (CS/EE/로봇 등)
- **능숙한 C/C++**
- **임베디드 시스템**, 프로파일·최적화
- **ROS/ROS2**, Python/Bash 자동화
- **Linux, Yocto**

### 우대
- Rust, 차량용 애플리케이션 Hands-on
- OpenCL/CUDA/SIMD, HW 가속 AI 코드
- 자발적 문제 해결·크로스펑셔널 소통

### 본인과의 매칭 포인트
| 요건 | 본인 경력 |
|------|-----------|
| C/C++ | Linux C (드라이버), C# 운영제어, Python 테스트 |
| 임베디드 | Yocto, 디바이스 드라이버, FPGA 통신카드 호환 |
| Linux | 드라이버·SBC·통신 스택 |
| 카메라/센서 | MWIR/CCD/EMCCD, GPS/NTP, 다채널 RS422/HDLC |
| 시스템 통합 | 6~7개 구성품, 4PC 아키텍처, PostgreSQL |
| 현장 검증 | 3년 거창 현장, ns급 동기화 튜닝 |

### 보강 필요
- **ROS/ROS2** (필수급 — 가장 큰 갭)
- 자동차 도메인 용어 (ADAS, E2E, HIL 등)
- 코딩테스트 (알고리즘)

---

## 2순위: Software Engineer (AD Framework)

### 핵심 업무
- 자율주행 **미들웨어** (실시간 통신, 실행 프레임워크)
- Linux/RTOS 이기종 분산 시스템
- DDS, TCP/IP, SOME/IP, DoIP 등 프로토콜
- 추상화 레이어·호환성 (→ HDLC 카드 프로젝트와 직결)

### 자격 요건
- C/C++, ROS/ROS2 또는 동급 미들웨어
- 3년+ automotive/robotics (Senior는 10년+)
- Yocto, CMake, CI/CD

### 본인과의 매칭
- 상용 드라이버(tdrv009/002) → 자체 FPGA 카드 **호환 레이어** 개발 경험이 AD Framework의 "abstraction layer" 스토리와 동일 구조
- 다채널 실시간 통신 (8ch RS422/HDLC)
- 레지스터 맵 분석·기능 대조·유저 앱 무수정 호환

---

## 지원 전략 (방향)

### 포지셔닝 한 줄
> **"실시간 센서·영상·제어를 통합해 현장까지 끌고 간 시스템 엔지니어"**
> — 방산/항공 우주에서 검증된 통합 역량을 SDV·자율주행 플랫폼으로 확장

### 이력서에 강조할 키워드 (42dot JD 대응)
- Real-time distributed system
- Multi-sensor / multi-camera integration
- Linux embedded (driver, Yocto)
- Middleware compatibility layer
- Field deployment & system validation
- Timing synchronization (NTP/GPS, ns-level awareness)

### 피해야 할 포지셔닝
- "OpenCV로 영상 처리한 개발자"만 강조 → CV Research Engineer와 혼동, ML 갭 노출
- "C# WinForms GUI 개발자"만 강조 → 임베디드/AD와 괴리
- 방산 프로젝트 **세부 군사 정보** 과다 기재 → 보안·채용 리스크

### 지원 시기
- 공고는 **상시 채용** — ROS2 보강(4~8주) 후 지원이 유리
- 2026 Atria AI 50명 채용 진행 중 → **상반기 지원 권장**

---

## 참고 링크

- [전체 채용 공고](https://42dot.ai/careers/openroles)
- [Software Engineer (Autonomous Driving) - Remember](https://career.rememberapp.co.kr/job/posting/281100)
- [현대차그룹 뉴스: 42dot AD 채용](https://www.hyundaimotorgroup.com/ko/news/42-dot-autonomous-driving-developer-recruitment)
