## π li

li μμλ **list(λͺ©λ‘)μ μ½μ**λ‘, ulμ΄λ ol, dlκ³Ό κ°μ λΆλͺ¨ μμκ° μμ΄ μ¬μ©ν  μ μλ€. μ¦, **λ¨λ μ¬μ©μ΄ λΆκ°λ₯**νλ€.  

<aside>
π‘ μμκ° μλ λͺ©λ‘(unordered list) λ₯Ό μ μνλ `ul` μμλ

μμκ° μλ λͺ©λ‘(ordered list) λ₯Ό μ μνλ `ol` μμ

μμ λͺ©λ‘μ κ° λ΄μ©μ μ μνλ€.

</aside>

μμκ° μλ λͺ©λ‘μ΄λ λ©λ΄ λͺ©λ‘μμλ `κ²μ μμ μμ μ(bullet)` λͺ¨μμΌλ‘ ννλλ©°, μμκ° μλ λ¦¬μ€νΈμμλ `μλΌλΉμ μ«μλ μνλ²³`μΌλ‘ νν λλ€.

**β μμ** 

```html
1. μμκ° μλ λͺ©λ‘
<ul>
	<li></li>
</ul>

2. μμκ° μλ λͺ©λ‘
<ol>
	<li></li>
</ol>
```

<br>

---

<br>

## π ul

<br>

> CSS κΈ°λ³Έκ°

Block Element
margin top & bottom: 1em;
padding left: 40px
> 

β Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Step05_ul.html</title>
</head>
<body>
    <h1>μμ μλ λͺ©λ‘(unordered list) ul μμ</h1>

    <h2>μΉκ΅¬ λͺ©λ‘μλλ€</h2>
    κΉκ΅¬λΌ<br>
    ν΄κ³¨<br>
    μμ­μ΄

    <p>
        μ΄λ€ λͺ©λ‘μ λνλΌλ λ¬Έμμ΄μ λ¨μν λμ΄νλ κ² μλκ³ 
        μλμ κ°μ΄ κ΅¬μ‘°νλ₯Ό ν΄μ λμ΄ν΄μΌ νλ€.
    </p>

    <h2>μΉκ΅¬ λͺ©λ‘μλλ€</h2>
    <ul>
        <li>κΉκ΅¬λΌ</li>
        <li>ν΄κ³¨</li>
        <li>μμ­μ΄</li>
        
    </ul>
    <p>
        ulμ block μμμ΄λ©° μ μλ λ§μ§κ³Ό μΌμͺ½ ν¨λ©μ κ°μ§κ³  μλ€.
    </p>
</body>
</html>
```

π¨ Result

![Untitled](https://ifh.cc/g/1GH75X.png)

<br>

---

<br>

ul μμλ₯Ό μ μ©νμ§ μκ³  <br> μμλ§μ μ΄μ©νμ¬ λͺ©λ‘μ λλμμ λμλ κ΅¬μ‘°νκ° λμ΄ μμ§ μμ λ°λ‘ λͺ©λ‘μ²λΌ λ³΄μ΄μ§ μμ μ λλ‘ λ¨μνκ² λμ΄μ΄ λμ΄ μλ€. νμ§λ§ ul μμλ₯Ό μ μ©νμμ λμλ μμ κ°μ΄ κ΅¬μ‘°ν λμ΄ λ³΄κΈ° μ’κ² λͺ©λ‘μ΄ λμ΄λμ΄ μλ κ²μ λ³Ό μ μλ€.

μ ul μμλ `κΈλ¨Έλ¦¬`λ‘ λͺ©λ‘μ λ³΄κΈ° μ’κ² λμ΄ν΄ μ£Όλ μ­ν μ νλ€.

ulμ **λΈλ‘(Block) μμ**μ΄λ©°, **μ μλ λ§μ§κ³Ό μΌμͺ½ ν¨λ©**μ κ°μ§κ³  μλ€κ³  νλλ° μ§μ  νμΈν΄ λ³΄μ.

![Untitled](https://ifh.cc/g/OTca8J.png)

```html
ul {
  display: block;
  list-style-type: disc;
  margin-top: 1em;
  margin-bottom: 1em;
  margin-left: 0;
  margin-right: 0;
  padding-left: 40px;
}
```

κ²μ¬ μ°½(F12)μ ν΅ν΄ ulμ CSS κΈ°λ³Έκ°μ νμΈν΄ λ³Έ κ²°κ³Ό,  `display: block;` λΌλ μμ±μ κ°μ§κ³  μμ΄ λΈλ‘ μμλΌλ κ²μ μ μ μλ€. `margin` μ μ΄ν΄λ³΄λ©΄ `topκ³Ό bottomμ margin: 1em;`μΈ κ²μ λ³Ό μ μκ³ , `rightμ leftλ margin: 0px;` μΈ κ²μ λ³Ό μ μλ€, `padding-left: 40px;` μΈ κ²μ λ³΄μ, μΌμͺ½μ ν¨λ©μ 40pxλ§νΌ μ μ©μ΄ λμλ€λ κ²μ μ μ μλ€.

<aside>
π‘ ***margin/padding-block-start = margin/padding-top
margin/padding-block-end = margin/padding-bottom
margin/padding-inline-start = margin/padding-left
margin/padding-inline-end = margin/padding-right***

</aside>

<br>

---

<br>

## π ol

> CSS κΈ°λ³Έκ°

Block Element
margin top & bottom: 1em;
padding left: 40px
> 

β Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Step06_ol.html</title>
</head>
<body>
    <h1>μμ μλ λͺ©λ‘ (ordered list) ol μμ</h1>
    <h2>ν  μΌ λͺ©λ‘μλλ€.</h2>
    <ol>
        <li>HTML κ³΅λΆνκΈ°</li>
        <li>CSS κ³΅λΆνκΈ°</li>
        <li>JavaScript κ³΅λΆνκΈ°</li>
    </ol>
</body>
</html>
```

π¨ Result

![Untitled](https://ifh.cc/g/WQnmKD.png)

<br>

---

<br>

ol μμλ μμκ° μλ λ¦¬μ€νΈ(list)λ₯Ό μ μν  λ μ¬μ©νλ€. μμκ° μλ€λ λ§μ λμ΄ν΄ λμ λ¦¬μ€νΈλ€μ΄ **κ°μ μμμ λ§κ² κ·Έμ λ§λ λ²νΈκ° λΆμ¬**λλ€λ λ§κ³Ό κ°λ€.

μ ol μμλ `μ«μ`λ‘ λͺ©λ‘μ μμλλ‘ λμ΄ν΄ μ£Όλ μ­ν μ νλ€. 

ulμ **λΈλ‘(Block) μμ**μ΄λ©°, **μ μλ λ§μ§κ³Ό μΌμͺ½ ν¨λ©**μ κ°μ§κ³  μλ€κ³  νλλ°

ol μμλ μ΄λ¨μ§ μ§μ  νμΈν΄ λ³΄μ.

![Untitled](https://ifh.cc/g/4OBR24.png)

```html
ol {
  display: block;
  list-style-type: decimal;
  margin-top: 1em;
  margin-bottom: 1em;
  margin-left: 0;
  margin-right: 0;
  padding-left: 40px;
}
```

κ²μ¬ μ°½(F12)μ ν΅ν΄ olμ CSS κΈ°λ³Έκ°μ νμΈν΄ λ³Έ κ²°κ³Ό, **ul μμμ λκ°μ κΈ°λ³Έκ°**μ΄ λμλ€. 

`display: block;` λΌλ μμ±μΌλ‘ λΈλ‘ μμλΌλ κ²μ μ μ μκ³ .  `topκ³Ό bottomμ margin: 1em;`μΈ κ²μ λ³Ό μ μμΌλ©°, `rightμ leftλ margin: 0px;` μΈ κ²μ λ³Ό μ μλ€. `padding-left: 40px;` μ²λΌ ν¨λ©μ΄ 40px μ μ© λμ΄ μλ κ²λ λκ°λ€.

<br>

---

<br>

## π dl

> CSS κΈ°λ³Έκ°

Block Element
margin top & margin bottom: 1em;
> 

β Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Step07_dl.html</title>
</head>
<body>
    <h1>μ μν λͺ©λ‘ (definition list) dl μμ</h1>
    <dl>
        <dt>
            μ λͺ©
        </dt>
        <dd>
            μμΈν λ΄μ©...
        </dd>

        <br>

        <dt>
            HTML
        </dt>
        <dd>
            Hyper Text Markup Language μ μ½μμ΄λ€.
        </dd>

        <br>

        <dt>
            CSS
        </dt>
        <dd>
            Designμ μΈ μμλ₯Ό κ²°μ νλ€.
        </dd>

        <br>

        <dt>
            Javascript
        </dt>
        <dd>
            language μ μΈ μμλ₯Ό λ΄λΉνλ€.
        </dd>
    </dl>
</body>
</html>
```

π¨ Result

![Untitled](https://ifh.cc/g/W9wxkv.png)

<br>

---

<br>

dl μμλ μμ νκΈ°ν ol, ul μμμλ μ‘°κΈ λ€λ₯΄λ€. dl μμλ μ μν λͺ©λ‘μ΄λΌλ λ»μ κ°μ§ Definition listμ μ½μλ‘, μ©μ΄μ κ·Έμ λν μ€λͺμ λ¦¬μ€νΈ νμμΌλ‘ μ μν  λ μ¬μ©νλ€. 

dl μμλ μ©μ΄λ μ΄λ¦μ λνλ΄λ `dt` μμμ, ν΄λΉ μ©μ΄μ λν μ€λͺμ λνλ΄λ `dd` μμλ‘ κ΅¬μ±λλ€. ulκ³Ό ol μμμ λ€λ₯Έ μ νμ λ¦¬μ€νΈ μμμ΄κΈ° λλ¬Έμ CSS κΈ°λ³Έκ°λ λ€λ₯Ό κ²μ΄λ€.

μ΄ν΄λ³΄μ.

![Untitled](https://ifh.cc/g/3p2KoV.png)

```html
dl {
  display: block;
  margin-top: 1em;
  margin-bottom: 1em;
  margin-left: 0;
  margin-right: 0;
}
```

marginκ³Ό paddingμ΄ λͺ¨λ μμλ olκ³Ό ul μμμλ λ€λ₯΄κ², dl μμλ paddingμ΄ μλ€. μ΄μΈμ margin-top μ κ°, margin-bottom μ κ°μ 1emμΌλ‘ κ°κ³ , λΈλ‘ μμμΈ μ λ κ°λ€.