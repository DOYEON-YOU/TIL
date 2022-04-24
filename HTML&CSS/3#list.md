## 👍 li

li 요소는 **list(목록)의 약자**로, ul이나 ol, dl과 같은 부모 요소가 없이 사용할 수 없다. 즉, **단독 사용이 불가능**하다.  

<aside>
💡 순서가 없는 목록(unordered list) 를 정의하는 `ul` 요소나

순서가 있는 목록(ordered list) 를 정의하는 `ol` 요소

에서 목록의 각 내용을 정의한다.

</aside>

순서가 없는 목록이나 메뉴 목록에서는 `검정색의 작은 원(bullet)` 모양으로 표현되며, 순서가 있는 리스트에서는 `아라비아 숫자나 알파벳`으로 표현 된다.

**✔ 예시** 

```html
1. 순서가 없는 목록
<ul>
	<li></li>
</ul>

2. 순서가 있는 목록
<ol>
	<li></li>
</ol>
```

<br>

---

<br>

## 👍 ul

<br>

> CSS 기본값

Block Element
margin top & bottom: 1em;
padding left: 40px
> 

⛏ Code

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
    <h1>순서 없는 목록(unordered list) ul 요소</h1>

    <h2>친구 목록입니다</h2>
    김구라<br>
    해골<br>
    원숭이

    <p>
        어떤 목록을 나타낼때 문자열을 단순히 나열하는 게 아니고
        아래와 같이 구조화를 해서 나열해야 한다.
    </p>

    <h2>친구 목록입니다</h2>
    <ul>
        <li>김구라</li>
        <li>해골</li>
        <li>원숭이</li>
        
    </ul>
    <p>
        ul은 block 요소이며 위 아래 마진과 왼쪽 패딩을 가지고 있다.
    </p>
</body>
</html>
```

🎨 Result

![Untitled](https://ifh.cc/g/1GH75X.png)

<br>

---

<br>

ul 요소를 적용하지 않고 <br> 요소만을 이용하여 목록을 나누었을 때에는 구조화가 되어 있지 않아 따로 목록처럼 보이지 않을 정도로 단순하게 나열이 되어 있다. 하지만 ul 요소를 적용하였을 때에는 위와 같이 구조화 되어 보기 좋게 목록이 나열되어 있는 것을 볼 수 있다.

위 ul 요소는 `글머리`로 목록을 보기 좋게 나열해 주는 역할을 한다.

ul은 **블록(Block) 요소**이며, **위 아래 마진과 왼쪽 패딩**을 가지고 있다고 하는데 직접 확인해 보자.

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

검사 창(F12)을 통해 ul의 CSS 기본값을 확인해 본 결과,  `display: block;` 라는 속성을 가지고 있어 블록 요소라는 것을 알 수 있다. `margin` 을 살펴보면 `top과 bottom은 margin: 1em;`인 것을 볼 수 있고, `right와 left는 margin: 0px;` 인 것을 볼 수 있다, `padding-left: 40px;` 인 것을 보아, 왼쪽의 패딩은 40px만큼 적용이 되었다는 것을 알 수 있다.

<aside>
💡 ***margin/padding-block-start = margin/padding-top
margin/padding-block-end = margin/padding-bottom
margin/padding-inline-start = margin/padding-left
margin/padding-inline-end = margin/padding-right***

</aside>

<br>

---

<br>

## 👍 ol

> CSS 기본값

Block Element
margin top & bottom: 1em;
padding left: 40px
> 

⛏ Code

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
    <h1>순서 있는 목록 (ordered list) ol 요소</h1>
    <h2>할 일 목록입니다.</h2>
    <ol>
        <li>HTML 공부하기</li>
        <li>CSS 공부하기</li>
        <li>JavaScript 공부하기</li>
    </ol>
</body>
</html>
```

🎨 Result

![Untitled](https://ifh.cc/g/WQnmKD.png)

<br>

---

<br>

ol 요소는 순서가 있는 리스트(list)를 정의할 때 사용한다. 순서가 있다는 말은 나열해 놓은 리스트들이 **각자 순서에 맞게 그에 맞는 번호가 부여**된다는 말과 같다.

위 ol 요소는 `숫자`로 목록을 순서대로 나열해 주는 역할을 한다. 

ul은 **블록(Block) 요소**이며, **위 아래 마진과 왼쪽 패딩**을 가지고 있다고 했는데

ol 요소는 어떨지 직접 확인해 보자.

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

검사 창(F12)을 통해 ol의 CSS 기본값을 확인해 본 결과, **ul 요소와 똑같은 기본값**이 나왔다. 

`display: block;` 라는 속성으로 블록 요소라는 것을 알 수 있고.  `top과 bottom은 margin: 1em;`인 것을 볼 수 있으며, `right와 left는 margin: 0px;` 인 것을 볼 수 있다. `padding-left: 40px;` 처럼 패딩이 40px 적용 되어 있는 것도 똑같다.

<br>

---

<br>

## 👍 dl

> CSS 기본값

Block Element
margin top & margin bottom: 1em;
> 

⛏ Code

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
    <h1>정의형 목록 (definition list) dl 요소</h1>
    <dl>
        <dt>
            제목
        </dt>
        <dd>
            자세한 내용...
        </dd>

        <br>

        <dt>
            HTML
        </dt>
        <dd>
            Hyper Text Markup Language 의 약자이다.
        </dd>

        <br>

        <dt>
            CSS
        </dt>
        <dd>
            Design적인 요소를 결정한다.
        </dd>

        <br>

        <dt>
            Javascript
        </dt>
        <dd>
            language 적인 요소를 담당한다.
        </dd>
    </dl>
</body>
</html>
```

🎨 Result

![Untitled](https://ifh.cc/g/W9wxkv.png)

<br>

---

<br>

dl 요소는 앞서 필기한 ol, ul 요소와는 조금 다르다. dl 요소는 정의형 목록이라는 뜻을 가진 Definition list의 약자로, 용어와 그에 대한 설명을 리스트 형식으로 정의할 때 사용한다. 

dl 요소는 용어나 이름을 나타내는 `dt` 요소와, 해당 용어에 대한 설명을 나타내는 `dd` 요소로 구성된다. ul과 ol 요소와 다른 유형의 리스트 요소이기 때문에 CSS 기본값도 다를 것이다.

살펴보자.

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

margin과 padding이 모두 있었던 ol과 ul 요소와는 다르게, dl 요소는 padding이 없다. 이외에 margin-top 의 값, margin-bottom 의 값은 1em으로 같고, 블록 요소인 점도 같다.