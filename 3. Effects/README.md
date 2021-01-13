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
