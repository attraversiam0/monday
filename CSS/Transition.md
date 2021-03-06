## π Quick menu

- [0.κ°μ](#0κ°μ)
- [1.λ³ν(transform)](#1-λ³νtransform)
    - [1-1. translate() ν¨μ](#1-1-μΉ-μμλ₯Ό-μ΄λμν€λ-translate-ν¨μ)
    - [1-2. scale() ν¨μ](#1-2-μμλ₯Ό-νλ-λ°-μΆμνλ-scale-ν¨μ)
    - [1-3. rotate() ν¨μ](#1-3-μμλ₯Ό-νμ μν€λ-rotate-ν¨μ)
    - [1-4. skew() ν¨μ](#1-4-μμλ₯Ό-λΉνμ΄-μκ³‘νλ-skew-ν¨μ)
- [2.νΈλμ§μ(transition)](#2-νΈλμ§μtransition)
- [3.μ λλ©μ΄μ(animation)](#3-μ λλ©μ΄μanimation)

## 0.κ°μ
λ³ν(transform)μ΄ νΈλμ§μκ³Ό μ λλ©μ΄μμ μμ±κ°μΌλ‘ μ¬μ©λ¨.

---

## 1. λ³ν(transform)
κΈ°λ³Έν `transform: ν¨μ`

λ¬Όμ²΄μ ν¬κΈ°λ ννμ μμΉλ₯Ό λ°κΎΈλ κ².

### 1-1. μΉ μμλ₯Ό μ΄λμν€λ translate() ν¨μ
κΈ°λ³Έν `transform: translate(tx, ty)
        transform: translate3d(tx, ty, tz)  
        transform: translateX(tx)
        transform: translateY(ty)
        transform: translateZ(tz)`
  
> xμΆμ +κ°μ΄λ©΄ μ€λ₯Έμͺ½μΌλ‘ μ΄λ, yμΆμ +κ°μ΄λ©΄ μλμͺ½μΌλ‘ μ΄λ, zμΆμ +κ°μ΄λ©΄ λ³΄λ μ¬λμͺ½μΌλ‘ μ΄λ.

### 1-2. μμλ₯Ό νλ λ° μΆμνλ scale() ν¨μ
  
  κΈ°λ³Έν `transform: scale(sx, sy)
          transform: scale3d(sx, sy, sz)
          tramsform: scaleX(sx)
          transform: scaleY(sy)
          transform: scaleZ(sz)`
  
> κ°μ λ°°μ. (2)λ 2λ°°, (0.7)μ 0.7λ°°

### 1-3. μμλ₯Ό νμ μν€λ rotate() ν¨μ
  
  κΈ°λ³Έν `transform: rotate(rx, ry, κ°λ)
          transform: rotate3d(rx, ry, rz, κ°λ)
          transform: rotateX(κ°λ)
          transform: rotateY(κ°λ)
          transform: rotateZ(κ°λ)`
  
> κ°λλ deg λλ λλμ, 1λλμ=180deg. νμ  κ°λκ° +μΈ κ²½μ° μ€λ₯Έμͺ½μΌλ‘ νμ νκ³ , -μΈ κ²½μ° μΌμͺ½μΌλ‘ νμ ν¨.  
μ΄λ, perspective μμ±μ ν¨κ» μ¬μ©νλ©΄ μκ·Όκ°μ μΆκ°ν΄ μμ²΄μ μΌλ‘ ννλ¨.

### 1-4. μμλ₯Ό λΉνμ΄ μκ³‘νλ skew() ν¨μ
  
  κΈ°λ³Έν `transform: skew(xκ°λ, yκ°λ)
          transform: skewX(xκ°λ)
          transform: skewY(yκ°λ)`

> xκ°λκ°μ΄ +μ΄λ©΄ / λ°λ λ°©ν₯. yκ°λκ°λ +μ΄λ©΄ / λ°λλ°©ν₯. 


---

## 2. νΈλμ§μ(transition)  
κΈ°λ³Έν `transition: λμμ§μ  μ§νμκ° μλκ³‘μ  μ§μ°μκ°`

λ¨μν λ³νμ΄ μλ νλμ μ€νμΌμ μμ ν λ€λ₯Έ μ€νμΌλ‘ λ³ν. (=μ€νμΌ μμ±μ΄ λ°λλ κ².)  

|**μ’λ₯**|μ€λͺ|
|:---|:---|
|transition-property| λμμ§μ . all/none/μμ±μ΄λ¦(μ¬λΏμΌ κ²½μ° μΌνλ‘ κ΅¬λΆ)|
|transition-duration| μ§νμκ°. sec(μμ±μ΄ μ¬λ¬ κ°λΌλ©΄ μΌνλ‘ κ΅¬λΆ)|
|transition-timing-function| μλκ³‘μ . linear/ease/ease-in/ease-out/ease-in-out/cubic-bezier(n,n,n,n)|
|transition-delay| μ§μ°μκ°. sec|  

*transition μμ±μΌλ‘ νκΊΌλ²μ νκΈ°νλ κ²½μ° μ§νμκ° λ€μ μ§μ°μκ° μμ.

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

## 3. μ λλ©μ΄μ(animation)  
κΈ°λ³Έν `animation: μ΄λ¦, μ§μμκ°, μλκ³‘μ , μ§μ°μκ°, λ°λ³΅νμ, λ°©ν₯`  

|**μ’λ₯**|μ€λͺ|
|:---|:---|
|animation-name| μ΄λ¦ |
|animation-duration| sec. κΈ°λ³Έκ°μ΄ 0μ΄λ―λ‘ μμ±κ°μ μ νμ§ μμΌλ©΄ μ λλ©μ΄μ μ€νλμ§ μμ.|
|animation-timing-function| μλκ³‘μ . linear/ease/ease-in/ease-out/ease-in-out/cubic-bezier(n,n,n,n) |
|animation-delay| μμμκ°(μ§μ°μκ°) |
|animation-iteration-count| μ«μ/infinite. |
|animation-direction| normal/reverse/alternate(νμ λ²μ§Έ normal, μ§μ λ²μ§Έ reverse)/alternate-reverse |
|animation| |

`@keyframes μ΄λ¦ {<μ νμ> {μ€νμΌ}} `  
> μ νμλ from/ 50%/ to. 

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

## μ°Έκ³ 

λμ - Do it! HTML + CSS + μλ°μ€ν¬λ¦½νΈ μΉ νμ€μ μ μ

---

[π](#π-quick-menu)