# CSS Layout - display
## 블록 엘리먼트
**언제나 줄바꿈**
- 블록 엘리먼트 종류 → 가장 유명한 블록 엘리먼트는 \<div>\ 태그.
```
<address><article><aside><blockquote><canvas>
<dd><div><dl><dt><fieldset><figcaption><figure>
<footer><form><h1>-<h6><header><hr><li><main>
<nav><noscript><ol><p><pre><section><table><tfoot><ul><video>
```
## 인라인 엘리먼트
**공간이 충분하다면 줄바꿈 하지 않고 옆에 표시**
- 인라인 엘리먼트 종류 → 가장 유명한 블록 엘리먼트는 \<span>
```
<a><abbr><acronym><b><bdo><big><br>
<button><cite><code><dfn><em><i><img>
<input><kbd><label><map><object><output>
<q><samp><script><select><small><span><strong>
<sub><sup><textarea><time><tt>< var >
```
# display 속성
모든 HTML태그는 기본적으로 block 또는 inline속성을 가지고 있다.
display 속성을 이용해서 block, inline을 설정할 수 있다.
## block
기본값이 `width: 100% , height: auto` → 언제나 줄바꿈을 하면서 등장한다.
박스 형태로 width, height, margin, padding등 속성을 설정 할 수 있다.
## inline
컨텐츠 크기만큼 너비를 차지한다.
박스 형태가 아니기 때문에 width, height, margin, padding 속성을 설정할 수 없다.
## inline-block
block, inline의 특성을 모두 가지고 있는 속성값.
inline처럼 한 라인에 표시가 되고 block처럼 박스 형태로 width, height, margin, padding 지정이 가능하다.
- 예시
```html
span{
	display: inline-block;
	font-size: 3rem;
}
```
## none
화면에 표시하지 않게 하는 속성. → (꽤 자주 사용한다)
차지하는 *공간까지* 사라지도록 만든다.
비슷한 속성으로 `visibility hidden`이 있다.
	이 요소는 해당 요소가 차지하는 공간 자체는 남겨둔다.