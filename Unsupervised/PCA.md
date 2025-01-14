# Principal Component Analysis, PCA
- 고차원 데이터를 저차원으로 변환하는 데 사용되는 통계적 기법이다.
- PCA 는 데이터의 분산을 최대한 보존하면서 변수의 수를 줄여 데이터의 차원을 축소하는 방법이다.
- 이를 통해 데이터의 구조를 이해하고, 노이즈를 줄이며, 계산 효율성을 높일 수 있다.

### 1-1. 주성분 분석의 주요 개념
#### 고차원 데이터
- 원래의 데이터는 여러 개의 변수(특성)로 구성되어 있을 수 있다.
- 이로 인해 데이터가 고차원 공간에 위치하게 된다.
#### 분산의 최대화
- PCA 의 목표는 데이터의 분산이 최대화되는 방향을 찾는 것이다.
- 데이터의 분산이 크다는 것은 데이터가 그 방향으로 많이 퍼져있다는 것을 의미하며,
  이 방향을 **주성분**이라 한다.
#### 주성분
- PCA 는 주성분 분석을 통해 데이터의 차원을 축소한다.
- 첫 번째 주성분은 데이터의 최대 분산 방향을 나타내며,두 번째로 큰 분산을 나타낸다.
- 이 과정을 반복하여 n차원 데이터에서 n개의 주성분을 얻을 수 있다.
#### 차원 축소
- 고차원 데이터를 주성분으로 변환하여 저차원 데이터로 압축한다.
- 이 과정에서 데이터의 주요 정보를 보존하면서 불필요한 정보를 제거할 수 있다.

### 1-2. PCA 의 주요 단계 
#### 데이터 표준화
- PCA 를 적용하기 전에 데이터의 평균을 0으로, 표준편차를 1로 조정하는 표준화를 수행한다.
- 이는 변수 간의 스케일 차이를 줄여준다.
#### 공분산 행렬 계산
- 데이터의 각 변수 간의 관계를 파악하기 위해 공분산 행렬을 계산한다.
- 공분산 행렬은 각 변수의 분산과 두 변수 간의 공분산을 나타낸다.
#### 고유값 및 고유 벡터 계산
- 공분산 행렬의 고유값과 고유벡터를 계산한다.
- 고유값은 각 주성분의 중요도를 나타내며, 고유 벡터는 주성분의 방향을 나타낸다.
#### 주성분 선택
- 고유값이 큰 순서대로 주성분을 선택한다.
- 일반적으로 전체 분산의 일정비율(예: 95%)을 설명하는 주성분 수를 선택한다.
#### 데이터 변환
- 선택된 주성분을 사용하여 원본 데이터를 새로운 저차원 공간으로 변환한다.
  
### 1-3. PCA 의 장단점
#### 장점
- 차원 축소: 고차원 데이터를 저차원으로 축소하여 시각화, 분석, 모델링에 용이하게 만든다.
- 노이즈 감소: 데이터의 주요 구조를 유지하면서 불필요한 변동성을 제거하여 노이즈를 줄인다.
- 계산 효율성 향상: 차원 축소를 통해 알고리즘의 학습 및 예측 속도를 개선한다.
- 정보 시각화: 저차원으로 변환된 데이터를 사용하여 데이터의 분포 및 패턴을 쉽게 시각화할 수 있다.
#### 단점
- 선형성 가정: PCA 는 데이터의 선형 구조를 가정하므로 비선형 데이터에는 한계가 있다.
- 해석의 어려움: 주성분 분석은 원래 변수의 선형 조합이기 때문에 해석하기 어려울 수 있다.
- 정보 손실: 차원 축소 과정에서 일부 정보가 손실될 수 있다.

### 1-4. PCA 활용 예
- 이미지 처리: 이미지 데이터의 차원을 줄여서 컴퓨터 비전에서의 처리 속도를 높인다.
- 데이터 시각화: 2D 또는 3D 로 데이터의 구조를 시각화하여 패턴을 파악한다.
- 특성 선택: 머신러닝 모델의 입력 변수(특성)를 줄여서 모델의 성능 및 해석 가능성을 높인다.
