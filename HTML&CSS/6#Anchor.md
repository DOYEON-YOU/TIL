# π a href

a(anchor) μμλ `νμ΄νΌλ§ν¬, μ±κ°νΌ, javascript` λ±μ μνν  λ μ¬μ©νλ€. inline μμλ block μμλ₯Ό μμ μμλ‘ κ°μ§ μ μμ§λ§, **a μμλ§ μμΈμ μΌλ‘ inline μμμ΄μ§λ§ block μμλ₯Ό μμ μμλ‘ κ°μ§ μ μλ€.** aλ κ°μ₯ μ€μν `href` μμ±μ κ°μ§κ³  μλλ°, μ΄ μμ±μ νλμ νμ΄μ§μμ λ€λ₯Έ νμ΄μ§λ₯Ό μ°κ²°ν  λ μ¬μ©νλ νμ΄νΌ  λ§ν¬μΈ a νκ·Έμμ `λ§ν¬μ λͺ©μ μ§λ₯Ό κ°λ¦¬ν€λ μμ±`μ΄λ€.

<br>

- μ£Όλ‘ μ¬μ©λλ a νκ·Έμ μμ±
    
    β­ download: μ¬μ©μκ° νμ΄νΌλ§ν¬λ₯Ό ν΄λ¦­νμ λ ν΄λΉ λμμΌλ‘ μ°κ²°λμ§ μκ³  λμ  ν΄λΉ μ½νμΈ κ° λ€μ΄λ‘λλ¨μ λͺμνλ€.
    
    β­ href: λ§ν¬λ νμ΄μ§μ URLμ λͺμνλ€.
    
    β­ rel: νμ¬ λ¬Έμμ λ§ν¬λ λ¬Έμ μ¬μ΄μ μ°κ΄ κ΄κ³λ₯Ό λͺμνλ€.
    
    β­ target: λ§ν¬λ λ¬Έμλ₯Ό ν΄λ¦­νμ λ λ¬Έμκ° μ΄λ¦΄ μμΉλ₯Ό λͺμνλ€.
    
<br>

---
<br>


## π Step 1. νμ΄νΌλ§ν¬ μμ±

a νκ·Έλ‘ λ§ν¬λ νμ΄νΌ λ§ν¬λ λͺ¨λ  λΈλΌμ°μ μμ λ€μκ³Ό κ°μ κΈ°λ³Έ μ€νμΌμ κ°μ§κ² λλ€.

<aside>
π‘ μμ§ λ°©λ¬Ένμ§ μμ λ§ν¬(unvisited link) : λ°μ€, νλμ(blue)

λ°©λ¬Ένλ λ§ν¬(visited link) : λ°μ€, λ³΄λΌμ(purple)

νμ±νλ(νμ¬ λ§μ°μ€κ° ν΄λ¦­νκ³  μλ) λ§ν¬(active link) : λ°μ€, λΉ¨κ°μ(red)

</aside>

<br>

β **Code**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Step10_anchor.html</title>
</head>
<body>

    <h1>a(anchor) μμλ νμ΄νΌλ§ν¬, μ±κ°νΌ, javascript λ±μ μνν  λ μ¬μ©νλ€.</h1>
    <a href="hello.html">λλ¬λ³΄μΈμ</a> <!-- Screen Reader focusλ λ°μ μ μλ€. -->
    <a href="https://daum.net">daumμΌλ‘ μ΄λ</a>
    <a href="https://naver.com">naverλ‘ μ΄λ</a>
    <a href="hello.html">
        <img src="../JavaScript/images/kim1.png">
    </a>
    <a href="hello.html">
        <div>
            <h3>μλνμΈμ</h3>
            <p>
                <img src="images/kim1.png">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Omnis
								quis possimus, et maxime esse harum, quos pariatur quae sit nulla
								ducimus provident fugit. Possimus consectetur quasi eaque laboriosam
								dolores reprehenderit?
            </p>
        </div>
    </a>
</body>
</html>
```

<br>

π¨ **Result**

![Untitled](https://ifh.cc/g/X0QZmV.png)

κΈ°λ³Έμ μΌλ‘ `<a href=βλ§ν¬β>λλ₯΄λ©΄ μ΄λ<a>` μ νμμ κ°μ§κ³  μλ€. λ§ν¬κ° μμ±λμ΄μ§λ λΆλΆμλ μ§μ μ μΈ `μΉ νμ΄μ§ λ§ν¬`κ° λ€μ΄κ° μ μκ³ , `μ»΄ν¨ν°μ μ μ₯λμ΄ μλ html νμΌ`μ κ²½λ‘λ₯Ό μλ ₯νμ¬ ν΄λΉ htmlλ‘ λ°λ‘ μ΄λν  μ μλ€.

<br>

---

<br>

## π Step 2. λͺ©μ°¨ μ€μ 

μλ μμ λ₯Ό ν΅ν΄ a hrefλ‘ λͺ©μ°¨λ₯Ό λ§λλ λ²μ λ§μ€ν°ν΄ λ³΄μ.

<br>

β **Code**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Step10_anchor2.html</title>
    <style>
        .container{
            /* margin: auto; κΈ°λ₯μ μμ£Ό νμ©λ¨. */
            width: 768px;
            margin-left: auto;
            margin-right: auto;
            background-color: yellow;
        }
        .spacer{
            height: 200px;
            background-color: antiquewhite;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>λμΌν νμ΄μ§ λ΄μμμ μ΄λ(λͺ©μ°¨)</h1>
        <ul>
            <li><a href="#one">one</a></li>
            <li><a href="#two">two</a></li>
            <li><a href="#three">three</a></li>
        </ul>
        <div class="spacer"></div>
        <p id="one">one Lorem ipsum dolor sit amet consectetur, adipisicing elit</p>
        <div class="spacer"></div>
        <p id="two">two Lorem ipsum dolor sit amet consectetur adipisicing elit</p>
        <div class="spacer"></div>
        <p id="three">three Lorem ipsum dolor sit amet consectetur adipisicing elit</p>
        <div class="spacer"></div>
    </div>
</body>
</html>
```

<br>

π¨ **Result**

![Untitled](https://ifh.cc/g/xlJYH0.png)

μ μ½λλ₯Ό μ λ¦¬ν΄ λ³΄μ. 

**μ°μ  css λΆλΆμ μ΄ν΄λ³΄κ² λ€.**

 `spacer`λΌλ `class`λ μ€κ°μ μ¬λ°±μ μ£ΌκΈ° μν΄ μμλ‘ μ€μ λ divμ΄λ©°, μ cssλ₯Ό λ³΄λ©΄ λμ΄κ° 500px μ΄κ³  antiquewhite μμμ κ°μ§ μ¬λ°±μ΄λ€. `container`λΌλ `class`λ `bodyμ μμ μμ`λ‘, λͺ¨λ  div μμλ€μ κ°μΈμ£Όκ³  μλ€. μ¦, `ννμ΄μ§μ νμλλ λͺ¨λ  μμλ€μ λΆλͺ¨ μμ`λΌλ κ²μ΄λ€. λΈλ‘ μμμΈ divμ κ°λ‘ν­μ μ ννκΈ° μν΄μ divμ μ§μ  classλ₯Ό μ μ©ν΄ `κ°λ‘ν­μ 768pxλ‘ μ ν`νκ³  μλ κ²μ νμΈν  μ μλ€. `margin-left`μ `right`λ₯Ό `auto`λ‘ μ€μ νκ² λλ©΄ μΉ λΈλΌμ°μ μ ν¬κΈ°λ₯Ό μ€μλ€ λλ Έλ€ λ°λ³΅νμ¬λ `containerλΌλ classμ μν΄ μλ μ λ³΄λ μ€μ μ λ ¬` λμ΄ νμλλ€.

<br>

**κ·Έλ λ€λ©΄ λͺ©μ°¨λ₯Ό μ΄λ»κ² μμ±νμκΉ?**

 `λ¬Έλ¨(p)λ€μ κ°μ idλ₯Ό λΆμ¬`νκ³  `λͺ©λ‘μ λ§λ€μ΄ μ£Όλ li μμ±μ μ¬μ©`ν΄ ν΄λΉ λͺ©μ°¨μ μ΄λ¦μ κ°κ° `one, two, threeλ‘ μ€μ νμ¬ λμ΄`ν λ€ νμ΄νΌλ§ν¬λ₯Ό μμ±ν  μ μλ a μμμ p μμ, μ¦ κ°μμ idκ° μλ p μμλ‘ λ°λ‘ λμ΄κ° μ μλ `href μμ±μ μμ±`νμ¬ ν΄λΉ λͺ©μ°¨λ‘ λ°λ‘λ°λ‘ λμ΄κ° μ μκ²λ ν κ²μ΄λ€.

<br>

---

<br>

## π Step 3. anchorμ λ λ€λ₯Έ κΈ°λ₯

<br>

a μμμλ λ λ€λ₯Έ κΈ°λ₯μ΄ μλ€. λ°μ μμλ₯Ό λ³΄λ©° μ΅ν λ³΄μ.

<br>

> a href=β`javascript:alert(Hi);`β

```html
<a href="javascript:alert(Hi);">λλ¬ λ³΄μΈμ</a>
```

**a μμ±μ μ§μ  javascriptλ₯Ό μ μ©νμ¬ λλ¬ λ³΄μΈμ λΌκ³  μ νμ Έ μλ λ§ν¬λ₯Ό λλ μ λ HiλΌλ νμ μλ¦Όμ΄ λ¨κ²λ νλ€.**

<br>

---

<br>

> a href=β`tel:010-0000-0000`β

```html
<a href="tel:010-5647-9689">μ ν</a>
```

**a μμ±μ [tel:μ νλ²νΈ] λ₯Ό μλ ₯νκ² λλ©΄ λ§ν¬λ₯Ό λλ μ λ ν΄λΉ μ νλ²νΈλ‘ μ νλ₯Ό μ°κ²°ν  μ μλ€.**

<br>

---

<br>

> a href=β`malito:email@email.com`β

```html
<a href="malito:doyeonyou@naver.com">μ΄λ©μΌ</a>
```

**a μμ±μ [malito:μ΄λ©μΌ] μ μλ ₯νκ² λλ©΄ λ§ν¬λ₯Ό λλ μ λ ν΄λΉ μ΄λ©μΌλ‘ μ΄λ©μΌμ μμ±ν  μ μλ€.**