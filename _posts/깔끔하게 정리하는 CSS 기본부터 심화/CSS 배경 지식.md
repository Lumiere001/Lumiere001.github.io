CSS(Cascading Style Sheets)란, HTML을 꾸미는 기술
핵심은 HTML의 어떤 부분을 어떻게 꾸밀지 정하는 것!

# 선택자(Selector)
HTML 문서에 존재하는 어떠한 부분을 선택하기 위해 존재하는 개념
![[CSS배경지식.png]]
# HTML CSS 연결하는 방법
## 대상 태그 내부 style 속성 사용
```html
<h1 style="color:red">빨강</h1>
```
## head 태그 내부 style 태그 선언
```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<style>
			h1 {
				color: red;
			}
		</style>
	</head>
	<body>
		<h1>빨간맛</h1>
	</body>
</htlm>
```
## 파일 분리 (가장 자주 쓰는 방식!!)
```html
<head>
	<link rel="stylesheet" href="style.css">
<head>
```

# 우선 순위
CSS에서 cascade는 ‘계단식’이라는 의미를 가지고 있다.
동일한 요소에 서로 다른 CSS를 적용했을 때 충돌이 일어난다.
대부분 나중에 선언된 스타일로 적용이 된다.

`예외 사항`
선택자 별로 아래와 같은 우선순위가 존재한다.
	id > class > tag ^119657
	[[CSS 선택자#^b300f6]]
- 예시
```html
<!-- id 선택자 -->
#b {  
	color: green;
}

<!-- class 선택자 -->
.a {
	color: blue;
}

<!-- tag 선택자 -->
h1 {
	color: red;
}
```

# 기본 셋팅
브러우저마다 기본 스타일이 지정되어 있다.
같은 태그라 해도 브라우저마다 조금씩 다르게 보일 수 있는 점을 취소화 시키기 위해
기본적으로 아래와 같은 CSS 속성을 설정하고 시작한다.
```html
* {
	margin: 0;
	padding: 0;
	box-sizing: border-box:
}

html {
	font-size: 10px;
}
```