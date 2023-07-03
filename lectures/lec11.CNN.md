# Lecture 11: CNN

## CNN 개요
- 이미지 관련 task에 탁월한 성능을 보이는 모델
- 사람이 이미지를 인식할 때에 전체 이미지를 부분으로 나누어 인식하는데, 이 방식을 모방한 딥러닝 구조

## layers
- Convolution layer
    - 정사각형 크기의 입력 데이터라고 가정할 때,
    - (input_shape[0] - filter_size[0]) / step_size + 1 번의 연산을 수행함
    - Convolution filter는 입력층에 대해서 공유되는 파라미터이며, 이 필터는 local features를 추출하는 역할을 함
- Pooling layer는 샘플링의 역할을 하며, mean, max 등의 방식으로 주로 사용됨
- FC layer (fully-connected)는 앞에서 추출한 특징들로 task를 수행하기 위한 연산을 하는 층. 일반적인 feed-forward 신경망

## The history of CNN architecture
1. LeNet
   * 5개의 층으로 구성된 간단한 모델 구조
2. AlexNet
   * 2012년도 ImageNet에서 우숭
   * 96개의 필터를 사용
   * normalization layer 사용
   * FC layers 4096 -> 4096 -> 1000 (classes)
3. GoogLeNet
   * 2014년도 발표. 6.7% 의 에러율
   * 병렬적으로 구성된 inception module을 사용
4. Resnet
   * 2015년, 3.6%의 에러율, He. et al
   * 이미지넷 뿐만 아니라 다른 대회까지 휩쓸었음
   * 주요 특징은 152개의 층을 사용했다는 점. 층이 깊어지면 학습이 잘 안되기 마련인데, Residual connection으로 이를 해소
   * Residual connection은 l1, l2의 출력을 l3의 입력으로 하는 방식.
   * 알파고도 CNN 기반의 모델
