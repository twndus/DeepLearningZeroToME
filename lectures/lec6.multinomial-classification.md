# Lecture 6: Multinomial Classification

* binary가 아니라 3개 이상의 클래스 중 어떤 것인지를 예측하는 문제
* 더 이상 시그모이드 또는 로지스틱 함수만으로는 문제를 해결할 수 없음
* 전체 결과의 합이 1이 되도록 각 클래스에 대한 예측 결과를 비율로 나타내는 소프트맥스(softmax) 함수를 사용하면 해결 가능
* 소프트맥스의 결과에 대해서 cross entropy(logistic cost와 같고, 약간 확장된) cost를 사용하여 파라미터를 업데이트할 수 있음
* Cross Entropy 손실은 정답과 유사한 형태일수록 낮은 패널티를, 그렇지 않을수록 높은 패널티를 부과하여 학습이 수행됨