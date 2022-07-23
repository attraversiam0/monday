## 👉 Quick menu

- [0.개요](#0개요)
- [1.변형(transform)](#1-변형transform)
    - [1-1. translate() 함수](#1-1-웹-요소를-이동시키는-translate-함수)
    - [1-2. scale() 함수](#1-2-요소를-확대-및-축소하는-scale-함수)
    - [1-3. rotate() 함수](#1-3-요소를-회전시키는-rotate-함수)
    - [1-4. skew() 함수](#1-4-요소를-비틀어-왜곡하는-skew-함수)
- [2.트랜지션(transition)](#2-트랜지션transition)
- [3.애니메이션(animation)](#3-애니메이션animation)

## 0.개요
변형(transform)이 트랜지션과 애니메이션의 속성값으로 사용됨.

--

## 1. 변형(transform)
기본형 `transform: 함수`

물체의 크기나 형태의 위치를 바꾸는 것.

### 1-1. 웹 요소를 이동시키는 translate() 함수
기본형 `transform: translate(tx, ty)
        transform: translate3d(tx, ty, tz)  
        transform: translateX(tx)
        transform: translateY(ty)
        transform: translateZ(tz)`
  
x축은 +값이면 오른쪽으로 이동, y축은 +값이면 아래쪽으로 이동, z축은 +값이면 보는 사람쪽으로 이동.

### 1-2. 요소를 확대 및 축소하는 scale() 함수
  
  기본형 `transform: scale(sx, sy)
          transform: scale3d(sx, sy, sz)
          tramsform: scaleX(sx)
          transform: scaleY(sy)
          transform: scaleZ(sz)`
  
  값은 배수. (2)는 2배, (0.7)은 0.7배

### 1-3. 요소를 회전시키는 rotate() 함수
  
  기본형 `transform: rotate(rx, ry, 각도)
          transform: rotate3d(rx, ry, rz, 각도)
          transform: rotateX(각도)
          transform: rotateY(각도)
          transform: rotateZ(각도)`
  
  각도는 deg 또는 래디안, 1래디안=180deg. 회전 각도가 +인 경우 오른쪽으로 회전하고, -인 경우 왼쪽으로 회전함.  
  이때, perspective 속성을 함께 사용하면 원근감을 추가해 입체적으로 표현됨.

### 1-4. 요소를 비틀어 왜곡하는 skew() 함수
  
  기본형 `transform: skew(x각도, y각도)
          transform: skewX(x각도)
          transform: skewY(y각도)`
  
  x각돗값이 +이면 / 반대 방향. y각돗값도 +이면 / 반대방향. 


---

## 2. 트랜지션(transition)  
기본형 `transition: 대상지정 진행시간 속도곡선 지연시간`

단순한 변형이 아닌 하나의 스타일을 완전히 다른 스타일로 변형. (=스타일 속성이 바뀌는 것.)  

|**종류**|설명|
|:---|:---|
|transition-property| 대상지정. all/none/속성이름(여럿일 경우 쉼표로 구분)|
|transition-duration| 진행시간. sec(속성이 여러 개라면 쉼표로 구분)|
|transition-timing-function| 속도곡선. linear/ease/ease-in/ease-out/ease-in-out/cubic-bezier(n,n,n,n)|
|transition-delay| 지연시간. sec|  

*transition 속성으로 한꺼번에 표기하는 경우 진행시간 다음 지연시간 순서.

```css
.box {
    transition: 2s ease-in;
}
.box:hover{
    width: 200px;
    height: 200px;
    background-color: #f50;
    transform: rotate(270deg);
}
```

---

## 3. 애니메이션(animation)  
기본형 `animation: 이름, 지속시간, 속도곡선, 지연시간, 반복횟수, 방향`  

|**종류**|설명|
|:---|:---|
|animation-name| 이름 |
|animation-duration| sec. 기본값이 0이므로 속성값을 정하지 않으면 애니메이션 실행되지 않음.|
|animation-timing-function| 속도곡선. linear/ease/ease-in/ease-out/ease-in-out/cubic-bezier(n,n,n,n) |
|animation-delay| 시작시간(지연시간) |
|animation-iteration-count| 숫자/infinite. |
|animation-direction| normal/reverse/alternate(홀수 번째 normal, 짝수 번째 reverse)/alternate-reverse |
|animation| |

`@keyframes 이름 {<선택자> {스타일}} `  
선택자는 from/ 50%/ to. 

```css
.box{
    width: 100px;
    height: 100px;
    margin: 60px auto;
    animation: rotate 1.5s infinite, background 1.5s infinite alternate;
}

@keyframes {
    from { transform: perspective(120px) rotate(0deg, 0deg); }
    to { transform: perspective(120px) rotate(-180deg, -180deg); }
}

@keyframes {
    from { background-color: red; }
    50% { background-color: green; }
    to {background-color: blue; }
}
```

## 참고

도서 - Do it! HTML + CSS + 자바스크립트 웹 표준의 정석

---

[👆](#👉-quick-menu)