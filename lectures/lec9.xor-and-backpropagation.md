# Lecture 9 XOR problem solving and Backpropagation

## XOR problem
- XOR: exclusive or로, 베타적인 or 일 때는 1 그렇지 않을 때는 0인 논리 연산
- 퍼셉트론 하나만을 사용할 때에는 AND, OR, NOT은 모두 해결 가능하나, XOR는 해결 불가능했음. 이 때문에 AI 겨울이 오기도 함
- Minsky 에 의해, 퍼셉트론을 두 층 이상 구성하면 XOR 문제를 해결 가능함이 증명됨
- 개인적으로 XOR 문제 해결의 핵심은 첫 번째 층을 지나면서 XOR 문제를 다른 문제(AND, OR, NOT)로 바꾸는 것이라고 생각함

## Backpropagation
- XOR problem을 해결하기 위해서는 최소 2개의 층이 필요함. 이렇게 깊어진 신경망의 가중치를 업데이트할 수 없는 문제가 있음. Minsky는 이 문제를 아무도 풀 수 없다고 말함
- Paul과 Hinton에 의해 미분을 사용하면 가중치의 업데이트가 가능함이 밝혀짐. 이를 역전파라고 함.
- 역전파할 때의 각각의 미분값은 가중치가 전체 loss에 미치는 영향을 의미함. 그 영향을 learning_rate 크기만큼 업데이트하여 학습을 거듭함에 따라 loss가 줄어들도록 함.
- 이로써, AI의 큰 고비를 넘게 됨.