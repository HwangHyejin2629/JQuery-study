# JQuary 사용법

## 다운로드
- lib 폴더 만들고 http://jquery.com/download/ 에서 다운로드 (compressed)
- <script src="/lib/jquery-버전.min.js></script>

## JQuery를 이용한 노드(웹요소) 찾기
```js
var $변수이름=$("CSS선택자") 
```
- $() : 함수호출 선택자에 해당하는 노드를 찾아주는 역할
- 선택자 : CSS 선택자 ID,CLASS,태그 -> 찾고싶은 선택자 만들어 $() 함수에 매개변수 값으로 넣어주면 된다.
- vae $변수이름 : $()함수에서 리턴값을 저장하는 변수 $붙이는 이유는 JQuery기능이 들어간 변수임을 표현

## JQuery 와 CSS관계