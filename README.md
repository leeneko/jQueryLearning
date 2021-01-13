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

