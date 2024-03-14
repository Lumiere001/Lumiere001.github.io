# font-size
폰트의 크기를 지정하는 속성. 주로 rem을 이용함
rem을 이용하면 웹/모바일 개발에서 유용하게 사용할 수 있음.
웹과 모바일의 화면 비율이 다르기 때문에 rem을 이용할 경우 모바일에서 따로 코드 수정을 하지 않아도 됨
(반대의 경우도 마찬가지)
[[CSS 단위 정리#^b4f3cc]]
# font-family
글꼴을 지정하는 속성
설정한 글꼴이 없는 경우를 대비하여 마지막은 generic family로 정해두기.
## generic family
- serif : 삐침 있는 명조계열의 글꼴
- sans-serif : 삐침 없고 굵기가 일정한 고딕계열의 글꼴
- monospace : 글자 폭과 간격이 일정한 글꼴
- cursive : 손으로 쓴 것 같은 필기계열의 글꼴
- fantasy : 화려한 글꼴
## 웹 폰트
사용자 PC환경에 관계없이 동일한 글꼴제공 가능!
- 구글 웹 폰트
- 눈누
- awesome font icon
## font-weight
폰트의 굵기를 설정하는 속성
## 속성값
- 100, 200, … 900
- normal = 400 / bold = 700
- bolder: 더 굵게 / lighter: 더 얇게
# font-height
택스트간의 세로 줄 간격을 설정하는 속성
일반적으로 단위 없이 숫자로 표현 함.

폰트 사이즈의 몇배로 라인 높이를 설정할 것인가에 대한 값으로 1~2 사이의 값을 주로 사용. (기본값은 1.2)
px, % em등의 단위도 사용 가능!
# text-align
글자의 수평 방향 정렬 방식을 설정하는 속성 (가운데 정렬 등…)
## 속성값
- left / right / center / justify
# text-decoration
글자에 선을 넣는 속성
## 속성값
- line-throght: 취소선
- overline: 글자 윗줄
- underline: 밑줄
# text-overflow
문자열이 지정된 공간을 벗어나는 경우 어떻게 처리할 것인가에 관련된 속성

**사용하기 위해서는 사전 조건이 있음**
→ 너비(weight)가 설정되어 있어야 함.
→ overflow hidden 설정 (컨텐츠가 블록을 가릴때 처리 방식에 관한 속성)
→ white-space: nowrap 설정 (줄바꿈, 공백을 어떻게 처리할 것인가에 관한 속성)
## 속성값
- clip : 자르기
- ellipsis : 점점점(…)으로 표시
```html
.text-overflow{
<!--사전 조건-->
	width: 300px;
	height: 300px;        <!--네모 박스 설정-->
	overflow: hidden;     <!--글자가 네모 박스를 넘어가면 안 보임-->
	white-space: nowrap;  <!--네모 박스를 넘어간 글자는 줄바꿈을 하지 않음-->
<!--text-overflow 사용-->
	text-overflow: clip;
}
```