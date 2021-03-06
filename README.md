# KoBERT_with_NAVER
- BERT는 Google에서 개발한 사전 훈련 언어모델으로, 자연어처리 전반적인 분야에 아주 좋은 성능을 보여주는 모델이다. 여기서 기존 BERT의 한국어 성능 한계를 극복하기 위해 SKT Brain에서 구축한 모델인 KoBERT를 활용해 한국어 문장에 대해 좋은 성능을 보여주고자 하였다. 해당 repository에서는 KoBERT에 NAVER에서 제공하는 영화 리뷰 데이터셋을 적용하여 한국어문장 감정분석을 수행하고 이를 다른 자연어처리 모델과 비교하여 실험 결과를 보인다.

## 코드 수행 과정
- 데이터의 전처리를 위해 온점(.)이나 ?와 같은 각종 특수문자를 한글만 남기고 제거하기 위해서 정규 표현식을 사용한다.
- KoBERT Tokenizer를 통해 문장을 Token화 하였고, 한국어 문장으로 pretrain되어있는 BERT Classification model으로 감정분석을 시행하여 감정분석의 결과인 긍/부정 감정이 상대적인 확률로 나타나도록 하였다.

## 주요 실험 결과
- accuracy

|Epoch|BERT(multi)|BERT(Ko)|
|------|---|---|
|1|0.8466|0.8827|
|2|0.8599|0.8910|
|3|0.8613|0.8933|
|4|0.8618|0.8920|
|5|0.8618|0.8948|

- 실제 데이터 적용 (킹스맨: 퍼스트 에이전트)

![1](https://user-images.githubusercontent.com/80094752/172822500-6c5ce706-7ec2-4592-aeb7-c43f1784226a.png)


![2](https://user-images.githubusercontent.com/80094752/172822740-ef674110-703c-43fa-b779-4bca3d428574.png)
