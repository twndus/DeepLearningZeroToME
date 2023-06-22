# Lecture 10 DL Concepts

## 10-1 ReLU
- Geoffrey Hinton의 4가지 발견 요약
  * 라벨링한 데이터가 너무 작다 (?)
  * 컴퓨터가 너무 느리다 (?)
  * 멍청한 방법으로 가중치를 초기화했다
  * 비선형 함수의 종류를 잘못 썼다
- 위 중 마지막 항목은 가중치가 소실되어 모델이 업데이트되지 않는 Gradient Vanishing 문제와 관련이 있음. 이 현상은 sigmoid의 특성 상 더 잘 발생하게 되어 있음. sigmoid는 0~1 사이의 값으로 변환하기 때문에 한 번 기울기의 크기가 작아지면, 0.001 * 0.01 * 0.00001 * ... 역전파 시 업데이트할 값이 점점 없어지게 됨
- 이러한 문제는 sigmoid 함수 대신에 ReLU를 사용하며 해결하게 됨. ReLU는 Rectified Linear Unit의 약자로, 0이하에서는 0의 값을, 0 이상에서는 identity 값을 반환하는 비선형 함수
- ReLU에 의해 예측 오차가 매우 줄게 되었고, 이에 따라 ELU, LeakyReLU 등의 다양한 비선형 함수가 등장하게 됨.

## 10-2 Weight Initialization
- 비선형 함수를 ReLU를 쓰더라도, 가중치가 잘 수렴하는지는 가중치를 어떻게 초기화하는지에 따라 달랐음. 0으로 시작하면 잘 업데이트가 안되기 때문.
- RBM (Restricted Boatman Machine)
  * KL distance
  * encoder, decoder
- Xavier and He
  * using only fan_in, fan_out
- still open..


## 10-3 Dropout, Ensemble
### Dropout
- 오버피팅을 막는 방법: more training data, less feature(optional), regularization
- 위 외에도 학습 과정에서 전체 네트워크의 일부 노드의 연결을 무작위로 끊어 특정 노드에 대한 의존도를 낮추는 기법인 Dropout도 사용할 수 있음.

### Ensemble
- 여러 개의 네트워크를 학습하고, 이 결과를 종합하여 결과로 함.
- 성능을 높이고 안정적인 결과를 내는 데에 좋음

## 10-4 DNN
- feedforward NN
- CNN
- RNN
- ... 상상력과 지식을 동원하자