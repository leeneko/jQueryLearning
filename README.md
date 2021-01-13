# jQueryLearning
[![jQuery](https://jquery.com/jquery-wp-content/themes/jquery/images/logo-jquery.png "jQuery")](https://jquery.com/ "jQuery")

Learning : [w3schools jQuery Tutorial](https://www.w3schools.com/jquery/jquery_intro.asp "w3schools jQuery Tutorial")

jQuery 소개
---
필요한 사전 지식
- HTML
- CSS
- JavaScript

jQeury란?
---
가볍고, 적게 작성하지만 더 많은 작업을 수행하는 JavaScript 라이브러리입니다.
또한 AJAX 호출 및 DOM 조작과 같은 복잡한 JavaScript를 단순화합니다.

사용하는 방법으로는
- [jQuery Site](https://jquery.com/ "jQuery Site")로부터 다운로드
- [Google CDN](https://cloud.google.com/cdn "Google CDN")과 같은 곳으로부터 jQuery 포함

Production(압축된 라이브용), Development(코드 확인 가능) 중 용도에 맞게 다운로드하세요.

- 다운로드 한 경우, 작성할 HTML에 아래와 같이 포함하세요.
```html
<head>
<script src="jquery-3.5.1.min.js"></script>
</head>
```

- CDN으로부터 include(포함)할 경우
```html
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
</head>
```

jQuery Syntax(구문)
---
$('selector').action() 입니다.

예
$(this).hide() - 현재 요소를 숨깁니다.
$("p").hide() -모든 요소를 숨깁니다.
$(".test").hide() - test class인 모든 요소를 숨깁니다.
$("#test").hide() - id가 test인 요소를 숨깁니다.

문서 준비 이벤트
---
아래와 같이 사용하여 HTML 문서 로드가 완료되기 전에 jQuery 코드 실행을 방지합니다.
```html
$(function(){
  // jQuery methods go here...
});
```

jQuery Selectors(선택자)
---
- 버튼 클릭하여 p 태그 전부 hide 처리
```html
  $(document).ready(function() {
    $("button").click(function() {
      $("p").hide();
    });
  });
```

- &#35;id 선택자
```html
  $(document).ready(function(){
    $("button").click(function(){
      $("#test").hide();
    });
  });
```

- .class 선택자
```html
  $(document).ready(function(){
    $("button").click(function(){
      $(".test").hide();
    });
  });
```

문법 | 설명
-----|-----
`$("*")` | 모두 선택
`$(this)` | 현재 HTML 선택
`$("p.intro")` | class가 intro 인 p 태그 선택
`$("p:first")` | 첫번째 p 태그 선택
`$("ul li:first")` | 첫번째 ul 태그의 첫번째 li 태그 선택
`$("ul li:first-child")` | 모든 ul 태그의 첫번째 li 태그 선택
`$("[href]")` | href 속성이 있는 모든 태그 선택
`$("a[target='_blank']")` | target 값이 "_blank"인  a 태그 선택
`$("a[target!='_blank']")` | target 값이 "_blank"가 아닌 a 태그 선택
`$(":button")` | 모든 button 태그와 type이 button인 input 태그 선택
`$("tr:even")` | 짝수 인덱스 선택
`$("tr:odd")` | 홀수 인덱스 선택

작성한 jQuery를 별도의 파일로
---
```html
  <head>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    <script src"my_jquery_functions.js"></script>
  </head>
```

jQuery 이벤트 메소드
---
마우스 이벤트 | 키보드 이벤트 | 폼 이벤트 | 화면 이벤트
-----|-----|-----|-----
click | keypress | submit | load
dbclick | keydown | change | resize
mouseenter | keyup | focus | scroll
mouseleave |  | blur | unload

e.g.
```html
<script>
$(document).ready(function(){
  $("#p1").mouseenter(function(){
    alert("You entered p1!");
  });
});
</script>
```
