# Lecture 5: Logistic Regression

## 5-1 Logistic Regression
- Binary Classification 문제(스팸 메일 여부, 피드 show 여부 등)는 선형 회귀에 적합하지 않음.
  * cost를 최적화 시키기 어렵고
  * 매우 큰 x가 학습 데이터에 있으면, x=100,000,000에 대해서도 y=1로 예측해야 해서 기울기가 매우 작아지고, 이에 따라 경계의 데이터에 대해 잘 예측하지 못하게 됨
- 이러한 문제를 해결하기 위한 함수로 logistic 또는 sigmoid 함수가 있음. S(x) = 1/(1+e^(-x))
- 로지스틱 회귀는 가설을 H(x) = 1/(1+e^-(Wx+b))로 하는 모델임

## 5-2 How to minimize cost of Logistic Regression
- 선형 회귀의 Cost(W, b) = 1/m Σ (H(x) - y)^2 의 경우, convex function 으로 미분한 기울기를 작게하는 방향으로 파라미터를 업데이트하면 최적의 해에 도달할 수 있음
- 그러나 로지스틱 회귀의 Cost를 선형 회귀의 cost와 같게 하면, convex 형태가 아니라 구불구불한 형태가 되어 미분 값이 0인 포인트가 매우 많아짐 (local minima) 그래서 global minimum인 최적의 해에 도달하기 어려움
- 따라서 다른 cost function을 사용해야 함. Cost(W, b) = -logy(H(x)) - log(1-y)(1-H(x))
- 위 cost는 cross entropy loss 인데, y가 1일 때는 -log(H(x)) 항만 관여하고, y=0일 때에는 -log(1-H(x))항만 관여함. 그리고 이 cost function은 다시 convex 형태가 되어 GD를 적용하여 최적의 해에 도달할 수 있게 됨.