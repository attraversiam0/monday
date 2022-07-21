## 👉 Quick menu

- [0. CSS 선택자](#0-CSS-선택자)
- [1. 전체 선택자(Universal Selector)](#1-전체-선택자universal-selector)
- [2. 타입 선택자(Type Selector)](#2-타입-선택자type-selector)
- [3. 클래스 선택자(Class Selector)](#3-클래스-선택자class-selector)
- [4. ID 선택자(ID Selector)](#4-id-선택자id-selector)
- [5. 연결 선택자(Combination Selector)](#5-연결-선택자combination-selector)
  - [5-1. 하위 선택자(Descendant Selector)](#5-1-하위-선택자descendant-selector)
  - [5-2. 자식 선택자(Child Selector)](#5-2-자식-선택자child-selector)
  - [5-3. 형제(동위) 선택자 (Sibling)](#5-3-형제동위-선택자-sibling)
    - [5-3-1. 인접 형제 선택자(Adjacent selector)](#5-3-1-인접-형제-선택자-adjacent-selector)
    - [5-3-2. 형제 선택자(Sibling selector)](#5-3-2-형제-선택자-sibling-selector)
- [6. 속성 선택자(Attribute Selector)](#6-속성-선택자attribute-selector))
- [7. 가상 클래스 선택자 (Pseudo-Class Selector)](#7-가상-클래스-선택자-pseudo-class-selector)
  - [7-1. 사용자 동작 반응 선택자 (User action pseudo-classes)](#7-1-사용자-동작-반응-선택자-user-action-pseudo-classes)
  - [7-2. UI 요소 상태 선택자 (UI element states pseudo-classes)](#7-2-ui-요소-상태-선택자-ui-element-states-pseudo-classes)
  - [7-3. 구조 가상 클래스 셀렉터 (Structural pseudo-classes)](#7-3-구조-가상-클래스-셀렉터-structural-pseudo-classes)
- [8. 가상 요소 선택자 (Pseudo-Element Selector)](#8-가상-요소-선택자-pseudo-element-selector)
- [참고](#참고)

---

## 0. CSS 선택자

웹 문서에서 어느 부분에 스타일을 적용할지 알려주는 것. 복수개의 셀렉터를 연속하여 지정할 수 있으며 쉼표(,)로 구분함.

---

## 1. 전체 선택자(Universal Selector)

기본형 `* { 속성: 값; ...}`

문서의 모든 요소에 적용. 기본 스타일을 초기화할 때 사용(예: 전체 문서 마진과 패딩 여백 0)
> 자주 사용 시 브라우저에 과부하 걸릴 수 있음. 사용에 유의.

---

## 2. 타입 선택자(Type Selector)

기본형 `태그명 {스타일 규칙}`

특정 태그를 사용한 모든 요소에 스타일 적용.

---

## 3. 클래스 선택자(Class Selector)

기본형 `.클래스명 {스타일 규칙}` --적용--> `class="클래스명"`

특정 부분을 선택해서 스타일 적용.

---

## 4. ID 선택자(ID Selector)

기본형 `#아이디명 {스타일 규칙}` --적용--> `id="아이디명"`

특정 부분을 선택해서 스타일 적용. 주로 문서의 레이아웃과 관련된 스타일을 지정하거나 웹 요소에 자바스크립트 프로그램을 사용하면서 요소를 구별할 때 사용.
> cf. 클래스 선택자와 달리 문서에서 한 번만 적용 가능.

---

## 5. 연결 선택자(Combination Selector)
둘 이상의 선택자를 연결. (=조합선택자, 콤비네이션 선택자)

### 5-1. 하위 선택자(Descendant Selector)

기본형 `상위요소 하위요소`

부모 요소에 포함된 하위 요소를 모두 선택함. 자손 선택자라고도 함.
```css
li a {
  text-decoration: none;
}
```

### 5-2. 자식 선택자(Child Selector)

기본형 `부모요소 > 자식요소`

부모 요소에 포함된 자식 요소만 선택함. 

```css
#container > ul {
  border: 1px solid black;
}
```
```html
<div id="container">
   <ul>
      <li> List Item
        <ul>
           <li> Child </li>
        </ul>
      </li>
      <li> List Item </li>
      <li> List Item </li>
      <li> List Item </li>
   </ul>
</div>
```
> cf. 하위 선택자와 달리 손자 요소 이하는 선택하지 않음. 첫 번째 li의 자식인 ul은 대상이 되지 않음.

### 5-3. 형제(동위) 선택자 (Sibling)
부모 요소가 같은 경우. 먼저 나오는 요소를 형 요소, 나중에 나오는 요소를 동생 요소라고 함.

### 5-3-1. 인접 형제 선택자 (Adjacent selector)
기본형 `형 요소 + 동생 요소`

형 요소 이후 가장 먼저 오는 동생 요소를 선택함.
```css
h1 + p {color: blue;}
```
```html
<h1>예약 방법 & 이용ㅇ요금<h1>
<p>아직 온라인 예약</p>
<p>가족실(2~4인) : 60,000원/일</p>
```
> '아직 온라인 예약'에만 css 적용.

### 5-3-2. 형제 선택자 (Sibling selector)
기본형 `형 요소 ~ 동생 요소`

형 요소의 동생 요소를 모두 선택함.

```css
h1 ~ p {
    color: blue;
}
```
```html
<h1>예약 방법 & 이용ㅇ요금<h1>
<p>아직 온라인 예약</p>
<p>가족실(2~4인) : 60,000원/일</p>
```
> cf. 인접 형제 선택자와 달리 모든 p요소에 css적용.

---

## 6. 속성 선택자(Attribute Selector)
태그 안에서 사용하는 속성값에 따라 요소를 선택함.

|**종류**|설명|
|:---:|:---|
|[속성]| 해당 속성이 있는 요소|
|[속성 = 값]| 지정한 속성값이 있는 요소|
|[속성 ~= 값]| 지정한 속성값이 있는 요소(단어별)|
|[속성ㅣ= 값]| 지정한 속성값이 포함된 요소(하이픈 포함, 단어별)|
|[속성 ^= 값]| 지정한 속성값으로 시작하는 요소|
|[속성 $= 값]| 지정한 속성값으로 끝나는 요소|
|[속성 *^*= 값]| 지정한 속성값의 일부가 일치하는 요소|

---

## 7. 가상 클래스 선택자 (Pseudo-Class Selector)

### 7-1. 사용자 동작 반응 선택자 (User action pseudo-classes)

|**종류**|설명|
|:---:|:---|
|:link| 방문하지 않은 링크에 스타일 적용|
|:visited| 방문했던 링크에 스타일 적용|
|:hover| 지정한 요소에 마우스 포인터를 올려놓을 때 스타일을 적용|
|:active| 지정한 요소를 활성화했을 때 스타일을 적용|
|:focus| 지정한 요소에 초점이 맞춰졌을 때 스타일을 적용|

> ~active까지 순서대로 정의해야 함. LoVe HAte

---

### 7-2. UI 요소 상태 선택자 (UI element states pseudo-classes)

|**종류**|설명|
|:---:|:---|
|:target| 앵커 대상에 스타일 적용|
|:enabled| 지정한 요소를 사용할 수 있는 상태일 때 스타일 적용|
|:disabled| 지정한 요소를 사용할 수 없는 상태일 때 스타일 적용|
|:checked| 선택한 요소의 스타일을 적용|
|:not| 지정한 요소가 아닐 때 선택해서 스타일 적용|

---

### 7-3. 구조 가상 클래스 셀렉터 (Structural pseudo-classes)
웹 문서의 구조를 기준으로 특정 위치에 있는 요소를 찾아 스타일을 적용할 때 사용. class나 id를 사용하지 않고 스타일을 지정할 수 있음.

|**종류(A:요소)**|설명|
|:---:|:---|
|:only-child/ A:only-type-of| 부모 안에 자식 요소가 하나뿐일 때 선택|
|:first-child/ A:first-of-type| 부모 안에 있는 요소 중 첫 번째 자식 요소 선택|
|:last-child/ A:last-of-type| 부모 안에 있는 요소 중 마지막 자식 요소 선택|
|:nth-child(n)/ A:nth-of-type(n)| 부모 안에 있는 요소 중에서 n번째 자식 요소 선택|
|:nth-last-child(n)/ A:nth-of-type(n)| 부모 안에 있는 요소 중에서 끝에서 n번째 자식 요소 선택|

```css
table tr:nth-child(odd) {
    background color: light gray;
}
```
> 홀수 번째 열만 스타일 적용

---

## 8. 가상 요소 선택자 (Pseudo-Element Selector)
요소 상태에 따른 가상 클래스

|**종류**|설명|
|:---:|:---|
|::first-line| 첫 번째 줄 선택|
|::first-letter| 줄에서 첫 번째 글자를 선택|
|::before| 특정 요소의 앞에 내용이나 스타일 추가|
|::after| 특정 요소의 뒤에 내용이나 스타일 추가|

---

## 참고

https://github.com/nlom0218/TIL/blob/main/CSS/Selector.md#4-id-%EC%85%80%EB%A0%89%ED%84%B0id-selector 

https://code.tutsplus.com/ko/tutorials/the-30-css-selectors-you-must-memorize--net-16048

도서 - Do it! HTML + CSS + 자바스크립트 웹 표준의 정석

---

[👆](#👉-quick-menu)