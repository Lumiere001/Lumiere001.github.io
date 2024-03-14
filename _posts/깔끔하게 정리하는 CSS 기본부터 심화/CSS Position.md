웹의 레이아웃을 설정하는데 사용된다.
## 속성값
- static: 기본값으로 고정을 의미합니다.
- relative: 기본 위치에 상대적으로 이동합니다.
- **absolute**: relative 속성을 가진 가장 가까운 부모 태그 기준으로 이동합니다.
  (부모 태그가 없을 경우 viewport기준으로 이동)
- fixed: viewport(화면) 기준으로 이동
- sticky: 스크롤 시에도 static 위치 고정

static 이외 속성값에서 공통적으로 top, left, right, bottom 값을 이용해서 위치를 조정
```html
.target {
  position: relative;
  top: 50px;
  left: 400px;
}
```
## Z-index
요소가 겹칠 때 z축 방향의 가중치를 설정하는 속성
숫자가 클 수록 앞으로 보내진다.
![[z-index.png]]
`쌓임 맥락의 계층 구조`
- DIV #1
- DIV #2
- DIV #3
    - DIV #4
    - DIV #5
    - DIV #6

같은 계층일 때 z값이 클 수록 앞으로 간다.
자식 계층이면 부모 계층 바로 위에 온다.
```html
z-index: 5;
```