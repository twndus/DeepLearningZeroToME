# Lecture 2: Linear regression

요약
- regression은 ML의 가장 기본적인 아이디어
- 데이터에 대해 H(x) = Wx + b를 따를 것으로 가정
- 가정과 실제 데이터 포인트의 차이를 계산하는 함수를 cost function이라 함
- cost function은 단순한 차이보다는 주로 제곱을 취해 부호의 영향을 없애고, 손실이 클수록 더 큰 패널티를 받게 함
- cost fucntion은 Cost(W, b) = 1/m SUM ((Wb+x)-x)^2으로 W, b에 관한 식이 되며, LR은 이를 최소화하는 것을 목표로 함
