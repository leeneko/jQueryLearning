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

jQuery 효과(Effects) - 숨기기 그리고 보이기(Hide and Show)
---
[jQuery Effect Methods](https://www.w3schools.com/jquery/jquery_ref_effects.asp)

.toggle() 을 사용해서 선택된 tag의 inline style에 display: none; 속성을 추가, 제거한다

```html
<!DOCTYPE html>
<html>
	<head>
		<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
		<script>
			$(document).ready(function(){
				$(".flip").click(function(){
					$(".panel").toggle();
				});
			});
		</script>
		<style type="text/css"> 
			div.panel,p.flip {
				line-height: 30px;
				margin:auto;
				font-size:16px;
				padding:5px;
				text-align:center;
				background:#555;
				border:solid 1px #666;
				color:#ffffff;
				border-radius:3px;
				user-select:none;
			}
			div.panel {
				display:none;
			}
			p.flip {
				cursor:pointer;
			}
		</style>
	</head>
	<body>
		<p class="flip">Click to show/hide panel</p>
		<div class="panel">
			<p>Because time is valuable, we deliver quick and easy learning.</p>
			<p>At W3Schools, you can study everything you need to learn, in an accessible and handy format.</p>
		</div>
	</body>
</html>
```

또한 아래와 같이 사용할 수도 있다
- speed : `$(selector).hide(speed);`
- speed, callback : `$(selector).hide(speed, callback);`

jQuery Effects - Fading
---
```html
$(document).ready(function(){
	$(".flip").click(function(){
		$(".panel").fadeToggle(1000);
	});
});
```

jQuery Effects - Sliding
---
```html
$(document).ready(function(){
	$(".flip").click(function(){
		$(".panel").slideToggle();
	});
});
```
