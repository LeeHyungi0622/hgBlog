---
title: 210309 Front-end Side Project Diary 1일차
date: 2021-03-09 16:59:42
tags:
  - Self-Development
  - React
  - Test-Scenario
  - Side-Project-Diary
categories:
  - Side-Project-Diary
hidden: true
secret: true
---

![](/images/post_images/side_project_diary_img.jpg)

## **Front-end Side Project Diary 1일차**

오늘은 본격적으로 Repository를 생성하고 header 부분의 레이아웃을 우선 설계해보았다. 확실히 HTML/CSS 수업을 듣고나서 진행하는 레이아웃 작성이라 그런지 레이아웃 구성시에 작성하는 코드에 대해서 설명이 가능한 것 같다.

header 레이아웃을 분석하던 도중에 반응형 레이아웃이라는 것을 고려한다면 어떻게 효율적으로 요소들을 배치해야 하는지 고민이 되었었다.

콘텐츠의 논리적 흐름을 최대한 유지한 상태에서 일부 요소의 배치를 이동하여 구성해야 된다는 것은 수업시간에 배워서 알고 있었는데, 막상 배치를 생각해보니 어려웠다. 더군다나 반응형 웹 페이지가 아닌 적응형 웹 디자인으로 작성된 페이지다보니 모바일과 데스크탑 웹 페이지의 헤더 부분이 많이 달라보였다.

그렇게 고민을 하던 중에 우연히 강의실을 지나가시던 데레사 강사님께 질문을 드렸다. **해답은 바로 콘텐츠의 논리적 흐름과 모바일 우선(mobile-first)방식**에 있었다. 이미 개념적으로는 머리 속에 박혀있어서 레이아웃을 설계하면서 되뇌이던 개념이었는데, 역시 아직 많은 연습이 필요한 것 같다.

  <!-- more -->

오늘 배운 가장 핵심이 되는 내용은 `만약 모바일 웹 화면의 콘텐츠 흐름과 데스크탑 웹 화면의 콘텐츠 흐름을 비교해서 설계를 하지 않으면, 먼저 설계한 쪽의 레이아웃을 기준으로 absolute positioning을 통해서 해결하는 잘못된 방식이 나온다`는 것이다.

레이아웃을 설계할 때 모바일의 레이아웃을 우선적으로 염두해두고 설계를 하되, 콘텐츠의 흐름은 두 부분 모두 고려해서 화면 배치방법을 고려해야 한다.

설계할때 작성했던 노트는 나중에 기억을 되살리기 위해서 아래에 첨부해두었다.
좌측 하단의 그림을 참고하도록 하자.

![](/images/post_images/210309_front-end-project.png)
