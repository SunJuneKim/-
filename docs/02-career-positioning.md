# 직무 결정 및 커리어 포지셔닝

## 결론: 추천 직무

### 지원 직무명 (한글/영문)

**1순위: Software Engineer (Autonomous Driving)**  
**2순위(병행 검토): Software Engineer (AD Framework)**

### 이력서에 쓸 직함 (Headline)

```
실시간 영상·센서 통합 시스템 엔지니어
(Embedded / Vision / System Integration)
```

또는 영문 병기:

```
Real-time Vision & Embedded Systems Engineer
7+ years | Multi-sensor integration | Linux/Driver | Field deployment
```

---

## 왜 이 직무인가

### 본인 경력의 본질
단일 스택 개발자가 아니라 **"장비가 실제로 돌아가게 만드는 엔지니어"**입니다.

| 레이어 | 경험 |
|--------|------|
| HW/FW | 펌웨어, 자이로 등 센서 시험 |
| Driver/OS | Linux 디바이스 드라이버, Yocto, SCC 리맵 |
| Middleware | 상용↔자체 통신카드 호환 레이어 |
| Application | 운영제어부, 영상 acquisition/display |
| Integration | 7구성품+3카메라, 4PC, NTP/GPS 동기화 |
| Validation | 3년 현장(구현·연동·관측 병행), 50 arcsec급 기여 |

이 스택은 42dot **Software Engineer (AD)** 또는 **AD Framework**가 요구하는  
"차량 내 분산 SW + 센서 + 실시간 + 현장 검증"과 구조적으로 같습니다.

### Computer Vision Engineer를 1순위로 안 하는 이유
- 42dot CV Engineer: **CV/ML 이론, 석사+, SLAM/3D, CUDA** 중심
- 본인 강점: **영상 파이프라인 구현·카메라 SDK·보정·전시** (응용/시스템)
- 지원 시 ML 딥다이브 면접에서 불리 → **AD SW Engineer가 합격 확률 높음**

### Test Engineer를 2순위로만 두는 이유
- 현장 검증·시나리오 경험은 강점
- 다만 7년차 개발 역량(드라이버, 통합, 영상)을 테스트 직무에 쓰면 **연봉·성장 천장**이 낮아질 수 있음
- "개발 + 검증 모두 가능"은 면접 어필 포인트로만 사용

---

## 경력 서사 (스토리라인)

### 3단계 성장 서사 (이력서·자기소개용)

**1단계 — HW/FW 기반 (초기)**  
펌웨어·하드웨어 접점에서 장비 동작 원리 습득

**2단계 — 시스템 확장 (중기)**  
Linux/Driver, 운영제어, 영상, DB, 다수 구성품 통합  
→ **NSLR(차세대 SLR)** 3년 — 운영제어부 **단독**, 거창 현장에서 **구현·연동·관측** 병행

**3단계 — 플랫폼·호환성 (현재)**  
호환 레이어 → **드라이버 로직 modify**, HDLC/RS422 8ch, 저궤도 1인 개발  
→ **추상화·드라이버** 역량으로 심화 중

### 차별화 메시지

> 많은 개발자는 라이브러리·샘플 코드 수준에서 끝납니다.  
> 저는 **coefficient 의미, calibration 모델, 구성품 인터페이스 제약**을 이해하고  
> 현장 tuning으로 **50 arcsec 이하** 정밀도에 기여했습니다.

> ns급 동기화가 필요한 시스템에서 **네트워크 기반 timing이 정밀도에 미치는 영향**을 체감했고,  
> 구조 변경이 불가한 상황에서는 **jitter 최소화 튜닝·보정**으로 운영 안정성을 확보했습니다.

---

## 프로젝트별 이력서 비중 (42dot 지원용)

| 프로젝트 | 이력서 비중 | 강조 축 |
|----------|-------------|---------|
| NSLR (차세대 SLR) | **40%** | 단독 운영제어·동기화·별보정·현장 개발 |
| XMC HDLC 통신카드 | **30%** | 호환레이어 단독 → 드라이버 modify |
| 저궤도 우주물체 | **20%** | WPF·Cesium·운영제어 확장 |
| 지능형 조준경 | **5%** | Yocto 부팅·영상전시 (보류 명시) |
| 기타 시험 프로그램 | **5%** | 센서 R&D 범용성 |

---

## 자기소개서 핵심 테마 (42dot 맞춤)

1. **Physical AI / Atria AI** — 카메라 기반 실시간 인지의 **시스템 구현** 경험 (알고리즘 연구가 아닌 **플랫폼·데이터 파이프라인**)
2. **SDV** — Software-Defined 관점에서 운영제어부 4PC·7구성품 = **분산 차량 SW**와 유사
3. **One Team** — 한화시스템 2년 현장 협업 = OEM-Tier1 협업 구조와 유사
4. **끝까지 운영** — 설치·유지보수·새벽까지 현장 = **production mindset**
