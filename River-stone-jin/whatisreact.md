<!--React 스터디 1회차
일시 : 2017년 4월 12일
범위 : 시작 ~ 리액트의 장점-->

# React란
`React`는 페이스북에서 만든 오픈소스 프로젝트로서 자바스크립트로 UI를 구축하는 창의적인 접근법을 제공한다.

### React는 프레임워크가 아니다
헷갈리시는 분들이 있는것 같던데 React는 프레임워크가 아닌 UI 컴포넌트를 만드는 `라이브러리`다.
React를 사용해서 재사용성이 높은 UI 컴포넌트를 만들수있다.
그리고 React는 프레임워크가 아닌 라이브러리기 때문에 기존에 짜져있는 프로그램에서 부분을 조금씩 바꾸어 갈수있다.

#### 프레임워크와 라이브러리의 차이
프레임워크와 라이브러리의 차이는 프레임워크는 미리 틀이 짜져있어 그 틀에 맞춰 개발을 해야하고 라이브러리는 내가 필요한 라이브러리를 가져다 쓰면서 자유롭게 개발 할 수있다. 즉, 누가 `프로그램 제어 주도권`을 지고 있느냐에 따라서 라이브러리인지 프레임워크인지 구분 할 수 있다.

### React가 프레임워크로 만들어지지 않은 이유(?)
#### 기존 MVC의 문제점
MVC(Model View Controller)는 새로운 기능이 추가될 경우 Model과 View의 수가 커지고 데이터의 흐름이 양방향으로 이루어질수록 시스템의 복잡도가 증가하여 작은 프로그램에 적합하다.  
즉, 큰 프로젝트에서는 사용하기 힘들다

#### MVC에 대한 대안
"좀 더 예측 가능한 코드 구조화"에 대한 목표로 "단방향 데이터 플로우인 시스템 아키텍쳐" `Flux`

Flux는 Store, Dispatcher, View, Action으로 이루어져있으며 역할은 아래와 같다.
- Store : MVC에서 Model과 같은 역할을 하며 프로그램의 모든 데이터를 담고있다.
- Dispatcher : MVC에서 Controller와 같은 역할을 하며 모든 데이터를 관리하고 Action이 있을때마다 어떻게 Store를 업데이트를 해야하는지 결정한다.
- View : Store가 변경될때마다 함께 변경된다.

일단 Flux는 'MVC의 다른 이름이다' 등 논란이 많기 때문에 차후에 정리해서 다시 올리도록 하겠다.

## React 특징

#### React는 XML을 이용  
React는 컴포넌트를 만들때 UI를 설명하는데 적합한 XML을 사용한다

#### MVC에서 View의 역할만을 위해 만든 라이브러리  
기존 컴포넌트 지향 프레임워크들과는 다르게 진짜 UI만 지원하기 때문에 Angular나 Backbone 같은 프레임워크에 View로만 사용 할 수있다.

#### Virture DOM
React는 DOM Tree 구조와 같은 Virture DOM을 만들어 DOM에 변경이 생길경우 Virture DOM을 변경한 후 변경된 부분만 파악하여 실제 DOM에 반영하여 빠르게 처리할수있다.

#### 단방향 데이터 흐름
React는 단방향 데이터 흐름을 지향한다. 그래서 Angular를 사용하여 양방향 데이터 바인딩을 사용할때처럼 작성할 코드 양이 줄거나 하지는 않는다.그렇지만, 애플리케이션의 데이터를 관리하는 모델 컴포넌트가 있고 그 데이터를 UI 컴포넌트에 전달하는 단순한 데이터 흐름으로 이해하고 관리하기 쉬운 애플리케이션을 만들 수 있다.


## Node.js와 npm

### Node.js

#### Node.js란?
Node.js는 Chrome V8 Engine위에서 Runtime으로 동작하는 서버사이드 플랫폼이다.
주로 웹브라우저에서 동작하던 Javascript를 서버에서도 사용 가능하게 해준 장본인이다.

#### Node.js 특징
- 싱글 스레드  
- Non-Blocking I/O
    <!--- 기존 멀티 스레드 기반의 프로그램들은 Client에서 Request가 들어오면  Thread pool안에서 스레드를 가져다 사용하였다. 즉, Thread pool 안에 있는 Thread의 수가 Client의 수이다.
     할당된 스레드가 IO작업을 하게되면 blocking 방식으로 처리되어 해당 스레드가 대기상태로 변환된다. 
    즉, IO시간만큼 스레드는 blocking-->
- 빠른 생산성
- 뛰어난 확장성

#### Node.js가 쓰이면 좋은 곳
- 입출력이 잦은 어플리케이션
- 데이터 스트리밍 어플리케이션
- 데이터를 실시간으로 다루는 어플리케이션
- JSON API 기반 어플리케이션
- 싱글페이지 어플리케이션

<!--
Reference
https://velopert.com/133
http://d2.naver.com/helloworld/4994500
http://www.nextree.co.kr/p7292/
http://blog.coderifleman.com/2015/06/23/learning-react-1/
-->

### NPM

#### NPM이란?
NPM(Node Package Mangaer)은 Javascript 모듈을 다운받고 공유할 수 있게해주는 패키지 매니저이다. 또한 package.json 파일로 npm에서 다운받은 모듈들의 의존성을 관리해줄수있다. 

