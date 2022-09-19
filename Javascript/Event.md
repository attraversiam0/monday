
## 0. 이벤트(Event)

웹 브라우저에서 일어나는 사건(웹 브라우저나 사용자가 행하는 어떤 동작)

---

## 1. 주요 이벤트

### 1-1. 마우스 이벤트
|**종류**|설명|
|:---|:---|
|click| 사용자가 html요소를 클릭할 때|
|dbclick| 사용자가 html요소를 더블클릭할 때|
|mousedown| 사용자가 요소 위에서 마우스 버튼으 눌렀을 때|
|mousemove| 사용자가 요소 위에서 마우스 포인터를 움직일 때|
|mouseover| 마우스 포인터가 요소 위로 옮겨질 때|
|mouseout| 마우스 포인터가 요소를 벗어날 때|
|mouseup| 사용자가 요소 위에 놓인 마우스 버튼에서 손을 뗄 때|

### 1-2. 키보드 이벤트
|**종류**|설명|
|:---|:---|
|keydown| 사용자가 키를 누르는 동안|
|keypress| 사용자가 키를 눌렀을 때|
|keyup| 사용자가 키에서 손을 땔 때|

### 1-3. 문서 로딩 이벤트
|**종류**|설명|
|:---|:---|
|abort| 문서가 완전히 로딩되기 전에 불러오기를 멈췄을 때|
|error| 문서가 정확히 로딩되지 않았을 때|
|load| 문서가 로딩이 끝나면|
|resize| 문서 화면 크기가 바뀌었을 때|
|scroll| 문서 화면이 스크롤되었을 때|
|unload| 문서에서 벗어날 때|

### 1-4. 폼 이벤트
|**종류**|설명|
|:---|:---|
|blur| 폼 요소에 포커스를 잃었을 때|
|change| 목록이나 체크 상태 등이 변경되면(input, select, textarea 태그에서 사용)|
|focus| 폼 요소에 포커스가 놓였을 때(label, select, textarea, button 태그에서 사용)|
|reset| 폼이 리셋되었을 때|
|submit| submit버튼을 클릭했을 때|

---

## 2. 이벤트 처리기/핸들러(event handler)
웹 문서에서 이벤트가 발생하면 처리하는 함수

### 2-1. html 태그에 직접 연결

기본형 `<태그 on이벤트명 = "함수명">`

```html
<body>
  <input type="button" value="night" onclick="alert('다크모드')">
```


### 2-2. DOM 이용

기본형 `<웹 요소.onclick = 함수;>`

2-1. 형식은 html이 주인이나 DOM을 사용하면 자바스크립트가 주인이 되어 html요소를 가져온다.

```html
  <button id="change">글자색 바꾸기</button>

<script>
  var chageBttn = document.querySelector("#change");
  changeBttn.onclick = changeColor;
</script>
```

## 참고

도서 - Do it! HTML + CSS + 자바스크립트 웹 표준의 정석
생활코딩 - 자바스크립트 기초/ 4. HTML과 JS의 만남 : 이벤트