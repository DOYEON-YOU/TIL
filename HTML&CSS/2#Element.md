# πμ£Όμ μ²λ¦¬νκΈ°

`Ctrl + /` λ¨μΆν€λ₯Ό μ¬μ©ν  μ μλ€.

<br>

## π HTML

> <!β β!>

## π CSS

> /* */

## π JavaScript

> //

<br>

---
<br>

μμ μμ μμΉνλ κΈμλ Inner TextλΌκ³  ν΅μΉ­νλ€.

ex) <p>`InnerText`</p>

<br>

# π **νΉμ  μμμ κ³΅ν΅ μμμ μ λ¦¬**

<br>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Step02_img.html</title>
    <style>
        /* id μμ±μΌλ‘ μ νν  λλ μ νμλ₯Ό #μΌλ‘ μμνλ€. */
        #one{ /* id="one"μΈ μμμ μ μ©ν  css */
            color: red;

        }
        .my-class{
            font-style: italic;
        }
        .img{
            width: 200px;
            height: 200px;
        }
    </style>
</head>
<body>
    <h1>μ΄λ―Έμ§μλλ€.</h1>
    <!--
        img μμμ src μμ±μ κ°μΌλ‘λ λ‘λ©ν  μ΄λ―Έμ§κ° μμΉν κ²½λ‘λ₯Ό μ μ΄λμΌλ©΄
        μΉλΈλΌμ°μ κ° ν΄λΉ κ²½λ‘λ₯Ό μ°Ύμμ μ΄λ―Έμ§ λ°μ΄ν°λ₯Ό λ°μμμ νλ©΄μμ νμν΄ μ€λ€.
        alt μμ±μ κ°μΌλ‘λ μ΄λ―Έμ§μ μμΈν μ€λͺμ μ μΌλ©΄ λλ€.

        img μμλ μΈλΌμΈ μμμ΄κΈ° λλ¬Έμ κ°ν(μ€λ°κΏ)μ λ°λ‘ ν΄μ£Όμ§ μμΌλ©΄ νμ€μ νκΈ°λλ€.
        alt μμ±μλ μ¬μ§μ μμΈν μ€λͺμ λ£μ μ μλ€. (μκ°μ₯μ μΈμκ² λμμ΄ λλ€.)
    -->
    <img src="./images/kim1.png" alt="κΉκ΅¬λΌκ° νμ±κΈ°λ₯Ό λ€κ³  μλ μ΄λ―Έμ§">
    <br>
    <img src="http://pics.gmarket.co.kr/pc/single/kr/common/image__logo.png"
    alt="Gmarket λ‘κ³ ">
    <!--
        μμ±μ μμλ³λ‘ κ³΅ν΅μ μΌλ‘ κ°μ§ μ μλ μμ±λ μκ³ 
        νΉμ  μμλ§ κ°μ§ μ μλ μμ±λ μλ€.
    -->
    <p id="one">p μμ</p>
    <div id="two" class="my-class">div μμ</div>
    <h3 id="three" class="my-class">h3 μμ</h3>
    <img src="images/1.jpg" width="200" height="200">
    <img src="images/2.jpg" width="200" height="200">
    <img src="images/3.jpg" width="200" height="200">
    <br>
    <!-- classλ‘ νλμ κ·Έλ£Ή νμμΌλ‘ λ¬Άμ΄ cssλ₯Ό μ μ©νλ€.
    CSS μ νμλ₯Ό μ¬μ©ν΄ κ³ μΉ  μ¬ν­μ κ³ μ³μ£Όλ©΄ class λ΄μ λͺ¨λ  μ¬μ§μ΄
    λ³κ²½λκΈ° λλ¬Έμ μ¬μ©νκΈ° νΈνλ€.-->
    <img src="images/1.jpg" class="img">
    <img src="images/2.jpg" class="img">
    <img src="images/3.jpg" class="img">
    <br>
    <!--cssλ₯Ό μμμ μμ±μΌλ‘ μ§μ  μμ±ν  μ μλ€.
        μ΄λ¬ν CSSλ₯Ό Inline CSSλΌκ³  νλ€. 
        μ μ°μ§ μμ.-->
    <img src="images/1.jpg" style="width:200px; height:200px;">
    <img src="images/2.jpg" style="width:200px; height:200px;">
    <img src="images/3.jpg" style="width:200px; height:200px;">
 
    -->
</body>
</html>
```

<br>

λ¨ src, alt, width, height μ κ°μ μμ±μ h1μ΄λ pμ κ°μ μμμ μλ ₯ν΄λ μ  μ­ν μ νμ§ λͺ» νλ€.

`μμ±λͺ=βμμ±κ°β` νμμ κ°μ§ μμ±μ `src, alt, class, id` λ±μ΄ μλ€.

μ¦, imgλΌλ νΉμ  μμλ§μ΄ κ°μ§ μ μλ `**νΉμ  μμ±**`μ΄λ€.

EX)

<br>


```html
<img src="images/μ¬μ§.jpg" alt="μ¬μ§" class="img">
```

<br>

λ°λ©΄ κ³΅ν΅ μμ±μ, μ΄λ€ μμμ΄λ  idμ class, title, style, dataμ κ°μ μμ±μ κ°μ§ μ μλ€. 

<br>

---

<br>

## π id

μμμ μμλ‘ idλ₯Ό λΆμ¬ν  μ μλ€. (idκ° μ¬λ¬ κ°μΌ κ²½μ°, idλ κ²ΉμΉμ§ μμμΌ νλ€.)

νΉμ  idλ₯Ό κ°μ§κ³  μλ μμμλ§ CSS μ μ©μ νκΈ° μ©μ΄νλ©°, idλ₯Ό μ νν΄ CSSλ₯Ό μ μ©νκΈ° μν΄μλ `#idλͺ` μ νμμΌλ‘ μ μ©νλ€.

oneμ΄λΌλ idκ° μλ€κ³  κ°μ ν΄ λ³΄μ.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>id</title>
    <style>
        ***#one{ 
            color: red;
			font-size: 50px;
			font-style: italic;
        }***
    </style>
</head>
<body>
    <div id="one">
        μλνμΈμ.
    </div>
</body>
</html>
```

<br>

![Untitled](https://ifh.cc/g/Yh6F1v.png)

<br>

μμ idλΌλ κ³΅ν΅ μμ±μΌλ‘ μΈν΄ oneμ΄λΌλ idλ₯Ό κ°μ§κ³  μλ μμλ₯Ό κ²°κ³Όλ¬Όλ‘ λμΆν΄ λ³΄μμ λ, λΉ¨κ°μμΈ 50px κΈμμ μ΄νλ¦­μ²΄κ° μ μ©λμ΄ μλ κ²°κ³Όκ° λμ¨λ€.

<br>

---

<br>

## π class

μμλ€μ νλμ κ·Έλ£ΉμΌλ‘ λ¬Άκ³  μΆμ λ μ¬μ©νλ€. (κ·Έλ£ΉμΌλ‘ λ¬Άλ κ²μ΄κΈ°μ κ²Ήμ³λ λλ€.)

νΉμ  κ·Έλ£Ήμ λ¬ΆμΈ μμμλ§ CSS μ μ©μ νκΈ° μ©μ΄νκ³ , νΉμ  classλ₯Ό μ ννμ¬ CSSμ μ μ©νκΈ° μν΄μλ `.classλͺ` μ νμμΌλ‘ μ μ©νλ€.

my-class λΌλ classλ₯Ό λ§λ€μ΄ μ€νν΄ λ³΄μ.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>id</title>
    <style>
        #one{ 
            color: red;
			font-size: 50px;
			font-style: italic;
        }
        .my-class{
            color: gray;
            font-size: 100px;
            font-weight: bolder;
        }
    </style>
</head>
<body>
    <div class="my-class">HELLO</div>
    <div class="my-class">WORLD</div>
    <div id="one">WELCOME!</div>
</body>
</html>
```

![Untitled](https://ifh.cc/g/NW8Bjg.png)

id, classλ₯Ό λ λ€ μ¬μ©νμ λ idμ classλΌλ κ³΅ν΅ μμ±μΌλ‘ μΈν΄ oneμ΄λΌλ idλ₯Ό κ°μ§κ³  μλ WELCOMEμ΄λΌλ κΈμ μμλ₯Ό κ²°κ³Όλ¬Όλ‘ λμΆν΄ λ³΄μμ λ, λΉ¨κ°μμΈ 50px κΈμμ μ΄νλ¦­μ²΄κ° μ μ©λμ΄ μλ κ²°κ³Όκ° λμ€κ³ , my-classλΌλ classλ₯Ό κ°μ§κ³  μλ HELLO WORLDλΌλ κΈμ μμλ₯Ό κ²°κ³Όλ¬Όλ‘ λμΆν΄ λ³΄μμ λ, νμμΈ 100px κΈμμ κ΅΅μ ν¨κ³Όκ° μ μ©λμ΄ μλ κ²°κ³Όκ° λμ¨λ€.

<br>

---

<br>

## π class/id/νμΌλͺ μ΄λ¦ μ§κΈ°

   
`λμ μ΄λ―Έμ§` λΌλ λ»μ μ΄λ¦μ λΆμ΄κ³  μΆλ€λ©΄

`My Image`λΌλ μΈμ΄λ₯Ό νννλ λ°μλ μ¬λ¬ κ°μ§μ μΌμ΄μ€κ° λλλ€.

| myImage | camel case | μΉ΄λ© μΌμ΄μ€ |
| --- | --- | --- |
| my-image | kebab case | μΌλ°₯ μΌμ΄μ€ |
| my_image | snake case | μ€λ€μ΄ν¬ μΌμ΄μ€ |

λ€λ§, κ΄λ‘κ° λͺ¨λ λ€λ₯΄κΈ° λλ¬Έμ κ΄λ‘λ₯Ό λ°λΌ μ£Όλ κ²μ΄ μ’μΌλ©°,

μ μ νκ² μμ΄μ μ°λ κ² μ’λ€.

μλ° μ€ν¬λ¦½νΈμμλ kebab caseλ₯Ό μ¬μ©νλ©΄ μ λλ€.

`class μμ±μ μ΄λ¦`μ μ§μ λλ `kebab case`λ₯Ό μ νΈνκ³ ,

`id μμ±μ μ΄λ¦`μ μ§μ λλ `camel case`λ₯Ό μ νΈνλ€.

`νμΌλͺμ μ΄λ¦`μ μ§μ λλ `snake case`λ₯Ό μ νΈνλ€.

CSSμ font-style, font-height λ± μμ±μ λͺ¨λ kebab caseλ‘ λμ΄ μλ€.

<br>

---

# π Block Element (λΈλ‘ μμ)

<br>

> **div, h1, h2, h3, h4, h5, h6, p, ul, li**
> 

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Step03_blockElement.html</title>
    <style>
        /* μ μ λ§λ€ λ μ°λ μμ±*/
        #imagePanel{
            border-color: blue;
            border-width: 2px;
            border-style: solid;
        }
    </style>
</head>
<body>
    <div>div μμλ μ£Όλ‘ λ¬Έλ¨μ λνλΌ λ μ¬μ©ν©λλ€.</div>
    <div>div μμλ μ£Όλ‘ λ€λ₯Έ μμλ₯Ό ν¬ν¨νλ μ©λλ‘ μ¬μ©ν©λλ€.</div>
    <div>div μμλ ν­μ 100% μ°¨μ§νλ block elementμλλ€.</div>
    <div id="imagePanel">
        <img src="images/kim1.png">
        <img src="images/rabbit_1.png">
    </div>
</body>
</html>
```

![Untitled](https://ifh.cc/g/J7vPmG.png)

μμ κ°μ΄ div μμλ μΉ λΈλΌμ°μ μ ν­μ 100% μ°¨μ§νλ©°, λμ΄λ νμνλ§νΌλ§ μ°¨μ§νλ Block μμμ΄λ€. `<div id=βimagePanel></div>` μμ μ΄λ―Έμ§ λ μ₯μ΄ λ€μ΄κ° μλ―μ΄, div μμλ μ£Όλ‘ λ€λ₯Έ μμλ₯Ό ν¬ν¨νλ μ©λλ‘ μ¬μ©λλ€. id μμ±μ μ΄μ©ν΄ μ μ λ§λ€μ΄μ κ°λ‘ν­μ΄ μΉ λΈλΌμ°μ μ 100%λΌλ κ²μ μ¦λͺνκ³  μλ€. divκ° κΈ°λ³Έμ μΌλ‘ κ°μ§κ³  μλ μμ±μ `display: block; margin: 0px; padding: 0px;` μ΄λ€.

<br>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Step03_blockElement2.html</title>
</head>
<body>
    <!-- hμμλ€μ λ°λ‘ CSSλ₯Ό μ μ©ν΄ μ£Όμ§ μμλ κΈ°λ³Έμ μΌλ‘ κ°μ§κ³  μλ CSSκ° μλ€. -->
    <h1>λμ λͺ©</h1>
    <h2>μ€μ λͺ©</h2>
    <h3>μμ λͺ©</h3>
    <h4>hn μμλ block Elementμ΄λ€.</h4>
    <h5>h1 ~ h6κΉμ§ μλ€.</h5>
    <h6>h6</h6>

    <!-- pμμλ κΈ°λ³Έ CSSλ‘ 16pxμ κΈμ ν¬κΈ°λ₯Ό κ°μ§κ³  μκ³ , λ§μ§μ΄ 1emλ§νΌ μ μ©λμ΄ μλ€. -->
    <p>p μμλ μ£Όλ‘ λ¬Έμμ΄ λ¨λ½(paragraph)λ₯Ό κ΅¬μ±ν  λ μ¬μ©νλ€.</p>
    <p>λν΄λ¬Όκ³Ό λ°±λμ°μ΄ λ§λ₯΄κ³  λ³λλ‘</p>
    <p>νλλμ΄ λ³΄μ°νμ¬ μ°λ¦¬ λλΌ λ§μΈ</p>
</body>
</html>
```

![Untitled](https://ifh.cc/g/TN3MqW.png)

hμμλ μ£Όλ‘ `μ λͺ©μ ννν  λ μ°λ μμ`μ΄κΈ° λλ¬Έμ, κΈ°λ³Έμ μΌλ‘ κ°μ§κ³  μλ CSSκ° μλ€. h1 μμμ κΈ°λ³Έ CSSλ₯Ό μ΄ν΄ λ³΄μ.

![Untitled](https://ifh.cc/g/dRNVCc.png)

μ΄μ κ°μ΄ κΈ°λ³Έμ μΌλ‘ `margin-top`, `margin-bottom`, `font-weight`, `font-size` μ κ°μ΄ μ€μ λμ΄ μλ κ²μ΄ λ³΄μΈλ€. 

<br>

---

# π Inline Element (μΈλΌμΈ μμ)

> **span, b, strong, i, em, a**
> 

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Step04_inlineElement.html</title>
    <style>
        .color-red{
            color:red;
            font-weight: bold;
            font-style: italic;
            /* top = block-start 
               bottom = block-end */
        }
    </style>
</head>
<body>
    <h1>inline μμμ λν΄ μμλ³΄μ.</h1>
    <!-- spanμ μ¬μ©νλ κ²κ³Ό κ·Έλ₯ μμ±νλ κ²κ³Ό λ³΄μ¬μ§λ κ²μ μ°¨μ΄λ μμ§λ§
				"λ" μ΄λΌλ κΈμμλ§ μμμ λ£κ±°λ λμμΈμ λ£κ³  μΆμ λμ μ¬μ©μ ν΄μΌ νλ€.
				λ¬Έμ₯μ νλ¦μ μν₯μ μ£Όμ§ μκ³  λμμΈμ λ³κ²½ν  μ μλ€. -->

    <span>νλ</span><span class="color-red">λ</span><span>μ</span>
    <br>
    νλλμ
    <p>span μμλ <span class="color-red">inline</span> μμμ΄λ€.</p>

    <h2>κΈ°λ³Έ μ€νμΌμ κ°μ§κ³  μλ μΈλΌμΈ μμ</h2>
    <!-- b μμλ λ¨μν κ΅΅μ κΈμ¨μ΄λ€. -->
    <p> λν΄λ¬Όκ³Ό <b>λ°±λμ°μ΄</b> λ§λ₯΄κ³  λ³λλ‘</p>
    <!-- strong μμλ κ΅΅μ κΈμ¨ + κ°μ‘° μ μλ―Έλ κ°μ§κ³  μλ€. -->
    <p> νλλμ΄ <strong>λ³΄μ°νμ¬</strong> μ°λ¦¬λλΌ λ§μΈ</p>

    <!-- i μμλ λ¨μν μ΄νλ¦­μ²΄ -->
    <p> λ¬΄κΆν <i>μΌμ²λ¦¬</i> νλ €κ°μ°</p>
    <!-- em μμλ μ΄νλ¦­μ²΄ + κ°μ‘° μ μλ―Έλ κ°μ§κ³  μλ€. -->
    <p> λν μ¬λ <em>λνμΌλ‘</em> κΈΈμ΄ λ³΄μ νμΈ</p>

    <!-- padding: μμͺ½ μ¬λ°± / border: κ²½κ³μ  / margin: μΈλΆ μ¬λ°± -->

</body>
</html>
```

![Untitled](https://ifh.cc/g/9W2Tsy.png)

| i | μ΄νλ¦­μ²΄ |
| --- | --- |
| em | μ΄νλ¦­μ²΄ + κ°μ‘° |
| b | κ΅΅μ κΈμ¨ |
| em | κ΅΅μ κΈμ¨ + κ°μ‘° |

λ³΄μ¬μ§λ μ°¨μ΄λ μμ§λ§, μ€ν¬λ¦° λ¦¬λ(Screen Reader)μμ κ°μ‘°μ μλ―Έκ° μλ μμλ κ°μ‘°ν΄μ μ½μ΄μ€λ€. `νμν λ§νΌλ§ κ³΅κ°μ μ°¨μ§`νκ³ , κΈ°λ³Έ CSSκ° μ μ©λμ΄ μμ§ μκΈ° λλ¬Έμ λμμΈμ μν₯μ μ£Όμ§ μλλ€. spanμ λͺ¨λ μν°λ‘ λλμ΄ μ€λ°κΏμ ν  μμ μΉ λΈλΌμ°μ μλ `λμ΄μ°κΈ°κ° λμ΄ νμ`λλ€.

κ·Έ μμλ₯Ό λ³΄μ.

<br>

### π **span νμ© μμ**

<br>

**span μμ± μ€λ°κΏμΌλ‘ μμ±**

<br>

```html
<body>
    <span>HELLO</span>
    <span>MY</span>
    <span>WORLD</span>
</body>
```

κ²°κ³Ό

```html
HELLO MY WORLD
```

<br>

**span μμ± μ€λ°κΏ μμ΄ μμ±**

<br>

```html
<body>
    <span>HELLO</span><span>MY</span><span>WORLD</span>
</body>
```

κ²°κ³Ό

```html
HELLOMYWORLD
```

---

# π μμΉμ λν μ΄ν΄

<br>

![Untitled](https://ifh.cc/g/YsTNPw.png)

`margin`(μΈλΆ μ¬λ°±), `padding`(λ΄λΆ μ¬λ°±), `border`(κ²½κ³μ ) μ κ°μ μ€μ ν΄ μ€ λ μνλ μμΉμλ§ κ°μ μ€μ ν΄ μ€ μ μλ μμΉμ΄λ€. `top / right / bottom / left` λ‘ μ΄λ£¨μ΄μ Έ μμΌλ©°, **μκ³ λ°©ν₯**μΌλ‘ μμλλ©΄ μ’λ€.

<aside>
π‘ **h1~h6κ³Ό κ°μ΄ μλμ μΌλ‘ CSSκ° μμ±λλ μμκ° μλ κ²½μ°μ, κΈ°λ³Έμ μΌλ‘ `font-size: 16px;` μ΄λ€. μ°Έκ³ νλ©΄ μ’λ€.**

</aside>

---