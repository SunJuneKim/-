# 학습 로드맵 (42dot 지원용)

## Phase 0: 지금 ~ 2주 (기반 정리)

| 항목 | 목표 | 산출물 |
|------|------|--------|
| 질문지 답변 | `questionnaire/` 완료 | 정량 성과·기술 스택 확정 |
| 경력기술서 1차 | PDF 2페이지 | `resume/career-summary-draft.md` |
| C++ 복습 | 포인터, STL, move, thread | LeetCode Easy/Medium 주 10문제 |
| 영문 elevator pitch | 2분 | `resume/elevator-pitch-en.md` (추가 예정) |

---

## Phase 1: 3~6주 (ROS2 + 포트폴리오)

### ROS2 미니 프로젝트 (필수)

**프로젝트명 제안**: `multi_camera_sync_sim` 또는 `sensor_hub_ros2`

| 구성 | 설명 |
|------|------|
| Node 1 | Camera/sensor mock publisher (3채널) |
| Node 2 | Time sync coordinator (NTP/GPS 개념 시뮬) |
| Node 3 | Image preprocess (OpenCV: AGC, ROI) |
| Node 4 | Status monitor + rosbag record |

**목적**: 42dot JD의 ROS2, camera, Linux, real-time 키워드 직접 대응  
**공개 GitHub**: 이력서에 링크 (방산 코드 X, 개념만)

### 학습 리소스
- [ROS2 Humble Docs](https://docs.ros.org/en/humble/)
- Robotics ROS2 Basics (Udemy/YouTube)
- 본인 우주물체 경험 → `sensor_msgs`, `tf2`, `message_filters` SyncPolicy 매핑

---

## Phase 2: 4~8주 (도메인 + 면접)

### 자동차/AD 도메인
| 주제 | 시간 | 리소스 |
|------|------|--------|
| ADAS/AD 개요 | 4h | 42dot KCCV/UMOS 영상 (채용 페이지 참고) |
| E2E vs 모듈형 AD | 2h | Atria AI 기사 |
| ISO 26262 개요 | 4h | functional safety 입문 |
| 좌표계 (vehicle/camera/world) | 4h | ROS tf2 + 본인 마운트/별보정 경험 연결 |

### 코딩테스트
- **SW Engineer AD**: 포함 가능성 높음
- 주 3회, 90분 타이머
- 유형: 배열/해시, BFS/DFS, 그리디, 기본 DP
- 플랫폼: programmers, LeetCode

### 시스템 설계 (면접)
- 분산 센서 데이터 파이프라인 설계
- "카메라 3대 동기화 시스템 설계" — 본인 경험 기반 15분 발표 준비

---

## Phase 3: 지원 직전 (1~2주)

- [ ] 이력서 PDF (30MB↓, 민감정보 제거)
- [ ] 포트폴리오 README 영문
- [ ] 지원 포지션 URL 스크린샷 보관
- [ ] 코딩테스트 모의 2회
- [ ] 기술 면접 영어 스크립트 암기

---

## 영어 학습 (병행)

| 주차 | focus |
|------|-------|
| 1-2 | 프로젝트 3개 영문 설명 각 200 words |
| 3-4 | ROS2/AD 용어 카드 50개 |
| 5-6 | mock interview (녹음) |
| 7-8 | 이력서·LinkedIn 영문 최종 |

**토익/토플**: 회사 요구 아님. 시간 있으면 **Speaking/Writing** 위주.

---

## 일일/주간 루틴 제안 (재직 중)

```
평일 1h:  ROS2 또는 C++ (교대)
평일 30m: 영어 스크립트
주말 3h:  포트폴리오 + 코딩테스트 2문제
```

---

## 완료 체크리스트

- [ ] ROS2 demo GitHub public
- [ ] LeetCode 50문제
- [ ] 영문 이력서 1페이지
- [ ] 본 repo questionnaire 100%
- [ ] 42dot 지원 완료
