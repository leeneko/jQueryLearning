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

그 외의 이벤트 [link](https://www.w3schools.com/jquery/jquery_ref_events.asp "link")
mousedown(), mouseup(), hover(), focus(), blur(), on() ...

e.g. p1 id를 가진 태그 위로 마우스가 올라가면 hover 이벤트 발생, 마우스가 떠나면 나머지 이벤트 발생
```html
<script>
$(document).ready(function(){
  $("#p1").hover(function(){
    alert("You entered p1!");
  }, function(){
    alert("Bye! You now leave p1!");
  }); 
});
</script>
```
