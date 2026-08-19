## tommyoon0827

컴퓨터 비전 모델을 **실제로 돌아가는 시스템에 얹는 일**을 합니다.
CCTV 관제 환경에서 객체 탐지·행동 분류·VLM 재판독을 운영에 투입하고 있습니다.

### 작업 방식

모델을 만드는 것보다 **그 모델이 얼마나 잘 동작하는지 믿을 수 있게 만드는 데** 시간을 더 씁니다.

- 검증 정확도 100%가 실제로는 배경을 학습한 것이었던 경우
- mAP 0.98 모델의 라이브 재현율이 31%였던 경우 — 학습셋과 평가셋이 같은 영상이었음
- "VLM이 칼을 못 읽는다"는 진단이 틀렸고, 저장 파이프라인이 픽셀을 지우고 있었던 경우

세 번 다 점수가 좋아 보일 때 **이 점수를 믿을 근거가 있는지** 물어서 잡았습니다.
그 과정에서 만든 평가 하네스가 다음 과제의 26일을 1일로 줄였습니다.

지표도 같은 이유로 고릅니다 — 클래스가 73:27로 기울어 있으면 아무 판단도 안 하는 모델이
정확도에서 이깁니다. 균형 정확도로 읽어야 75.5% 대 50.0%가 보입니다.

### 공개된 것

| | |
|---|---|
| [Pediatric_previsit_ai_agent](https://github.com/tommyoon0827/Pediatric_previsit_ai_agent) | 소아과 사전문진 AI 에이전트 (2025.10~11) |
| [CapstoneDesign](https://github.com/tommyoon0827/CapstoneDesign) | 폐기물 분류 캡스톤 — Flutter + Django + 이미지 분류 (팀 프로젝트) |

사내에서 진행한 CCTV 비전 작업은 공개할 수 없습니다.
코드와 방법론만 정리한 저장소가 따로 있으니 필요하시면 말씀해 주세요.

### 스택

`Python` `PyTorch` `Ultralytics YOLO` `OpenCV` `Ollama` `Django` `PySide6` `MySQL` `PostgreSQL`

📮 secure0514@gmail.com
