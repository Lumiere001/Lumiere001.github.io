CSS의 핵심은 HTML의 어떤 부분을 어떻게 꾸밀 것인가이다.
선택자는 그중 어떤 부분을 정의하는데 필요한 개념이다.

# 기본 선택자
## 전체
문서 전체를 선택하는 선택자(\*)
```html
*{
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}
```
## 태그
태그명으로 선택
```html
h1 {
	color: red;
}
```
## id
id속성 값으로 선택(#아이디)
```html
#b {
	color: green;
}
```
아이디는 가능하면 유일하게 구분할 때 하나만 사용하기!
## class
class속성 값으로 선택(.)
```html
.common {
	color: blue;
}
```
## attribute
- \[속성]
- \[속성=속성값]
- 위와 같은 형식을 선택해서 사용한다.

- \[속성]의 경우 → a태그를 이용하는 경우 예시
```html
[href]
{
	color: blue;
}
```
href 속성을 가지고 있는 모든 a태그가 파란색으로 바뀜

- \[속성=속성값]의 경우 → a태그를 이용하는 경우 예시
```html
[href="htts://www.naver.com"]
{
	color: blue;
}
```
href=htts://www.naver.com인 속성을 가지고 있는 a태그만 파란색으로 바뀜

# CSS 우선순위
^b300f6
id > class=attribute > tag

[[CSS 배경 지식#^119657]]
# 심화 선택자
## 여러개 선택자
- 기본 선택자들을 조합해서 사용할 수 있다.
- 하나의 태그에도 여러개의 클래스가 설정될 수 있다.
```html
<div class="one two three">복수 클래스</div>

<!-- one, two, three클래스가 모두 요소에 포함되어 있는 것을 aqua색으로 지정하라는 의미 -->
.one.two.three {
	background-color: aqua;
}
```

```html
<!-- one클래스가 요소에 포함되어 있기만 하면 aqua색으로 지정하라는 의미 -->
.one {
	background-color: aqua;
}
```

```html
<!-- first 아이디, one, two클래스가 모두 요소에 포함되어 있는 것을 aqua색으로 지정하라는 의미 -->
#first.one.two {
	background-color: aqua;
}
```
# 복합 선택자
HTML 태그는 중첩하여 사용이 가능하다.
- 부모 태그 : 상위에 있는 태그
- 자식 태그 : 바로 하위에 있는 태그
- 후손 태그 : 바로 하위에 있는 태그 + 바로 하위에 있는 태그 이하로 있는 모든 테그들
- 형제 태그 : 같은 레벨에 있는 태그 → 같은 래벨인지 아닌지 보는 방법은 들여쓰기로 본다.

## 복합 선택자 종류
- 후손 : 띄어쓰기
- 자식: >
- 인접 형제: +
- 형제: ~
```html
/* 후손 */
.container .user-name {
	color: red;
}

/* 자식 */
.container > .item {
	background-color: blue;
}

/* 인접 형제 */
<!-- h3가 aqua색으로 변함 -->
h2 + h3 {
	color: aqua;
}

/* 형제 */
<!-- h5가 red색으로 변함 -->
h3 ~ h5 {
	color: red;
}
```
# 가상 선택자
요소에 클릭, 호버 등 다양한 이벤트가 일어났을 때를 표현하는 선택자

가상 선택자 종류
- :hover 마우스 호버(올라간) 상태
- :active 활성 상태 (마우스 클릭 후 때는 시점까지)
- :focus 포커스가 있는 상태 (input 입력창에서 커서가 깜빡이는 상태)
- :link 하이퍼링크에 방문하지 않은 상태
- :visited 하이퍼링크에 방문한 상태

```html
<!-- hover -->
button:hover {
	background-color: green;
}
<!-- active -->
.activated:active {
	background-color: gray;
}
<!-- focus -->
input:focus {
	background-color: red;
}
<!-- link -->
a:link {
	color: green;
}
<!-- visited -->
a:visited {
	color: red;
}
```
# 간단한 게임으로 선택자를 배울 수 있는 곳
https://flukeout.github.io/ → 개임
https://velog.io/@jaedie/CSS-Diner-%EC%99%84%EB%A3%8C%EB%8B%B5%EC%95%88%EC%9A%94%EC%A0%90%EC%A0%95%EB%A6%AC-13 → 정답

https://developer.mozilla.org/ko/docs/Learn/CSS/Building_blocks/Selectors → 강의 자료에 나와있는 참고 자료