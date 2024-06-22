# wine-classification-ML-model

Dacon에서 주최하는 교육목적 경진대회인
와인 품질 분류 경진대회의 데이터를 활용
> https://dacon.io/competitions/open/235610/overview/description

주어진 데이터 파일(train.csv, test.csv파일)에서 
랜덤포레스트 모델을 사용하여 와인의 Type이 red인지 white인지 예측하는 프로젝트

## 기술 스택

- **라이브러리**: numpy, pandas, matplotlib, seaborn, scikit-learn, pickle
- **플랫폼**: jupyter notebook

## 종속변수

- 클래스 개수: 2개 (White wine: 0, Red wine: 1)
- 목표변수명: ```type_init```

## 독립변수 (Feature) 12개

- fixed acidity: 산도
- volatile acidity: 휘발성산
- citric acid: 시트르산
- residual sugar: 잔당(발효 후 남은 당분)
- chlorides: 염화물
- free sulfur dioxide: 독립 이산화황
- total sulfur dioxide: 총 이산화황
- density: 밀도
- pH: 수소이온농도
- sulphates: 황산염
- alcohol: 알코올

## EDA (탐색적 데이터 분석)

데이터의 특성과 구조를 이해하기 위해 다양한 기법을 사용하는 초기 분석 단계

데이터의 분포, 이상치, 패턴 및 변수 간의 관계를 파악함

기술 통계(평균, 표 준편차 등)와 데이터 시각화(히스토그램, 박스 플롯 등)를 활용

바이올린 플롯, 히스토그램, 박스 플롯으로 통계량을 시각화함

<img src="https://github.com/shimyounseob/wine-classification-ML-model/assets/97441805/9535bf3a-2522-4a92-a68b-9eafed6cd10f" width="600">

## 변수간 상관관계

점 이항 상관관계(Point-Biserial Correlation) 

하나는 연속형 변수이고 다른 하나는 이진형 변수인 두 변수 간의 관계를 측정하는 상관계수

값의 범위는 -1에서 1까지이며, 1에 가까울수록 강한 양의 상관관계, -1에 가까울수록 강한 음의 상관관계를 가짐

<img src="https://github.com/shimyounseob/wine-classification-ML-model/assets/97441805/3097dbf0-821e-4e59-bf83-9a5cffa2e121" width="600">

## 머신러닝 모델

랜덤포레스트 모델 (Random Forest Model)

다수의 결정 트리를 생성하고 이들의 예측을 종합하여 최종 예측 진행함

과적합을 줄이고 높은 정확도를 가짐

## 모델 정확도 결과

<img src="https://github.com/shimyounseob/wine-classification-ML-model/assets/97441805/7221ba3c-9ca8-4206-bfb8-4273f8d12ac5" width="600">

- Accuracy: 전체 중에서 맞춘 비율
- Precision: 맞다고 예측한 것 중에서 실제로 맞은 비율
- Recall: 실제 맞은 것 중에서 예측도 맞은 비율
- F1-score: Precision과 Recall의 평균

<img src="https://github.com/shimyounseob/wine-classification-ML-model/assets/97441805/7bf554ee-9546-4395-a8a3-285f90b0d2e3" width="400">

## 변수 중요도
<img src="https://github.com/shimyounseob/wine-classification-ML-model/assets/97441805/b75092cd-8bdb-486e-8943-6fecaa650e1a" width="600">
