---
title: 220301 인공지능(AI)에 한 걸음 다가가기
date: 2022-03-01 15:46:00
tags:
  - AI
  - ML
categories:
  - AI
---

<div align="center">
  <img src="/images/post_images/220301_ml_beginner.png" alt="머신러닝 비기너 이미지">
</div>

<br/>

`(2022/03/01) 작성`

이번 포스팅에서는 이전에 궁금했지만 어려운 분야라서 선뜻 다가가기 어려웠던 인공지능이라는 분야에 대해 한 번 개념적인 부분을 공부해보면서 공부한 내용을 정리해보려고 한다.
완전 입문이기 때문에 생활코딩의 머신러닝 강의를 듣고 학습한 내용을 정리해보려고 한다.

<h2><b>머신러닝(Machine Learning) ?</b></h2>

인공지능이라는 말과 함께 빠지지 않고 나오는 말이 바로 이 `머신러닝`이라는 말이다. 한국말로는 기계학습인데, 왜 기계가 학습을 하는가 생각을 해보면, 인공지능이라는 것이 인간의 판단을 기계에 위임하기 위한 기술이기 때문이다. 전염병 판단이나 자율주행 등과 같이 무언가 인간을 대신해서 의사결정을 해야되는데, 이를 위해서는 이 머신러닝, 즉 기계학습이 필요하기 때문이다.

<h2><b>문제 + 공부 = 문제 의 밸런스</b></h2>

우리의 일상에는 많은 문제들이 존재하며, 이러한 문제들을 해결하기 위해 우리는 공부(학습)를 한다. 가장 이상적인 형태가 바로 해결하려는 문제에 비해 해야되는 공부의 양이 적고, 이를 통해 문제의 양의 줄어드는 것인데, 이러한 형태는 우리의 일상에서 일반적이지 않다. 이와 반대로 문제의 크기에 비해 공부하는 양의 크기가 크고, 공부한 양에 비해 문제는 해결되지 않고 오히려 문제의 크기가 더 커지는 부작용이 발생하기도 한다.
따라서 공부의 효용적 측면에서 우선 문제의 양적 측면을 최대한 부각시켜서 상대적으로 공부해야되는 양이 작게 보이도록 함으로써 공부의 양적 부담을 줄이는 방향으로 한 번 머신러닝이라는 분야에 접근해보도록 하겠다.

<h2><b>결정 = 비교 + 선택</b></h2>

결정은 비교와 선택의 합이다. 우리의 일상에는 다양성으로 인해 무언가를 선택함에 있어 비교해야되는 항목이 엄청나며, 이로인해 우리는 무언가 결정을 하는데 있어 어려움을 겪는다. 따라서 이러한 결정을 기계에게 부여함으로써 기계가 대신 결정할 수 있도록 할 수 있다. 여기서 오해가 있을 수 있는데, 망원경이 있다고 해서 눈이 필요없는 것이 아니고, 포크레인이 있다고 해서 손이 필요없는 것이 아니듯, ML이 있다고 해서 우리의 두뇌가 필요없는 것이 아니다. 우리의 두뇌가 더 나은 가치 판단 능력으로 확장시키기 위해 ML이 필요한 것이다.

<h2><b>소비자가 아닌 생산자의 입장에서 머신러닝 바라보기</b></h2>

이전에는 불가능하다고 했던 것들이 요즘 머신러닝을 통해 가능해지고 있다. 이러한 편안함을 느끼고 사용하는 단순 소비자에 그치지 않고, 우리의 일상에 잠재되어있는 각종 불편한 것들을 어떻게 해결할지 항상 궁리하는 습관을 가지고 해결하고자 노력하는 생산자의 입장에서 앞으로 머신러닝과 관련된 개념과 기술들을 학습해보도록 하겠다.

`(2022/03/06) 작성`

<h2><b>우선 스마트 폰의 사용자가 되어보고, 차후에 필요한 지식을 쌓아나가자.</b></h2>

머신러닝 이라는 분야를 공부하기 위해서는 `원리 + 수학 + 코딩` 이 세 가지 부분은 필수적으로 알아야 한다. 하지만 우리가 스마트폰을 처음 사용했을 때 스마트 폰의 원리에 대해서 전부 이해한 상태였는가? 아니다. 우리는 우선 사용자적 관점에서 스마트폰을 사용해보고 좀 더 심도있게 스마트 폰을 사용해보고자 개인적으로 원리나 코딩을 공부해본다.
요즘 수학을 몰라도 머신러닝 서비스를 사용해서 개발할 수 있도록 나온 `Teachable machine` [https://teachablemachine.withgoogle.com/](https://teachablemachine.withgoogle.com/)이라는 서비스가 있다. 이 서비스를 이용하면 이미지, 오디오, 포즈 등의 데이터를 컴퓨터에 학습시킬 수 있다.

예를들어 A 또는 B라는 포즈의 사진을 학습시키기 위해서는 학습력을 높이기 위해 여러개의 사진을 학습시켜야 한다.
각 각의 Class 사진들이 입력이 되었다면, Training 시켜주면 되고, Training 결과 판단력의 결과로 `model`이 출력된다.
좋은 model일수록 좋은 추측 결과를 도출하며, model을 만드는 과정이 학습의 과정이다.

`(2022/03/07) 작성`

<h2><b>모델(model), 머신러닝(machine learning)의 중요 열쇠</b></h2>

일반적으로 사람이 먹을 수 있는 것과 먹을 수 없는 것을 판단 할 때에는 겸험에 의해 판단을 한다. 경험해보지 못한 음식이어도 유사 경험을 통해 추측 및 예측을 통해 결정을 할 수 있다.
과학에 있어서도 특정 현상이 관찰되면, 일단 해당 현상에 대해서 추측 및 가설을 세우게 되고, 검증을 위해 실험을 하게 된다. 실험을 통해 해당 가설의 진위를 가리게 된다.

여기서 무언가를 최종적으로 결정하는데 있어 판단하는데 있어 `판단력`이라는 것이 필요한데, 이 판단력을 기계에 부여하는 것이 바로 기계학습이며, 여기서 판단력은 `model`이다.
좋은 model일수록 좋은 추측과 좋은 결정이라는 결과를 도출해낼 수 있다.

`(2022/03/08) 작성`

<h2><b>머신러닝으로 문제해결하고 싶은 일상의 문제 생각해보기</b></h2>

[https://bit.ly/ml-other-plan](https://bit.ly/ml-other-plan)

자영업자

- 환경

- 불만족

- 꿈
