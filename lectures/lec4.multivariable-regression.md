# Lecture 4: Multivariable linear regression

- linear regression 에는 다음 세 가지 요소가 필요함
   * 가설(Hypothesis): H(x) = W * x + b
   * 손실함수(Cost function): Cost(W, b) = 1/m * sum(H(x) - y)**2
   * 경사하강법(Gradient Descent Algorithm): W := W - alpha * dL/dW
- multivariable linear regression 이란, W 하나가 아니라 여러 개인 linear regression을 말함
- H(x) = w1*x1 + w2*x2 + ... + wn*xn + b
- 그리고 위 식을 행렬(matrix)로 확장하면 아래와 같이 쓸 수 있ㅇ므
- H(x) = XW, 실제 코드에서도 위와 같이 표현하여 clean한 코딩이 가능해짐