## 📃Project(머신러닝 학습 후 수술실패여부 예측해서 서비스 배포)
- dataset: RecurrenceOfSurgery.csv 사용
- 목표변수 : 범주형, 설명변수 : 최소 6개 
- 서비스 대상과 목표 설명, 변수 선택 이유
<br>

## 😊 Authors
- 김혜인 : 데이터 전처리, 모델학습, 서비스 배포(FastAPI)
- 김동현 : 데이터 전처리, 프론트엔드
<br>

## 📝기술스택
- PYTHON / VISUAL STUDIO CODE / POSTMAN / ANACONDA / GITHUB
<br>

## 🔬 분석 목적
- 서비스 대상 : 환자
- 목적 : '수술실패여부'에 영향을 줄 수 있는 요인들을 선정해 관계 확인 후 환자에게 설명을 해드리기 위함
- 목적변수(Target) : '수술실패여부'
- 설명변수(Features) : '고혈압여부', '성별', '신부전여부', '연령', '체중', '수술시간'
<br>

## 🌟 변수 선택 이유
|변수|변수 설명|변수타입|변수 선택 이유|
|----|---------|--------|--------------|
|수술실패여부|환자의 수술 실패 여부|범주형|환자에게 수술 실패에 영향을 미칠 수 있는 여러 요인들을 설명하고자 함|
|고혈압여부|환자의 고혈압 여부|범주형|고혈압이 있을 경우 수술실패에 영향을 미치는지 확인하고자 함|
|성별|환자의 성별|범주형|성별이 수술실패에 영향을 미치는지 확인하고자 함|
|신부전여부|환자의 신부전 여부|범주형|신부전이 있을 경우 수술실패에 영향을 미치는지 확인하고자 함|
|연령|환자의 연령|연속형|환자의 연령에 따라 수술실패여부가 달라지는지 확인하고자 함 |
|체중|환자의 체중|연속형|환자의 체중에 따라 수술실패여부가 달라지는지 확인하고자 함|
|수술시간|환자의 수술시간|연속형|수술시간에 따라 수술실패여부가 달라지는지 확인하고자 함|
<br>

## 🔎 분석 결과
- 전처리 후의 f1-score를 보면 높은 정확도로 모델이 예측을 매우 잘 수행했다고 생각할 수 있으나 1.0이라는 수치가 나온 건 의심해볼만함.
- 전처리 전의 값

|  |precision|recall|f1-score|support|
|--|---------|------|--------|-------|
|0 |0.94|1.00|0.97|516|
|1 |1.00|0.03|0.05|36|

- 전처리 후의 값

|  |precision|recall|f1-score|support|
|--|---------|------|--------|-------|
|0 |0.99|1.00|1.00|131|
|1 |1.00|0.99|1.00|169|
<br>

## ⭐️머신러닝 서비스
- html 화면
![image](https://github.com/dancingKimDH/toy_machinelearning/assets/132973368/7f5ac0ae-fe88-4c49-97f3-1e2fa3498ce2)

- 값 입력 후 결과 출력
<br>

## 💜느낀점
- 김동현 : 머신러닝의 과정을 처음부터 끝까지 경험해 볼 수 있는 좋은 기회였습니다. 특히 전처리 전후로 결과값이 크게 바뀌는 것을 보면서 전처리 과정의 중요성을 되짚어 볼 수 있었습니다.
- 김혜인 : 모델이 더 나은 예측을 하기 위해서 데이터의 처리가 얼마나 중요한지 알 수 있었고, 결손값 처리에 대해 조금 더 공부를 할 수 있는 시간이었습니다. 결손값이 있을 경우 그냥 삭제하면 편하겠지만 데이터 손실이 발생하게 되고 결손값 자체에도 의미있는 정보가 포함될 수 있으므로 결손값을 삭제하는 대신 대체하는 것이 모델 성능 향상에 도움이 될 수 있음을 배웠습니다.
