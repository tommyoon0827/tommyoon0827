## 김윤지 (Yoon)

LLM과 비전 모델을 실제 서비스에서 쓸 수 있게 만드는 AI 엔지니어를 목표로 하고 있습니다.
학부 연구생으로 LangChain 기반 의료 AI 에이전트와 RAG 챗봇을 만들었고,
인턴으로 일하면서는 운영 중인 CCTV 관제 시스템에 비전 모델과 VLM 판독을 붙이고 학습 데이터 파이프라인을 만들었습니다.
주로 Python으로 작업하고, 학습 점수보다 실제 데이터에서 얼마나 맞는지를 먼저 재 보는 편입니다.

📂 [포트폴리오](https://github.com/tommyoon0827/portfolio) · 📝 [velog](https://velog.io/@rosyoon/posts)

---

### 주요 프로젝트

**LLM · RAG · 에이전트**

| 프로젝트 | 무엇을 | 결과 |
|---|---|---|
| [소아과 사전 문진 AI 에이전트](https://github.com/tommyoon0827/portfolio/tree/main/pediatric-previsit-agent) · [코드](https://github.com/tommyoon0827/Pediatric_previsit_ai_agent) | LangChain + GPT-4o-mini 문진 에이전트 메인 개발. 답변마다 LLM이 진료 시 주의가 필요한지 판단, 보호자 눈높이로 답하는 RAG(ChromaDB) 육아 상담 챗봇, 의료진용 요약과 PDF 리포트 | 실제 소아청소년과 문진 자료 기반, 한국어·영어 두 버전 |
| 지자체 분리배출 안내 RAG 챗봇 | 데이터 담당. 지역별 배출 기준을 ChromaDB에 인덱싱하고, 이미지 분류(EfficientNet-b0)와 LLM을 잇는 멀티모달 구조 설계 | 춘천시 생성형 AI 아이디어 경진대회 동상 (43개 팀) |
| VLM 2차 판독 | 운영 CCTV의 1차 탐지 결과를 VLM으로 다시 확인해 오탐 필터링 | 사무실 오탐 218건 전부 제거, 심각도 4단계 자동 부여 |

**ML · 비전 · 데이터**

| 프로젝트 | 무엇을 | 결과 |
|---|---|---|
| [행동 분류](https://github.com/tommyoon0827/portfolio/tree/main/walk-stand-classification) | 사람의 걷기/서기를 프레임 간 이동량으로 판정 | 균형 정확도 75.5% (기저 50%), 추가 연산 없음 |
| [화분·야구방망이 탐지](https://github.com/tommyoon0827/portfolio/tree/main/potbat-detection) | 공개 데이터가 없는 2클래스 경량 탐지 모델 (YOLO12n) | 미탐률 44% → 14%, 범용 탐지 성능 손실 없음 |
| [라벨링 도구](https://github.com/tommyoon0827/portfolio/tree/main/cctv-labeling-tool) | 영상→프레임→YOLO 데이터셋 자동화 + 검수 모드 | 행동 분류·화분 탐지 두 모델의 학습·검수 데이터를 생산 |
| [학습 데이터 수집](https://github.com/tommyoon0827/portfolio/tree/main/training-dataset-collection) | 모델 배포 플랫폼에 재학습 데이터 수집·자동 검사·검수·릴리스 기능 추가 | YARA 규칙 작동률 0.2% → 93.9%, 정상 파일 26,768개에서 오탐 0건 |
| [쓰레기 분류·재활용 가이드 앱](https://github.com/tommyoon0827/portfolio/tree/main/waste-classification-app) · [코드](https://github.com/tommyoon0827/CapstoneDesign) | 4인 팀 데이터 담당. 공개 데이터 재분류, 중복 제거, 전처리로 15종 분류 데이터셋 구축 | 한림대 캡스톤 디자인 경진대회 동상 |

CCTV 쪽 모델(행동 분류, 화분 탐지, VLM 판독)은 기존 흉기 탐지를 건드리지 않는 게 조건이었습니다.
확장 슬롯과 읽기 전용 경로만 써서 붙였고, 문제가 생겨도 기존 탐지는 계속 돌아가게 격리했습니다.

**그 밖에**

**CCTV 관제 시스템 재작성** (2026.07~08) · [화면·설계 보기 →](https://github.com/tommyoon0827/portfolio/tree/main/cctv-control-system)

위 모델들이 올라가는 기존 PHP 관제 시스템을 대체하려고, 화면부터 서버까지 Vue 3 + Go로 새로 만들었습니다.
화면 41개·API 115개를 혼자 개발했고, 실제 서버에 설치해 사무실 CCTV로 동작을 확인했습니다.

---

### 경력

| 기간 | 소속 | 역할 |
|---|---|---|
| 2026.07 ~ present | 시큐어시스템즈 | AI Vision Engineer (인턴) — 운영 CCTV 관제 시스템에 행동 분류·객체 탐지·VLM 재판독 투입, 평가 하네스와 학습 데이터 파이프라인 구축 |
| 2025.10 ~ 2026.03 | DASH Lab | 학부 연구생 · AI Agent Developer — 소아과 문진 지원 에이전트 개발 주도, 응급 추천 시스템 모델 설계 |
| 2025.03 ~ 2025.08 | APC Lab | 학부 연구생 · Deep Learning Researcher — 화학정보학 기반 딥러닝 모델 연구, LLM 챗봇 개발 |
| 2025.01 ~ 2025.02 | Claion | AI Developer Intern — 최신 AI 트렌드 분석 및 비즈니스 모델 적용 프로세스 연구 |
| 2024.07 ~ 2024.08 | ZIOVISION | 데이터 라벨링 인턴 — 비전 모델 학습 데이터 정제·수집 |

---

### 수상 & 활동

- 춘천시 생성형 AI 아이디어 경진대회 동상 — 춘천시 (2025.07) · 지자체 분리배출 안내 RAG 챗봇 개발
- 교양 교과목 개발 공모전 총장상(우수상) — 한림대학교 (2025.11) · 프롬프트 엔지니어링 방법론 교양 설계
- 한림대학교 캡스톤 디자인 경진대회 동상 — 한림대학교 (2025.03~06) · 쓰레기 분류·재활용 가이드 앱 개발
- Solverton New York (Impact Track) — 미국 뉴욕 해외연수 (2026.01~02) · CUNY 현지 검증 인터뷰 기반 글로벌 커리어 플랫폼 PoC 개발
- 학사경고자 멘토링 프로그램 우수 멘토 — 한림대학교 (2025.03~06) · 1:1 학습 전략 지도로 멘티 성적 약 2.0점 상승

---

### 스택

**LLM** `LangChain` `OpenAI API (GPT-4o-mini)` `RAG · ChromaDB` `Prompt Engineering` `Streamlit`  
**ML · Vision** `PyTorch` `Ultralytics YOLO` `EfficientNet` `OpenCV`  
**Language · Data** `Python` `R` `Pydantic` `Data Pipeline · QC`  
**그 밖에** `TypeScript` `Vue 3` `Go` `PostgreSQL`
