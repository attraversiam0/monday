# Seletor

## 👉 Quick menu

- [0. CSS 선택자](#0-CSS-선택자)
- [1. 전체 선택자(Universal Selector)](#1-전체-선택자-universal-selector)
- [2. 타입 선택자(Type Selector)](#2-타입-선택자-type-selector)
- [3. 클래스 선택자(Class Selector)](#4-클래스-선택자class-selector)
- [4. ID 선택자(ID Selector)](#3-id-선택자-id-selector)
- [5. 연결 선택자(Combination Selector)](#5-연결-선택자combination-selector)
  - [5-1. 하위 선택자(Descendant Selector)](#5-1-하위-선택자-descendant-selector)
  - [5-2. 자식 선택자(Child Selector)](#5-2-자식-셀렉터-child-selector)
  - [5-3. 형제(동위) 선택자 (Sibling)](#5-3-형제동위-셀렉터-sibling-selector)
    - [5-3-1. 인접 형제 선택자(Adjacent selector)](#5-3-1-인접-형제-선택자-adjacent-selector)
    - [5-3-2. 형제 선택자(Sibling selector)](#5-3-2-형제-선택자-sibling-selector)
- [6. 속성 선택자(Attribute Selector)](#6-속성-선택자-attribute-selector)
- [7. 가상 클래스 선택자 (Pseudo-Class Selector)](#7-가상-클래스-선택자-pseudo-class-selector)
  - [7-1. 사용자 동작 반응 선택자 (User action pseudo-classes)](#7-1-사용자-동작-반응-선택자-user-action-pseudo-classes)
  - [7-2. UI 요소 상태 선택자 (UI element states pseudo-classes)](#7-2-ui-요소-상태-선택자-ui-element-states-pseudo-classes)
  - [7-3. 구조 가상 클래스 셀렉터 (Structural pseudo-classes)](#7-3-구조-가상-클래스-선택자-structural-pseudo-classes)
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

기본형 `상위요소 하위요소`

부모 요소에 포함된 하위 요소를 모두 선택함. 자손 선택자라고도 함.
```
li a {
  text-decoration: none;
}
```

---

## 6. 속성 선택자(Attribute Selector)

---

## 7. 가상 클래스 선택자 (Pseudo-Class Selector)

---

## 8. 가상 요소 선택자 (Pseudo-Element Selector)

---
## 참고

https://code.tutsplus.com/ko/tutorials/the-30-css-selectors-you-must-memorize--net-16048

도서 - Do it! HTML + CSS + 자바스크립트 웹 표준의 정석

---

[👆](#seletor)
