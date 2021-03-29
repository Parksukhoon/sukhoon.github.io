# HTML

- 해당 내용은 생활코딩 강의(WEB1 - HTML & Internet)를 정리한 내용입니다.

### 1) 코딩과 HTML

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled.png)

웹페이지를 만드는 코드인 'HTML'

 장점 1 = 쉽다. 웹 페이지를 만드는 그 어떠한 언어보다도 쉽다.

 장점 2 = 퍼블릭 도메인. 저작권이 없다.

### 2) HTML 코딩 실습 환경 준비

 웹 페이지와 코드를 작성하는 프로그램인 '에디터'가 있어야 함.

 본 강의에서는 '아톰'이라는 에디터를 사용함(검색어 : HTML editor, best HTML editor 2021)

 새 파일을 생성하고(1.html) window의 경우 Ctrl + O를 누르면 새 창이 뜸

 원하는 메시지를 입력(ex. hello web)한 후 저장하면, 실시간 반영(visual studio code의 Go Live)

### 3) 기본문법 - 태그

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%201.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%201.png)

<strong>메시지</strong>  = 굵은 글씨

<u>메시지 </u> = 밑줄

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%202.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%202.png)

### 4) 혁명적인 변화

<h1> 태그란?
코드 :

```html
<h1>Beetles</h1>
<h2>External morphology</h2>
<h3>Head</h3>
<h4>Mouthparts</h4>
<h3>Thorax</h3>
<h4>Prothorax</h4>
<h4>Pterothorax</h4>
```



![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%203.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%203.png)

(출처 : [https://developer.mozilla.org/ko/docs/Web/HTML/Element/Heading_Elements](https://developer.mozilla.org/ko/docs/Web/HTML/Element/Heading_Elements))

<실습>

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%204.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%204.png)

<출력결과>

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%205.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%205.png)

'제목스러운' 것을 만들었다!

### 5) 통계에 기반한 학습

[https://www.advancedwebranking.com/html/](https://www.advancedwebranking.com/html/)

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%206.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%206.png)

 25개~30개의 tag를 알고 있다면, '어느 정도' 커버한다고 할 수 있다.

모든 것을 다 공부한다기보다는, 잘 쓰이는 것들을 공부하고, 모르는 것을 '찾아보는 습관'이 중요.

### 6) 줄바꿈

br, p

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%207.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%207.png)

<br>br을 이용하면 한 줄 띄우기가 가능하다. 여러 번 쓰면, 여러 줄이 띄워질 수 있다(조금 더 자유도가 높다)

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%208.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%208.png)

가운데 <br>을 네 번 써서 공백이 보다 많이 생긴 것을 확인할 수 있다.

반면 p는 단락임을 표시하는 태그이다.

단락을 표시할 때는 보다 좋지만, 문제는 원하는 만큼의 공간을 띄워놓을 수 없다는 단점이 있다.

→ css를 이용해서 해결 가능

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%209.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%209.png)

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2010.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2010.png)

<p style = "margin-top : 70px">를 통해 단락 간 구분을 넓게한 것을 확인할 수 있다.

### 7) HTML이 중요한 이유

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2011.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2011.png)

일반인(글씨 크기 변경) vs 지식인?(<h3></h3>)

'지식인'의 사이트가 보다 상위에 노출됨.

검색 엔진에서 하위에 위치한다 → 존재하지 않는다와는 말과 동일함.

html의 의미에 맞게 쓴다는 것은 비즈니스에 있어 '생명줄'과 같음.

Web은 접근성이 매우 높으며, 그 누구도 접근할 수 있다.

→ 시각장애인 등 어려운 분들께도 정보를 제대로 전달할 수 있는 수단이 됨.

### 8) 최후의 문법 속성과 img

<img>태그

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2012.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2012.png)

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2013.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2013.png)

<img width = "100%" src = "helpme.jpg">와 같은 방식을 통해 이미지를 삽입할 수 있다.

width = "100%"로 둘 경우, 화면에 딱 맞게 설정 가능.

이미지는 [unsplash](https://unsplash.com/).com을 통해서 쉽게 다운받을 수 있다.

### 9) 부모 자식과 목록

<parent>

<child></child>

</parent>

<li> 태그는 반드시 부모 태그인 <ul>을 가지고 있고, <ul> 역시 자식 태그를 가지고 있다.

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2014.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2014.png)

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2015.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2015.png)

<li>를 통해서 목록임을 표시할 수 있으며,

<ul>을 통해서 부모-자식 관계를 설정하고, 범주화할 수 있다.

문제는 HTML, CSS, JavaScript 중 만약 1. HTML을 없앤다면, 일일히 번호를 다 다시 수정해야 한다.

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2016.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2016.png)

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2017.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2017.png)

그럴 경우를 대비하여 <ol>로 해두면, 변경 사항이 자동적으로 반영됨을 알 수 있다.

ol = ordered list

ul = unordered list

### 10) 문서의 구조와 슈퍼스타들

<title>web1 - html</title> 을 통해 제목을 설정할 수 있다.

<meta charset="utf-8"> 코드를 설정하면, 한국어도 깨지지 않고 페이지에 반영 가능하다.

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2018.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2018.png)

html 코드는 <head></head>와 <body></body> 중에 하나에 위치해야 한다.

<head>에는 <body>의 코드를 설명해주는 코드가, <body>는 본문 내용이 해당된다.

이러한 <head>와 <body>를 모두 감싸는 <html>이 있으며,

이 문서가 html임을 표시하기 위해 관용적으로 <!doctype html>이라고 표기해야 한다.

### 11) HTML 태그의 제왕

링크를 거는 <a> 태그

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2019.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2019.png)

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2020.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2020.png)

<a> 태그를 이용해서 링크를 걸어줄 수 있다.

a = anchor

링크 걸 주소는 href = ""이다. h(omepage) + ref(erence)

저렇게 저장을 해두면, 페이지가 링크 걸어둔 페이지로 바뀌는 것을 확인할 수 있다.

만약, 새 페이지로 열 것이라면 target = "_blank"를 추가하면 되고,

해당 링크의 제목을 달기 위해서는 title = "html5 specification"과 같이, title = "제목" 을 달면 된다.

### 12) 웹사이트 완성

<이렇게 만드는게 목표다>

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2021.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2021.png)

<WEB> 만들기

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2022.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2022.png)

기존 1.html 파일을 3개 더 복사해서 각각 index.html, 1.html, 2.html, 3.html로 생성

새롭게 생성된 파일별로 정보를 다르게 입력하면 됨

<title> <h2> <p> 부분에 각 페이지에 맞는 내용 삽입

ex) WEB1 - Welcome, WEB... 

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2023.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2023.png)

### 13)  원시웹

웹의 역사를 살펴보면서 웹을 이해하는 과정

Internet vs Web

도시 vs 건물

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2024.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2024.png)

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2025.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2025.png)

인터넷 - 중앙이 없고, 하나하나가 각 기지국과 같은 역할을 수행.

[http://info.cern.ch/](http://info.cern.ch/) 최초의 웹(웹의 역사, 1990) = 원시웹(primitive web)

### 14) 인터넷을 여는 열쇠 : 서버와 클라이언트

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2026.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2026.png)

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2027.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2027.png)

웹 서버를 사용할 줄 안다는 것은,

다른 사용자가 웹 브라우저를 깔면 내 정보를 볼 수 있다는 것을 의미

방법 1) 웹 서버를 자신의 컴퓨터에 직접 까는 것

→ 많이 배우겠지?(순서 2. 웹 서버를 통해서 원리를 파악해보는 것)

방법 2) 대행해주는 업체에게 맡기는 것

→ 쉬움(순서 1. 쉽게 해보고)

### 15) 웹호스팅(github pages)

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2028.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2028.png)

- 웹호스팅 추천 사이트
- [https://bitballoon.com](https://bitballoon.com/)
- [http://neocities.org](http://neocities.org/)
- [Azure Blob](https://azure.microsoft.com/en-us/services/storage/blobs/)
- [Google Cloud Storage](https://cloud.google.com/storage/)
- [Amazon S3](http://aws.amazon.com/s3)

### 16) 웹서버 운영하기(Apache)

how to install apache http server window 2021

to be continued...([https://opentutorials.org/course/3084/18893](https://opentutorials.org/course/3084/18893))

### 17) 수업을 마치며

![HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2029.png](HTML%20fc88e1659d284dfda2fac733bc3f7e25/Untitled%2029.png)