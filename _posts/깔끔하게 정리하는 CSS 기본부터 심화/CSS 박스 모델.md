# block, inline-block에 대한 설명
GPT4.0 에게 물어봄
![[block, inline-block설명.png]]
# CSS 박스 모델
block, inline-block 속성값을 가지는 요소는 박스형태이다.

- content: 실제 html 태그 내 컨텐츠로써 내용이 차지하는 영역
- padding: 태두리(border)와 컨텐츠 사이의 여백
- border: 박스의 테두리
- margin: 테두리 바깥 여백
![[CSS Box Model.png]]
# 박스 모델과 관련된 CSS 주요 속성
- width & height
	- 컨텐츠의 너비와 높이를 지정하는 속성
- max-width, min-width & max-height, min-height
	- 너비, 높이의 최대, 최솟값을 지정하는 속성 → **반응형에서 주로 씀**
- border
	- 테두리의 두께, 색상, 스타일을 지정하는 속성
- padding (top right bottom left) (top&bottom left&right) → 시계 방향
	- 안쪽 여백 크기를 정하는 속성
- margin (top right bottom left) (top&bottom left&right) → 시계 방향
	- 외부 여백의 크기를 정하는 속성
- box-sizing (https://developer.mozilla.org/ko/docs/Web/CSS/box-sizing)
	- 너비와 높이의 기준(좌우, 상하 간격의 최대 틀)을 어떻게 잡을까에 관한 속성
- border-radius (https://developer.mozilla.org/ko/docs/Web/CSS/border-radius)
	- 테두리를 둥글게 만드는 속성
	- 단위는 다 사용 가능, 입력 순서는 시계방향! 왼쪽 위가 첫 시작임.
	- **`border-radius: 25%`**: each corner's radius is set to 25% of the box's width and height
- box-shadow (https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow)
	- 테두리를 감싼 그림자 효과를 추가
	- Tip → Google에 `box shoadow example`이라고 치면 다양한 예시를 볼 수 있다.(필요한 건 복붙해서 쓰면 됨)
## 예시
- border
```html
.app{
width: 300px;
height: 300px;

/* 테두리 */
/*
border-width: 10px;
border-color: black;
border-style: solid;
*/

<!--위 주석 표시한 부분과 같은 의미-->
border: 1px black solid;

}
```
- padding
```html
<!--하나만 있으면 4면의 모든 두께를 10px로 지정하는 것임. 아래 주석과 같은 의미-->
<!--두개 있으면 위 아래 & 양옆을 의미함-->
<!--세개 있으면 위, 양옆, 아래 두께를 의미함-->
padding 10px

/*
padding-top: 10px;
padding-right: 10px;
padding-bottom: 10px;
padding-left: 10px;
*/
```
- margin은 border, padding과 거의 비슷하므로 예시는 생략
---
- box-sizing
```html
*{
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}

.app{
	box-sizing: border-box;
	width: 300px;
	height: 300px;
	
	border: 1px black solid;
	padding: 10px;
	margin: 10px;
}
```
너비와 높이의 기준을 content로 하고 싶다면 content-box로 지정하면 된다.

- border-radius
```html
border-radius: 5%;
```

- box-shadow
```html
box-shadow: 10px 10px (50px) red;
```
- 첫 번째 10px : X축 이동 방향
- 두 번째 10px : Y축 이동 방향
	- → 여기에서 Y축 이동방향은 위 방향이 아니라 아래 방향임. 컴퓨터에서 Y축 양의 방향은 아래 방향이다,
- 세 번째 px: 블러 효과의 정도 → 생략 가능!
- 네 번째 red : 그림자의 색이 빨간색