# 과제 1번 필수과제 

# Regression Analysis 과제

이 코드는 주어진 데이터셋을 사용하여 회귀 모델을 학습하고 평가하는 과정을 담고 있습니다. 단계별로 데이터 탐색, 전처리, 모델 학습 및 성능 평가를 수행합니다.

## 주요 단계

### 1. 데이터 로드 및 탐색
- 데이터셋을 로드하고 구조를 확인합니다.
- 결측치 및 데이터의 기본 정보를 출력합니다.

### 2. 데이터 전처리
- 결측치를 평균값으로 채워서 처리합니다.
- 박스플롯을 활용해 이상치를 탐지하고 제거합니다.

### 3. 모델 학습 및 평가
- 세 가지 회귀 모델을 사용합니다:
  - 선형 회귀 (Linear Regression)
  - 의사결정 나무 (Decision Tree)
  - 랜덤 포레스트 (Random Forest)
- 각 모델의 성능을 평가합니다 (MAE, MSE, R²).

### 4. 성능 시각화
- 모델 성능을 막대 그래프로 시각화합니다.

### 5. 최적 모델 분석
- R² 점수가 가장 높은 모델을 선택하여, 실제 값과 예측 값을 비교합니다.

# 고객 세분화 분석 (Mall_Customers 데이터)

## 개요
이 프로젝트는 **Mall_Customers 데이터셋**을 사용하여 고객을 여러 그룹으로 세분화하는 작업을 수행합니다. 클러스터링 기법(K-Means)을 적용하여 고객의 소득과 소비 점수를 기준으로 그룹화하였습니다. 이를 통해 고객 행동 패턴을 이해하고, 마케팅 전략에 활용할 수 있는 인사이트를 도출합니다.

## 주요 작업 단계

### 1. 데이터 로드 및 탐색
- **데이터셋:** Mall_Customers.csv
- 주요 열:
  - `Annual Income (k$)` (연간 소득)
  - `Spending Score (1-100)` (소비 점수)
- 데이터 구조와 결측치를 확인하여 분석 준비 완료.

### 2. 데이터 전처리
- **필요한 열 선택**: 고객의 연간 소득과 소비 점수.
- **스케일링**: StandardScaler를 사용해 데이터를 표준화하여 클러스터링에 적합하게 변환.

### 3. 클러스터링 수행
- **K-Means 클러스터링**:
  - 클러스터 수(k)를 2부터 10까지 테스트.
  - 엘보우 방법과 실루엣 점수를 통해 최적의 클러스터 수 결정.
  - 최적의 k=5로 설정.

### 4. 클러스터링 결과 시각화
- **산점도**:
  - 고객 데이터를 시각화하여 클러스터링 결과를 확인.
  - x축: 연간 소득, y축: 소비 점수.
  - 각 클러스터를 색상으로 구분.

### 5. 결과 저장
- **저장 파일**: 클러스터링 결과를 `Mall_Customers_Clustered.csv`로 저장.

## 실행 환경
- **필요한 라이브러리**:
  - pandas
  - matplotlib
  - seaborn
  - scikit-learn

## 실행 방법
1. `Mall_Customers.csv` 파일이 실행 환경에 있어야 합니다.
2. Python 스크립트를 실행하면 클러스터링과 시각화가 수행됩니다.
3. 결과는 `Mall_Customers_Clustered.csv`로 저장됩니다.

## 시각화 예시
- 엘보우 방법 그래프
- 실루엣 점수 그래프
- 클러스터링 결과 산점도

## 분석 결과
- **k=5** 클러스터:
  - 소비 점수와 소득을 기준으로 고객을 5개의 그룹으로 분류.
  - 그룹별 특성을 바탕으로 고객 행동 패턴 분석 가능.





