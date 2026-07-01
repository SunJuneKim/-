# 면접 · 코딩테스트 준비

## 예상 전형 (Software Engineer AD)

```
서류 → 코딩테스트 → 화상(1h) → 대면/화상(3h) → 최종
```

---

## 코딩테스트 대비

### 출제 유형 (추정)
- 배열/문자열, 해시맵
- BFS/DFS (그리드, 그래프)
- 정렬/이진탐색
- 구현 (시뮬레이션)
- DP (기초)

### C++ vs Python
- JD는 C/C++ — **C++17로 풀기 연습** 권장
- 시간 부족 시 Python 허용 여부는 전형 안내 확인

### 추천 문제 (예시)
| 난이도 | 유형 | 비고 |
|--------|------|------|
| Easy | Two Sum, Valid Parentheses | 워밍업 |
| Medium | Number of Islands, LRU Cache | 빈출 |
| Medium | Merge Intervals | 실시간 스케줄링 연상 |

---

## 기술 면접 예상 질문

### C/C++/Linux
- multi-thread 환경에서 race condition 경험?
- device driver user/kernel space 개념
- `select` vs `epoll`
- shared memory vs socket

### "현장 = 코딩 안 함?" 반박 (필수)
> 거창 2년은 유지보수만이 아닙니다. **운영제어부 구현·7구성품 실장비 연동·관측**을 동시에 했고, 한화시스템과 협업하며 새벽 운영까지 **직접 코드 수정**했습니다.

### 본인 경력 연계 답변 준비
1. **7개 구성품 + 3카메라 동기화를 어떻게 설계했나?**
2. **NTP/GPS 동기화에서 가장 어려웠던 점?**
3. **50 arcsec 정밀도를 위해 한 구체적 조치는?**
4. **HDLC stash/split 이슈 원인과 디버깅 방법?**
5. **상용 드라이버 호환 레이어 설계 원칙?**
6. **OpenCV AGC/ROI 파이프라인 구조?**
7. **Yocto 빌드에서 겪은 이슈?**

### AD 도메인
- ROS2를 써본 적 / 없다면 배우는 중 + 포트폴리오
- Camera calibration 경험 (별보정 → pinhole/radial distortion 연결)
- Real-time system에서 latency 줄인 경험
- Functional safety 알고 있는지 (ISO 26262 개요)

### 시스템 설계
- "자율주행 차량에 카메라 6대, LiDAR 1대 — 데이터 어떻게 모을 것인가?"
  → 본인 4PC·7구성품 아키텍처 경험으로 답변

---

## 행동 면접 (STAR)

### Situation–Task–Action–Result 템플릿

**Q: 일정이 촉박한데 구조 변경이 필요해 보였던 경험?**

- S: ns급 동기화, 아키텍처 고정
- T: 정밀도 유지하며 운영 안정화
- A: jitter 측정, 타이머·보정 튜닝, 구성품별 latency 보상
- R: 50 arcsec 이하 기여 (수치 확정 필요)

**Q: 협업 업체와 갈등/이슈?**

- S: 한화시스템 2년 현장
- T: 다수 업체 인터페이스
- A: 운영제어부에서 제약 흡수, 상태 전시·로그로 재현성 확보
- R: (구체 에피소드 — 질문지에서 보강)

---

## 42dot 맞춤 질문 (역질문)

1. Atria AI E2E 스택에서 sensor platform 팀의 역할 범위는?
2. Software Engineer AD 팀의 ROS2 사용 범위와 배포 타깃 ECU는?
3. 현장 vehicle test와 bench 개발 비율은?
4. 온보딩 시 functional safety 교육이 있는지?

---

## 지양할 답변

- "ROS는 안 해봤고 배울 의지 있습니다"만 반복 → **포트폴리오 없으면 약함**
- 방산 세부 스펙·보안 등급 과다 노출
- "정밀도를 구조적으로 개선했다" (실제는 튜닝) — **솔직히 튜닝 + trade-off 설명이 더 신뢰**
