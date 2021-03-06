# React Quickly

## 프로젝트 개요

React의 이해도를 높이고 동작과정을 깊게 학습하고자 '리액트 교과서'의 내용을 재구성한 프로젝트 입니다.

- [Intro](#intro)
- [Chapter1](#chapter1)
  - React란 무엇인가?
  - React가 해결할 수 있는 문제
  - React의 장점
  - React의 단점
  - 웹 애플리케이션에 React 적용하기

## Intro

React는 템플릿을 제거하고 자바스크립트 사용자 인터페이스를 컴포넌트 기반으로 설계했습니다..
가상DOM을 이용한 빠른 속도와 활발한 사용자 커뮤니티를 가장 큰 장점으로 꼽을 수 있습니다.

React는 불필요한 것을 모두 걷어내었습니다.

## Chapter1

옛날 방식은 관심사 분리에 초점이 맞춰져 있었는데 이 말은 CSS, HTML, JAVASCRIPT를 각각 스타일, 데이터 추상화, 동적 인터렉션으로 구분하는 방식입니다.
React는 강력한 UI라이브러리로 기존의 방식과 달리 컴포넌트를 재사용할 수 있습니다.

### React란 무엇인가?

React는 UI컴포넌트 라이브러리입니다. 특별한 템플릿 언어가 아닌 자바스크립트를 이용해서 만들며 여러 컴포넌트로 UI를 구성하는 방식은 React의 핵심 철학입니다.
React UI컴포넌트는 매우 독립적이며 특정 관심사에 집중된 **기능 블록** 입니다.

물론 컴포넌트 기반 아키텍처(Component-based architecture, CBA)는 React이전에도 존재했습니다.

### React가 해결할 수 있는 문제

기존의 웹 개발은 복잡한 웹 UI로 구성되어 개발, 관리하는 데 어려움을 겪었습니다.

이러한 문제를 해결하는 과정에서 메모리에서 DOM요소를 생성하는 것은 빠르지만, 실제 DOM으로 렌더링하는 과정에서 병목이 발생한다는 점을 인지했고, 이러한 문제를 해결하기 위한 알고리즘을 만들어 냈습니다.
그 덕분에 React의 속도는 높아졌고, 성능 이슈도 해결할 수 있었습니다. React의 성공 요인으로는 이러한 성능과 개발자 친화적이고 컴포넌트를 기반으로 한 구조라고 할 수 있습니다.

### React의 장점

- 간결성
  간결성을 위해 React가 선택한 방법은 소프트웨어 엔지니어의 웹 개발 경험을 극적으로 개선했습니다. React를 간결하게 만드는 기능으로는 다음과 같습니다.

**선언형 스타일 채택**
React는 뷰를 자동으로 갱신하는 선언형 스타일을 채택합니다. 개발자가 UI요소를 선언형 스타일로 작성한 후 뷰에 변경이 발생하는 경우 React가 알아서 갱신합니다. 또한 뷰를 갱신해야 할 때가 바로 선언형 스타일이 빛을 발하는 순간으로 이것을 **내부 상태**변화라고 합니다.
React는 상태 변경에 따라 뷰를 갱신합니다.

React는 내부적으로 가상DOM을 사용하여 브라우저에 이미 반영된 뷰와 새로운 뷰의 차이점을 찾아내는데 이 과정을 **DOM비교** 또는 **상태와 뷰의 보정**이라고 부릅니다.

**순수한 자바스크립트를 이용한 컴포넌트 기반 아키텍처**
React는 컴포넌트에 자바스크립트만 사용할 뿐 템플릿 엔진 같은 도메인 특정 언어(DSL)을 사용하지 않습니다.

템플릿의 문제점 중 하나는 개발자가 다른 언어를 배워야 한다는 점인데 React는 순수한 자바스크립트이므로 새로운 언어를 배워야하는 비용이 들지 않습니다.

**강력한 추상화**
React는 DOM을 쉽게 다룰 수 있고, 같은 기능이지만 크로스 브라우징을 위해 다르게 구현할 수밖에 없었던 인터페이스나 이벤트 핸들링을 정규화했습니다. React는 강력한 문서 모델 추상화를 제공합니다.
내부의 인터페이스는 숨기고, 대신에 정규화 과정을 거친 합성 메서드와 속성을 제공합니다.

React는 터치 이벤트에 대해서도 합성 이벤트를 제공하므로 모바일 기기를 대응한 웹, 앱을 만들 때 매우 유용합니다.

React의 우수한 DOM추상화를 증명하는 또 다른 예는 SSR입니다. SSR은 검색 엔진 최적화(SEO)와 성능 개선에도 유용합니다.

- 속도와 테스트 용이성
  프레임워크에서 불필요한 갱신을 일으키는 경우가 있는데 이런게 발생하면 성능이 저하될 수 있습니다. React의 가상 DOM은 자바스크립트 메모리에만 존재하기에 데이털르 변경하면 React는 가상 DOM을 먼저 비교하고,
  렌더링 변경이 필요한 경우에만 실제 DOM에 렌더링합니다.
  React는 꼭 필요한 부분만 갱신하여 내부 상태(가상DOM)와 뷰(실제DOM)를 같게 만듭니다.

- 폭 넓은 개발 커뮤니티와 생태계
  말 그대로 폭 넓은 커뮤니티로 많은 오픈 소스가 제공되어 있습니다.

### React의 단점

- React는 모든 기능을 갖춘 프레임워크는 아니기에 Redux나 React Router 같은 라이브러리를 함께 사용해야합니다..
- 단방향 데이터 바인딩만 제공하여 양방향 바인딩에 익숙한 개발자에겐 불편할 수 있습니다.

### 웹 애플리케이션에 React 적용하기

React를 UI 일부에만 적용할 수 있습니다..

React로 프론트엔드를 개발하기 위해 특정 백엔드를 사용할 필요는없습니다. 다른 언어로 백엔드를 개발한 경우에도 React를 사용할 수 있습니다.
React는 UI라이브러리일 뿐이므로 어떤 형태의 백엔드나 프론트엔드 데이터 관리 라이브러리와 함께 사용할 수 있습니다.

- UI 라이브러리로 React와 관련된 Redux나 React Router를 활용한 단일 페이지 애플리케이션 스택의 구성
- MVC의 V를 대체하는 UI라이브러리로 기존 MVC 프레임워크와의 결합
- jQuery를 기반으로 서버 측 렌더링을 거친 애플리케이션에서 자동완성 등 일부 기능을 위한 UI컴포넌트로 활용
- 대부분의 로직을 직접 처리하는 전통적인 방식의 백엔드에서 서버 측 렌더링 템플릿 라이브러리로 활용
- 백엔드와 프론트엔드에서 모두 자바스크립트를 사용하는 경우
- React Native를 UI라이브러리로 사용한 모바일 앱
- 여러 가지 렌더링 대상에 적용할 목적으로 사용하는 UI라이브러리

**React 라이브러리와 렌더링 대상**
React는 거의 항상 JSX와 함께 사용됩니다. JSX는 React UI 개발을 편리하게 해주는 간단한 언어로 Babel 같은 도구를 사용해서 JSX를 자바스크립트로 변환합니다.

**단인 페이지 애플리케이션과 React**
단일 페이지 애플리케이션 아키텍처는 서버보다는 클라이언트, 즉 브라우저 측에 로직이 더 많은 팻 클라이언트입니다. SPA는 HTML렌더링, 입력값 검증, UI변경 등의 기능을 브라우저에서 해결합니다.

렌더링 과정

1. 사용자가 새로운 페이지를 열기 위해 브라우저에 URL을 입력
2. 브라우저가 URL요청을 서버로 전송
3. 서버는 응답으로 HTML, CSS, 자바스크립트 파일 같은 정적 자원을 보냄
4. 자바스크립트 로드 후 추가로 AJAX나 XHR 요청을 보내 서버에서 데이터를 불러옴
5. 데이터는 JSON, XML등의 포맷으로 전닯다음
6. SPA에 데이터가 전달되면 사용자 인터페이스를 구성하는 HTML을 렌더링, SPA는 템플릿에 전달받은 데이터를 밀어넣고 브라우저상에서 UI를 렌더링
7. 브라우저 렌더링이 끝나면 SPA는 사용 가능한 상태가 됨
8. 사용자가 웹 페이지를 볼 수 있음

SPA 방식은 UI렌더링을 대부분 브라우저 상에서 해결합니다. 모든 렌더링을 서버에서 해결하는 전통적인 방식과 달리 SPA에서는 데이터만 주고 받습니다.
