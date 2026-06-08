# AI_Web_Service_Portfolio

Flask 기반 메인 웹 UI를 중심으로 ML, Vision, LLM, VLM 기능을 REST API 방식으로 확장한 통합 AI 웹 서비스 포트폴리오입니다.

## Project Overview

이 프로젝트는 교육 과정에서 진행한 AI 프로젝트들을 하나의 웹 서비스 구조로 통합한 포트폴리오입니다.

초기에는 OTT 이탈 예측 ML 모델을 Flask 웹 서비스로 구현했고, 이후 자전거 헬멧 탐지 Vision API, 교통사고 상담 RoadSafe LLM API, 교통사고 영상 기반 법률·과실 쟁점 리포트 생성을 목표로 하는 RoadSafe VLM 모듈로 확장했습니다.

## Modules

### 1. Web Main / ML

* OTT 구독 이탈 위험 예측
* Flask 기반 메인 웹 UI
* ML 모델 결과를 웹 화면에서 확인
* 이후 Vision, LLM 기능을 REST API 방식으로 연결하는 포털 역할

### 2. YOLO Vision

* 자전거 라이더 헬멧 착용 여부 탐지
* YOLO 기반 객체 탐지 모델 사용
* Flask 메인 웹과 REST API 방식으로 연동
* 교통안전 도메인 확장의 시작점

### 3. RoadSafe LLM

* 도로교통 사고 상담 및 법률·과실 쟁점 리포트 생성
* Llama 3.2 3B 기반 QLoRA fine-tuning 실험
* 사고 유형, 사고 상황, 법률·과실 쟁점, 보험사 질문, 추가 자료, 행동 체크리스트 구조로 답변 생성
* 출력 포맷 개선 및 semantic guardrail 적용

### 4. RoadSafe VLM

* 교통사고 영상 기반 법률·과실 쟁점 리포트 생성 시스템 예정
* 블랙박스 또는 사고 현장 이미지에서 대표 프레임 추출
* VLM으로 시각 정보 분석
* RoadSafe LLM/RAG와 연결하여 사고 쟁점 리포트 생성 목표

## Repository Structure

```text
AI_Web_Service_Portfolio/
├── ML_Project/
├── web_main/
├── yolo_vision/
├── roadsafe_llm/
├── roadsafe_vlm/
├── docs/
├── assets/
├── README.md
└── requirements.txt
```

## Tech Stack

* Python
* Flask / FastAPI
* REST API
* Scikit-learn
* YOLO / Ultralytics
* PyTorch
* Hugging Face Transformers
* QLoRA / LoRA
* Llama 3.2 3B
* OpenCV

## Key Points

* 단일 Flask 웹 UI에서 여러 AI 기능을 API 방식으로 통합
* ML, Vision, LLM, VLM으로 확장되는 단계형 프로젝트 구조
* 단순 모델 실험이 아니라 웹 서비스 형태로 연결
* 교통안전 도메인을 중심으로 Vision → LLM → VLM 확장
* 작은 LLM의 한계를 보완하기 위해 출력 포맷 개선과 semantic guardrail 적용

## Status

* ML Web Service: Completed
* YOLO Vision API: Completed
* RoadSafe LLM API: In Progress / Improving
* RoadSafe VLM: Planned
