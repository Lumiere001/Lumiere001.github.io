색상, 이미지, 크기 등 배경 스타일을 지정하는 속성으로 자주 사용한다.

# background-color
배경 색상을 지정하는 속성
색상코드 rgb, rgba로 지정할 수 있다.[[CSS 단위 정리#RGB]]
```html
background-color: blue;
```
# background-image
배경 이미지를 지정하는 속성
```html
background-image: url(...);
```
# background-size
배경 이미지의 크기를 설정
원본, 크기 수정, 공간에 맞게 등… 다양한 설정이 가능하다.
## 속성값
- contain
	- 이미지 비율이 바뀌지 않는 한도 안에서 가장 크게 설정
- cover
	- 이미지 비율이 바뀌지 않는 한도 안에서 가장 크게 설정
	  이미지의 비율이 요소와 다르다면 이미지를 가로/세로 방향으로 잘라내어 빈 공간이 생기지 않도록 한다.
- 너비, 높이 지정
```html
background-size: 500px 500px;
background-size: contain;
```
# background-repeat
배경 이미지의 반복 방법을 지칭
가로, 세로 공간에 따라 반복하거나 반복하지 않을 수 있다.
## 속성값
- repeat : 배경 영역을 채울 때까지 이미지를 반복하며, 넘치는 경우 이미지를 잘라낸다.
- no-repeat : 반복하지 않음
- space : 잘리지 않을 만큼 반복
- round : 공간이 늘어나면 이미지도 늘어나 여백을 남기지 않음
```html
background-repeat: no-repeat;
```
# background-position
background-image를 이용하면 기본적으로 좌측 상단에 이미지가 위치한다.
배경 이미지의 위치를 지정하는 속성임
## 속성값
- top, left, right, bottom, center
- x y
- right 10px bottom 10px → 위치를 구체적으로 설정 가능
```html
background-position: center;
```
# background-attachment
배경 이미지를 뷰포트에 고정할 것인지, 함께 스크롤 할 것인지에 대한 속성이다.
## 속성값
- scroll : 배경 이미지를 요소에 고정 (기본값)
- fixed : 배경을 뷰포트에 고정 (절대 위치)
```html
background-attachment: fixed;
```
# background 관련 속성 단축
`background: color image repeat attachment position`
+ position과 size 사이에는 “/”를 넣어서 구분 해줘야 한다!