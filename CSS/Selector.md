# Seletor

## 👉 바로가기

- [0. CSS선택자](#0-CSS선택자)
- [1. 전체 선택자(Universal Selector)](#1-전체-선택자universal-selector)
- [2. 타입 선택자(Type Selector)](#2-태그타입-선택자type-selector)
- [3. ID 선택자(ID Selector)](#3-id-선택자id-selector)
- [4. 클래스 선택자(Class Selector)](#4-클래스-선택자class-selector)
- [5. 연결 선택자(Combination Selector)](#5-연결-선택자combination-selector)
  - [5-1. 후손 선택자(Descendant Selector)](#5-1-후손-셀렉터-descendant-selector)
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

## 0. CSS선택자

style를 적용 하고자하는 HTML요소를 특정할 필요가 있다. 이때 사용하는 것이 셀렉터/선택자(Selector)이다. style를 적용하고자하는 HTML 요소를 셀렉터로 특정하고 선택된 요소에 스타일을 정의하는 것. 복수개의 셀렉터를 연속하여 지정할 수 있으며 쉼표(,)로 구분함.
![CSS Rule Set](../image/CSS/CSSRuleSet.png)

- 태그(tag): `<p></p>`와 같은 태그 자체
- 요소(element): `<p>hello world</p>`에서 `<p>`태그 및 내부 부분을 모두 포함

> `<p>`태그를 적용한 스타일이라는 표현은 옳지 않음. p요소에 적용하는 스타일로 표현하는 것이 옳바름.

---


---

## 참고

[poiemaweb 2-2 셀렉터](https://poiemaweb.com/css3-selector)  
도서 - HTML + CSS + 자바스크립트 웹 표준의 정석

---

[👆](#seletor)
