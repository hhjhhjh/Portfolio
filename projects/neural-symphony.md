# Neural Symphony: 딥러닝 기반 클래식 음악 생성

> 클래식 피아노 MIDI를 이벤트 언어로 변환하고 LSTM과 Transformer로 새로운 연주를 생성한 팀 프로젝트입니다.

- 형태: 서울대학교 빅데이터 핀테크 AI 고급 전문가 과정 팀 프로젝트
- 담당 범위: Beethoven 파트, miniGPT 기반 Decoder-only Transformer 모델 코드 구현, LSTM 비교 실험과 생성 결과 제작
- 기술: Python, PyTorch, LSTM, Self-Attention, miniGPT, Decoder-only Transformer, MIDI, Temperature Sampling
- 원본 저장소: [Classical_Music_DeepLearning](https://github.com/SNU-Bigdata-Fintech-AI/Classical_Music_DeepLearning)

## 문제와 목표

음악 생성 모델은 음높이뿐 아니라 음의 시작과 끝, 시간 간격, 세기를 함께 표현해야 리듬과 화음을 보존할 수 있습니다. 또한 짧은 선율을 학습하는 능력과 긴 곡의 구조를 학습하는 능력이 모델마다 어떻게 다른지 비교할 필요가 있었습니다.

## 직접 기여

### Beethoven miniGPT 모델 구현

Beethoven 곡을 담당해 이벤트 기반 MIDI 시퀀스를 학습하는 miniGPT 기반 Decoder-only Transformer 모델 코드를 직접 구현했습니다. LSTM 기준선과 동일한 작곡가 데이터에서 비교할 수 있도록 학습·생성 흐름을 정리하고 두 모델을 실험했습니다.

### 생성 결과 제작

학습한 모델을 사용해 LSTM 생성곡 4개와 Transformer 장기 생성곡 2개를 MIDI로 제작하고 팀 결과물에 포함했습니다.

## 핵심 기술 결정

아래는 팀 전체가 사용한 접근이며, 제 직접 담당 범위는 Beethoven 파트의 miniGPT 기반 Transformer 모델 코드 구현, LSTM 비교 실험과 생성 결과 제작입니다.

- 음높이만으로는 리듬·셈여림·화음을 표현하기 어려워 `TIME_SHIFT`, `VELOCITY`, `NOTE_ON`, `NOTE_OFF` 이벤트로 MIDI를 토큰화했습니다.
- 순환 구조와 Attention 기반 구조의 시퀀스 학습 특성을 비교하기 위해 LSTM, LSTM과 Self-Attention의 결합, Decoder-only Transformer를 실험했습니다.
- Greedy decoding의 반복적인 출력을 줄이고 다양성을 조절하기 위해 Temperature, Top-k, Top-p와 반복 방지 전략을 적용했습니다.
- NLL과 Perplexity만으로는 음악성을 판단하기 어려워 음고 분포 유사도와 53명의 청취 평가를 함께 사용했습니다.

## 결과와 검증

팀은 일곱 작곡가를 대상으로 생성 실험을 수행하고 33개 MIDI와 청취 평가용 11개 MP3를 제작했습니다. 작곡가와 평가 관점에 따라 LSTM과 Transformer의 우위가 달랐으며, 모델 구조뿐 아니라 이벤트 토큰화와 샘플링 전략이 생성 품질에 큰 영향을 준다는 결론을 얻었습니다.

## 제약과 개선 방향

- pitch-class 분포만으로는 리듬, 화성 진행, 프레이즈와 전체 형식을 충분히 평가할 수 없습니다.
- 정량 지표가 좋아도 실제 청취 만족도가 높다고 단정할 수 없어 사람 평가와 함께 해석해야 합니다.
- 후속 실험에서는 이벤트 표현과 디코딩 전략을 분리한 실험을 통해 각 요소가 장기 구조와 청취 품질에 미치는 영향을 검증할 필요가 있습니다.

## 관련 자료

- [Beethoven miniGPT 실험 노트북](https://github.com/SNU-Bigdata-Fintech-AI/Classical_Music_DeepLearning/blob/main/model/transformer/transformer_beethoven.ipynb)
- [생성 결과](https://github.com/SNU-Bigdata-Fintech-AI/Classical_Music_DeepLearning/tree/main/outputs)

[포트폴리오로 돌아가기](../README.md)
