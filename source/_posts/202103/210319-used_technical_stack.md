---
title: 210319 기술 스택의 선택과 이유
date: 2021-03-19 15:39:00
tags:
  - React-Framework
  - self-development
categories:
  - To-Be-Good-Front-end-Developer
---

<div align="center">
  <img src="/images/post_images/210426_tech_stack.jpeg" alt="다양한 기술스택"/>
</div>

## <ins><b>왜 굳이 이 라이브러리 이 프레임워크를 사용했나요?</b></ins>

사이드 프로젝트를 하기로 결심했다면 각자 어떤 라이브러리를 사용할지 또는 어떤 프레임워크를 사용할지 결정했을 것이다. 그런데 만약에 그 프로젝트가 완성이 되었다고 가정하고, 누군가 그 프로젝트에 대해서 구체적으로 왜 그 라이브러리(혹은 프레임워크)를 사용했나요? 라고 묻는다면 뭐라고 대답할지 생각해본 적이 있는가?
나 역시도 이전에는 그냥 요즘 많이 언급되고 실무에서 많이 쓰인다는 이유로 학습을 한 경우가 많았다. 물론 뭔가가 이전에 이미 존재했던 것들에 비해 나은 점이 있으니 각광을 받고 있는 것이다.

하지만 지금 이 시점 이후에 하려는 사이드 프로젝트는 사용하려는 기술에 대해 제대로 이해하고 누군가가 물어봐도 확실하게 대답할 수 있을 정도로 알고 있다는 전제하에 시작하려고 한다.

  <!-- more -->

## <ins><b>사용하려는 기술의 선택과 이유</b></ins>

간단하게 어떻게 기술스택을 선택하고 선택한 이유에 대해서 어떻게 설명해야되는지 적어보겠다.

- **React를 사용한 이유?**
  요즘에는 사용자들이 3~4초 정도 페이지 로딩이 지연되어도 해당 웹 어플리케이션을 이용하지 않는다고 합니다. 이처럼 React는 사용자가 빠른 interaction을 필요로 하기 때문에 선택을 하게 되었습니다.
  react의 사용은 사용자로 하여금 웹 어플리케이션이 아니라 마치 모바일 앱을 사용하는 것과 같은 사용자 경험을 주기 위해 사용합니다.

- **React를 사용함으로써 생기는 문제**
  React는 CSR 방식으로 초기 로딩시에 모든 페이지에 대한 정보를 내려받습니다. 그리고 각 화면에 필요한 데이터가 있는 경우, 백엔드 서버에 데이터를 요청해서 동적으로 DOM을 구성해서 Re-rendering을 하게 됩니다.
  첫 번째, 작은 규모의 어플리케이션의 경우에는 문제가 안되지만 규모가 큰 어플리케이션의 경우에는 초기 로딩시에 모든 페이지에 대한 정보를 내려받는 것이 큰 부담이 됩니다.
  두 번째, 검색엔진이 초기에 보여지는 페이지가 로딩페이지인 경우 아직 미완성의 페이지로 인식하고 낮은 순위로 검색결과에 노출시키게 됩니다. 하지만 구글 검색엔진의 경우에는 자바스크립트까지 크롤링을 하기 때문에 검색엔진 최적화에 따른 검색결과 노출이 가능합니다.

- **위에서 언급한 문제에 대해서 해결책을 알고 있는지?**
  우선 첫 번째로 말씀드린 문제의 경우에는 `code splitting`으로 해결할 수 있습니다. 초기 로딩시에 모든 페이지에 대한 정보를 내려받게 되면 초기 로딩에 대한 시간 지연으로 이어질 수 있기 때문에, 페이지 방문시에 필요한 파일들만 분리해서 내려받음으로써 해결할 수 있습니다.
  두 번째로 말씀드린 SEO(검색엔진 최적화) 문제의 경우에는 기존의 SPA이 채택하고 있는 CSR 방식을 SSR방식으로 변경해서 구현함으로써 해결할 수 있습니다.

- **그럼 본 프로젝트에서 위의 문제들을 해결하기 위해 어떻게 구현을 했나요?**
  저는 NextJS라는 React 프레임워크를 사용해서 프로젝트를 만들었습니다. 물론 React 자체로도 프레임워크를 사용하지 않고도 SSR을 구현할 수도 있지만, 좀 더 쉽게 구현할 수 있도록 도와주는 NextJS라는 프레임워크를 사용하기로 했습니다.

- **그럼 프로젝트의 모든 페이지를 NextJS 프레임워크를 적용해서 구현했나요?**
  아닙니다. 각 페이지를 구현할때 해당 페이지가 `code splitting`이나 `server side rendering`이 필요한 페이지인지 우선 생각을 한 뒤에 필요하다고 판단된 페이지에만 NextJS 프레임워크를 적용했습니다.
  만약에 관리자 페이지(admin page)의 경우에는 검색엔진의 노출을 위한 SEO가 불필요하기 때문에 SSR방식이 불필요하고, 속도도 빠르게 할 필요성(code splitting)이 없다고 생각되어 단순하게 React로만 구현을 하였습니다. 만약에 개발하려는 어플리케이션이 BtoC 서비스인 경우 관리자 페이지도 NextJS를 사용해서 구현할 것을 고민할 필요는 있을 것 같습니다.

- **`code splitting`과 `Server Side Rendering`의 효과에 대해서 구체적으로 설명해주세요.**
  Code splitting은 일괄적으로 코드를 내려받는 방식이 아닌 각 페이지별로 필요한 코드들을 분리시켜서 초기 로딩시에 일괄적으로 코드들을 내려받지 않고, 각 페이지 전이시에 필요한 코드들만 내려받게 함으로써 초기 로딩 속도를 높일 수 있습니다.
  SSR의 경우에는 SEO(검색엔진 최적화)와 밀접한 관련이 있습니다. 구글 검색 엔진의 경우에는 자바스크립트까지 크롤링하기 때문에 문제없지만, 일반적인 검색엔진의 경우에는 초기에 빈 페이지만을 로딩하는 SPA의 특성상 초기 HTML페이지에 아무것도 없기 때문에 미완성 페이지로 인식하고, 검색 노출 순위를 낮게 책정하게 됩니다. 이러한 문제는 CSR방식이 아닌 SSR방식으로 구현함으로써 해결할 수 있습니다.

  실무에서는 대부분의 서비스가 검색엔진에서의 노출과 빠른 응답속도를 요구하기 때문에 code splitting은 필수입니다.

- **NextJS의 특징에 대해서 설명해보세요.**
  NextJS는 `첫 로딩, 페이지 새로고침, 검색엔진으로부터 접속, 직접 주소를 쳐서 웹 페이지 접속`할때에는 SSR방식(browser - front - back - DB - back - front - browser 순)으로 페이지를 렌더링하게 됩니다. (Caching 기능으로 인해 새로고침된 페이지의 경우 빠르게 표시됩니다)
  또한 `Pre-fetching 기능`을 제공하기 때문에 로드될 페이지에 다른 페이지로 이동하는 링크가 존재하는 경우에는 링크들에 해당하는 코드들을 미리 내려받습니다. 따라서 이렇게 미리 내려받은 코드와 관련된 페이지로 이동시에는 back-end에서 데이터만 받아오게 됩니다. (CSR)

  - 메인 페이지에 있는 메뉴를 클릭해서 해당 메뉴의 세부 페이지를 로딩하는 경우, 데이터만 비어있는 skeleton frame이 보이다가 잠시후에 데이터가 채워져서 보이는 경우가 `CSR의 예시`이다.
  - 아무런 지연없이 HTML과 데이터가 완전히 결합된 상태로 빠르게 페이지에 표시되는 경우가 `SSR의 예시`이다.

위와같이 어떤 기술을 선택해서 사이드 프로젝트를 할때에는 구체적으로 왜 해당 기술스택을 사용했는지 구체적인 이유와 설명을 정리해보고 말로 설명해보는 연습이 필요하다. 그래야 나중에 실무에서 일을 할때에도 왜 내가 해당 기술 스택을 가지고 개발을 해야 되는지에 대한 깊은 이해를 통해 프로젝트에 사용된 기술 스택의 특징을 잘 살려서 견고한 어플리케이션을 개발할 수 있을 것이다.
