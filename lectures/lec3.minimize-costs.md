# Lecture 3: How to minimize cost

- 선형 회귀에서 cost는 실제 값과 모델로 구한 값의 차이를 제곱하여 구할 수 있음.
- 이 cost를 최소화하기 위한 방법으로는 Gradient Descent Algorithm이 있음.
- Gradient Descent는 경사 하강법으로, 말 그대로 경사를 따라 내려하는 알고리즘.
- 경사하강법 수식 W := W - alpha * dL/dW
- 경사는 해당 지점에서의 미분값, 즉 기울기를 의미하며 기울기가 양수이면 음의 방향으로, 음수이면 양의 방향으로 파라미터를 업데이트
- 여기서 파라미터는 H(x) = W * x + b에서 W와 b를 의미하며, W와 b에 대해서 각각 미분하여 각 파라미터를 업데이트함
- w가 여러 개 생겨도 업데이트하는 데에 지장 없음.
- alpha는 learning_rate로 한 번에 업데이트할 크기(step size)를 결정함