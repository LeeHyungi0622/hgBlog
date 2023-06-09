---
title: 210309 TDD study for React
date: 2021-03-09 17:18:00
tags:
  - React-testing-library
  - Unit-testing
  - Jest
  - TDD
categories:
  - React-Test
---

![](/images/post_images/tdd_co-work_img.png)

요 몇일동안 아니 저번달도 몇 일정도 이 TDD라는 녀석에 대해서 검색도 해보고, 영상도 보고 나름 이것저것 시행착오를 겪어가며 공부를 하였다.

처음에는 요즘 트렌드라고 하니깐, 그리고 완벽하게는 아니지만, 개발 도중에 발생하는 대다수의 버그를 잡아낼 수도 있다는 이야기를 듣고 무작정 해보려고 테스트 코드 작성법부터 찾아보았다. 하지만 왠지 제대로 작성하고 있는건지 의문이 들었었다.

그래서 <ins><b>그때부터 이론적인 부분부터 실무에서 직접 적용해 본 실무자들이 올린 블로그 글, 유뷰트 관련 영상 등등 이 곳 저 곳에 흩어져 있는 알짜배기 내용들을 읽고 정리하고 연습하기를 반복하였다.</b></ins>

가장 도움이 되었던 블로그 글은 `네이버 기술 블로그`에 프론트엔드 개발자 분이 올려주신 TDD관련 내용이었다. 그 분의 글을 보면서 실무에서는 어떤 방식으로 테스트 코드를 작성하고 어떤 테스트가 좋은 테스트인지에 대해서도 자세하게 알 수 있었다. 너무 내용이 좋아서 노트 필기를 하며 읽어 보았는데, 나중에 한 번 더 보고 싶을 때 참고할 수 있게 아래에 필기내용을 첨부하였다.

  <!-- more -->

그 결과 처음과 비교했을때, 이 TDD라는 개발 방법론과 조금은 친해진 것 같다. 그래서 이번에 진행하려고 하는 프론트엔드 사이드 프로젝트에 한 번 적용해보려고 한다.

아래에서 정리한 내용 중에서 가장 좋았던 내용은 `실용적인 프론트엔드 테스트를 위한 전략`에 관한 내용과 테스트 도구에 관한 내용 그리고 테스트를 `시각적 요소의 테스트`와 `외부 요소(입력, 서버 통신)으로 인한 상태 변화에 대한 테스트` 이 두 가지로 분류하여 설명해주신 부분 그리고 이전에 들었었지만 스냅샷 테스트의 정의와 한계점에 대해서 설명해주신 부분이 너무나도 유익했다.

이전 TDD관련 포스팅에서 React에서 단위 테스트를 할때 고려해야 할 요소에 대해서 잠깐 언급한 적이 있는데, 세 번째 노트 필기에는 고려해야 할 요소들 중에 하나인 `Testing event handlers`에 대해 테스트 코드를 손으로 작성해보았다.

jest에서 제공해주는 mock function(jest.fn())과 react-testing-library에서 제공해주는 fireEvent를 사용해서 테스트 코드를 작성해보았는데 두 번째 보게 되는 부분이라 처음보다 많이 익숙해진 것 같다.

좀 더 효율적인 테스트 코드 작성을 연습해서, 효율적인 테스트 코드를 작성하지 않으면 오히려 불편함을 느끼는 개발자가 되도록 노력을 해야겠다.

<table>
  <tr>
    <td>
      <img src="/images/post_images/210309_react-test.png" alt="노트필기 첫번째 사진">
    </td>
    <td>
      <img src="/images/post_images/210309_react-test1.png" alt="노트필기 두번째 사진">
    </td>
  </tr>
  <tr>
    <td>
      <img src="/images/post_images/210309_react-test2.png" alt="노트필기 세번째 사진">
    </td>
    <td>
    </td>
  </tr>
</table>
