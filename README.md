# 황정현 | Financial AI & Data Portfolio

금융 업무를 이해하고 AI 기능을 실제 서비스와 의사결정 흐름에 연결해 온 프로젝트를 소개합니다. 사내 AI 에이전트와 공통 플랫폼, 금융 문서 RAG, 신용위험 기반 투자전략을 중심으로 의료영상·생성형 AI·공간분석 경험까지 담았습니다. 각 프로젝트에서는 제가 직접 담당한 범위와 팀 전체 결과를 구분합니다.

[GitHub Profile](https://github.com/hhjhhjh)

## 핵심 역량

- 투자운용 현장의 리스크관리, 컴플라이언스, 회의록과 데이터 적재 업무를 AI 에이전트와 자동화 파이프라인으로 구현했습니다.
- LLM의 비결정적 출력과 고정된 판단 로직을 분리하고 비동기 작업, 공통 SDK, 캐시와 장애 대응 구조를 갖춘 서비스로 발전시켰습니다.
- 신용위험 예측을 대출 승인 기준, 현금흐름, IRR과 Sharpe Ratio로 연결해 모델을 실제 투자 의사결정 관점에서 평가했습니다.
- 금융 문서의 표·본문 분리와 SQL 조회를 구현하고, 팀의 SQL·벡터 검색 결합 RAG 시스템 개발에 참여했습니다.
- 의료영상·임상정보의 멀티모달 학습과 불균형 분류, 생성형 AI와 공간분석 프로젝트로 데이터 유형과 문제 범위를 확장했습니다.

## 주요 수상

- 2026.01.22 · 서울대학교 빅데이터 핀테크 AI 고급 전문가 과정 캡스톤 우수 발표상 — 키움투자자산운용 연계 팀 프로젝트
- 2025.06.30 · 대한임베디드공학회 ICT 대학생 논문경진대회 우수논문발표상 장려상(3위) — 제1저자

## 💼 금융 AI·핀테크

### 🏦 키움투자자산운용 AI 업무지원 플랫폼

- 프로젝트: 2025년 10월 캡스톤 프로젝트로 시작해 인턴십까지 이어진 경험으로, 투자 리스크, ESG, 컴플라이언스와 문서·음성 처리 업무를 지원하는 사내 AI 서비스들을 개발했습니다.
- 직접 기여: 리스크 코멘트와 회의록 생성, 컴플라이언스 심사, 디지털마케팅 데이터 적재 파이프라인을 개발하고, 여러 서비스의 외부 API·파일 처리 기능을 공통 서비스와 SDK로 분리했습니다.
- 결과: 팀 캡스톤 프로젝트가 우수 발표상을 받은 뒤 저는 인턴 제안을 받았습니다. 인턴십에서는 리스크 코멘트 작성 시간을 수일에서 하루 이내로 단축하고, 1시간 이상 회의 녹음을 10분 이내에 전사하도록 자동화했습니다.

`Python` `FastAPI` `React` `LangGraph` `LLM/RAG` `MongoDB` `Redis` `Docker`

[상세 설명](projects/kiwoom-ai-platform.md) · 원본 저장소: 비공개 사내 저장소

### 📈 Lending Club 대출 투자 전략

- 프로젝트: 부도확률 예측을 대출 승인 임계값과 현금흐름 기반 수익률에 연결해 Sharpe Ratio를 최적화한 프로젝트입니다.
- 직접 기여: 데이터 전처리와 Random Forest·LightGBM 모델 구현 및 반복 실험을 담당했습니다.
- 결과: 팀의 별도 테스트 실험에서는 XGBoost가 약 0.116의 Sharpe Ratio를 기록했습니다.

`Python` `Random Forest` `LightGBM` `IRR` `Sharpe Ratio`

[상세 설명](projects/lending-club.md) · [원본 저장소](https://github.com/SNU-Bigdata-Fintech-AI/Lending-Club-Project)

### 📄 AuditQA: 삼성전자 감사보고서 RAG QA 시스템

- 프로젝트: 감사보고서의 정량 표는 SQL로, 정성 본문은 벡터 DB로 검색하는 금융 문서 질의응답 시스템입니다.
- 직접 기여: 파싱 파트 리더로 복잡한 감사보고서의 본문·표 구조를 보존하는 파싱 방법론을 제안하고 구현했으며, SQL 조회 실험과 프로젝트 문서화도 담당했습니다.
- 결과: 팀의 LoRA 슬롯 파서는 검증 481건에서 JSON 파싱 성공률 100%, 전체 객체 Exact Match 67.98%를 기록했습니다.

`Python` `BeautifulSoup` `MariaDB` `DuckDB` `Qdrant` `RAG`

[상세 설명](projects/auditqa.md) · [원본 저장소](https://github.com/SNU-Bigdata-Fintech-AI-11th-Team6/Samsung-Financial-Reports-NLP)

## 🧠 AI 연구·모델링

금융 AI 프로젝트에서 활용한 모델 설계·평가와 비정형 데이터 처리 역량을 다른 데이터와 문제로 확장한 경험입니다.

### 🫀 심혈관 질환 멀티모달 분류

- 프로젝트: 좌·우 안저영상과 임상정보를 함께 사용해 심혈관 질환을 예측한 개인 연구 프로젝트입니다.
- 직접 기여: 제1저자로 문제 정의, 2,903명의 환자 단위 데이터 분할, 모델 설계·실험과 논문 작성을 수행했습니다.
- 결과: 최종 모델은 정확도 83.67%, AUC 0.926, F1 0.837을 기록했고, 최고 단안 기준선 대비 정확도 8.0%p와 F1 0.084를 개선해 우수논문발표상 장려상(3위)을 받았습니다.

`Python` `PyTorch` `EfficientNetV2-S` `Multimodal Learning` `Multitask Learning`

[상세 설명](projects/multimodal-cvd.md) · [원본 저장소](https://github.com/hhjhhjh/Multimodal-CVD-Classification)

### 🎹 Neural Symphony: 클래식 음악 생성

- 프로젝트: MIDI를 이벤트 시퀀스로 표현하고 LSTM과 Transformer가 다음 이벤트를 예측하도록 학습한 생성형 딥러닝 프로젝트입니다.
- 직접 기여: Beethoven 파트를 맡아 miniGPT 기반 Decoder-only Transformer 모델 코드를 직접 구현하고, LSTM과 비교 실험해 생성 결과를 제작했습니다.
- 결과: 직접 LSTM 생성곡 4개와 Transformer 장기 생성곡 2개를 제작했으며, 팀은 총 33개 MIDI·11개 MP3와 53명 청취 평가로 모델별 생성 특성을 비교했습니다.

`Python` `PyTorch` `LSTM` `miniGPT` `Transformer` `MIDI`

[상세 설명](projects/neural-symphony.md) · [원본 저장소](https://github.com/SNU-Bigdata-Fintech-AI/Classical_Music_DeepLearning)

### 🧪 COVID-19 환자 사망위험 예측

- 프로젝트: 불균형 의료 데이터에서 모델 구조와 리샘플링, 분류 임계값이 사망위험 예측에 미치는 영향을 비교한 개인 프로젝트입니다.
- 직접 기여: 전처리부터 Logistic Regression·LightGBM 실험과 평가까지 수행했습니다.
- 결과: LightGBM의 임계값을 0.50에서 0.825로 조정해 precision을 0.3095에서 0.4882로, F1을 0.4583에서 0.5598로 개선하고 recall 감소와의 상충 관계를 확인했습니다.

`Python` `scikit-learn` `LightGBM` `Imbalanced Classification`

[상세 설명](projects/covid-19-ml.md) · [원본 저장소](https://github.com/hhjhhjh/COVID-19-Machine-Learning)

## 🛠️ AI 서비스·데이터 분석

모델과 분석 결과를 웹 서비스, 데이터 파이프라인과 실제 사용 흐름으로 연결한 프로젝트입니다.

### 🧴 피그널: 피부 트러블 위치 분석 서비스

- 프로젝트: 5인 팀으로 얼굴 이미지에서 피부 트러블을 탐지하고 얼굴 부위별 정보를 제공하는 웹 서비스를 개발했습니다.
- 직접 기여: YOLOv8 모델 학습·모델링과 추론 후처리, Flask 백엔드, DB 저장과 결과·기록 조회 기능을 담당했습니다.
- 결과: 팀은 이미지 업로드부터 분석 결과 조회까지 이어지는 프로토타입을 구현했습니다.

`Python` `YOLO` `MediaPipe` `Flask` `SQLite`

[상세 설명](projects/acne-cv.md) · [원본 저장소](https://github.com/NIS-co-create/acne-CV)

### 🔥 한국 산불 진압시간 예측

- 프로젝트: 기상·산림·화재 데이터를 결합해 산불 진압 소요시간을 예측한 프로젝트입니다.
- 직접 기여: 팀 리더로 분석 방법론을 설계하고 선형·트리 모델 코드를 모두 구현·실행했으며 결과 분석을 주도했습니다.
- 결과: 팀의 대표 실험은 원 단위 MAE 약 108분을 기록했고, 극단치와 제한된 데이터가 정밀 예측의 주요 제약임을 확인했습니다.

`Python` `pandas` `scikit-learn` `LightGBM` `XGBoost`

[상세 설명](projects/wildfire-duration.md) · [원본 저장소](https://github.com/SNU-Bigdata-Fintech-AI/KR-WIldfireData-MachineLearning)

### 🏠 안전한 자취방 구하기

- 프로젝트: 서울시 공공데이터와 부동산 매물 정보를 결합한 프로젝트입니다.
- 직접 기여: 4명의 팀원이 같은 범위로 협업했으며, 데이터 수집·전처리·분석·시각화와 안전점수 산출 전 과정에 함께 참여했습니다.
- 결과: 서울 오피스텔 3,781건에 주변 시설과 법정동 군집 결과를 결합해 매물 단위 안전점수를 산출하고 지도에 시각화했습니다.

`Python` `pandas` `K-means` `Regression` `Geospatial Analysis`

[상세 설명](projects/safe-house.md) · [원본 저장소](https://github.com/Tave-14-Aespo/safe-house)

## 포트폴리오 안내

각 상세 페이지는 팀 전체 결과와 제가 직접 담당한 범위를 구분해 설명합니다. 공개 프로젝트는 원본 저장소로 연결하며, 사내 비공개 프로젝트는 기밀정보를 제외한 역할과 구현 결과만 소개합니다.
