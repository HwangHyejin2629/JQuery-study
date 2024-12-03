# JQuary
- 자바스크립트로 만들어진 라이브러리로 DOM(Document Object Model)을 더 쉽게 다룰 수 있다.
- 프로토타입으로 만들어진 클래스 : Jquery 배운다 = Jquery메서드를 배운다
- 크로스 브라우징 : 모든 브라우저에서 깨지지 않게 만들 수 있다.

## JQuery 기능
- DOM 작업 쉽다 : 메서드,노드추가, 삭제,찾기, 이동, 스타일, 수정, 값구하기, 속성추가, 수정, 값구하기, 이벤트등록, 발생, 위치, 크기 관련된 프로퍼티와 메서드
- Ajax : 데이터 서버와 통신 포멧
- 플러그인 : 많은 기능 만들어놓음
- 효과 : 에니메이션 기능 (javascript는 에니메이션 어려움)
- 모바일화면 JQueryMobile로 제작 가능
- API 문서 페이지 : http://api.jquery.com

## 다운로드
- lib 폴더 만들고 http://jquery.com/download/ 에서 다운로드 (compressed)
- <script src="/lib/jquery-버전.min.js></script>

## JQuery를 이용한 노드(웹요소) 찾기
- 선택자로 찾기(.,#,태그이름) :  $("CSS선택자") 
- 속성으로 노드 찾기 : $("[속성이름=값]")
```js
var $변수이름=$("CSS선택자") 
```
- $() : 함수호출 선택자에 해당하는 노드를 찾아주는 역할
- 선택자 : CSS 선택자 ID,CLASS,태그 -> 찾고싶은 선택자 만들어 $() 함수에 매개변수 값으로 넣어주면 된다.
- vae $변수이름 : $()함수에서 리턴값을 저장하는 변수, $붙이는 이유는 JQuery기능이 들어간 변수임을 표현


## JQuery 와 CSS관계
- css 선택자 알면 jQuery기능을 사용할 수 있다.

## JQuery핵심기능

### 이벤트 등록
- hover, onclick 등 이벤트
- $대상.on("이벤트이름","이벤트리스너");
- $대상.단축이벤트함수(이벤트리스너);
```js
$(document).ready(function(){ //document가 준비되면, 실행해라
    $("#btnCheck").on("click",function(){alert("환영합니다")})
    $("#btnCheck").click(funcion(){alert("환영합니다")})
})
```

### 스타일 설정
- $대상.css("스타일이름",값);
```js
$(document).ready(function(){ 
    $("#btnCheck").on("click",function){
        $("#panel").css("border","4px solid #f00")
    }
})
```
## 찾은 노드 다루기
- 찾은 개수 : $대상.length
- n번째 노드 접근 : $대상.eq(index)
- DOM 객체 접근 : $대상.get(index), $대상[index] 
- 순차적으로 노드 접근 : $대상.each(function(index){$(this) 또는 $대상.eq(index)})
- 찾은 노드중 특정노드만 찾기 : $대상.filter("선택자")
- 찾은 노드의 자손노드 중 특정노드 찾기 : $대상.find("선택자")
- 인덱스 값 : $대상.index() , $목록.index($대상) , $목록.index(대상Dom객체)

## 자식 노드 찾기
- 모든자식 : $대상.children("선택자") 
- 특정자식 : $대상.children().first , $대상.eq(index) 