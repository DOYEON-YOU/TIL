# 👍주석 처리하기

`Ctrl + /` 단축키를 사용할 수 있다.

<br>

## 👌 HTML

> <!— —!>

## 👌 CSS

> /* */

## 👌 JavaScript

> //

<br>

---
<br>

요소 안에 위치하는 글자는 Inner Text라고 통칭한다.

ex) <p>`InnerText`</p>

<br>

# 👍 **특정 요소와 공통 요소의 정리**

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
        /* id 속성으로 선택할 때는 선택자를 #으로 시작한다. */
        #one{ /* id="one"인 요소에 적용할 css */
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
    <h1>이미지입니다.</h1>
    <!--
        img 요소의 src 속성의 값으로는 로딩할 이미지가 위치한 경로를 적어놓으면
        웹브라우저가 해당 경로를 찾아서 이미지 데이터를 받아와서 화면상에 표시해 준다.
        alt 속성의 값으로는 이미지의 자세한 설명을 적으면 된다.

        img 요소는 인라인 요소이기 때문에 개행(줄바꿈)을 따로 해주지 않으면 한줄에 표기된다.
        alt 속성에는 사진의 자세한 설명을 넣을 수 있다. (시각장애인에게 도움이 된다.)
    -->
    <img src="./images/kim1.png" alt="김구라가 확성기를 들고 있는 이미지">
    <br>
    <img src="http://pics.gmarket.co.kr/pc/single/kr/common/image__logo.png"
    alt="Gmarket 로고">
    <!--
        속성은 요소별로 공통적으로 가질 수 있는 속성도 있고
        특정 요소만 가질 수 있는 속성도 있다.
    -->
    <p id="one">p 요소</p>
    <div id="two" class="my-class">div 요소</div>
    <h3 id="three" class="my-class">h3 요소</h3>
    <img src="images/1.jpg" width="200" height="200">
    <img src="images/2.jpg" width="200" height="200">
    <img src="images/3.jpg" width="200" height="200">
    <br>
    <!-- class로 하나의 그룹 형식으로 묶어 css를 적용한다.
    CSS 선택자를 사용해 고칠 사항을 고쳐주면 class 내에 모든 사진이
    변경되기 때문에 사용하기 편하다.-->
    <img src="images/1.jpg" class="img">
    <img src="images/2.jpg" class="img">
    <img src="images/3.jpg" class="img">
    <br>
    <!--css를 요소의 속성으로 직접 작성할 수 있다.
        이러한 CSS를 Inline CSS라고 한다. 
        잘 쓰지 않음.-->
    <img src="images/1.jpg" style="width:200px; height:200px;">
    <img src="images/2.jpg" style="width:200px; height:200px;">
    <img src="images/3.jpg" style="width:200px; height:200px;">
 
    -->
</body>
</html>
```

<br>

단 src, alt, width, height 와 같은 속성은 h1이나 p와 같은 요소에 입력해도 제 역할을 하지 못 한다.

`속성명=”속성값”` 형식을 가진 속성은 `src, alt, class, id` 등이 있다.

즉, img라는 특정 요소만이 가질 수 있는 `**특정 속성**`이다.

EX)

<br>


```html
<img src="images/사진.jpg" alt="사진" class="img">
```

<br>

반면 공통 속성은, 어떤 요소이든 id와 class, title, style, data와 같은 속성을 가질 수 있다. 

<br>

---

<br>

## 👌 id

요소에 임의로 id를 부여할 수 있다. (id가 여러 개일 경우, id는 겹치지 않아야 한다.)

특정 id를 가지고 있는 요소에만 CSS 적용을 하기 용이하며, id를 선택해 CSS를 적용하기 위해서는 `#id명` 의 형식으로 적용한다.

one이라는 id가 있다고 가정해 보자.

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
        안녕하세요.
    </div>
</body>
</html>
```

<br>

![Untitled](https://ifh.cc/g/Yh6F1v.png)

<br>

위의 id라는 공통 속성으로 인해 one이라는 id를 가지고 있는 요소를 결과물로 도출해 보았을 때, 빨간색인 50px 글자에 이태릭체가 적용되어 있는 결과가 나온다.

<br>

---

<br>

## 👌 class

요소들을 하나의 그룹으로 묶고 싶을 때 사용한다. (그룹으로 묶는 것이기에 겹쳐도 된다.)

특정 그룹에 묶인 요소에만 CSS 적용을 하기 용이하고, 특정 class를 선택하여 CSS에 적용하기 위해서는 `.class명` 의 형식으로 적용한다.

my-class 라는 class를 만들어 실험해 보자.

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

id, class를 둘 다 사용했을 때 id와 class라는 공통 속성으로 인해 one이라는 id를 가지고 있는 WELCOME이라는 글자 요소를 결과물로 도출해 보았을 때, 빨간색인 50px 글자에 이태릭체가 적용되어 있는 결과가 나오고, my-class라는 class를 가지고 있는 HELLO WORLD라는 글자 요소를 결과물로 도출해 보았을 때, 회색인 100px 글자에 굵음 효과가 적용되어 있는 결과가 나온다.

<br>

---

<br>

## 👌 class/id/파일명 이름 짓기

   
`나의 이미지` 라는 뜻의 이름을 붙이고 싶다면

`My Image`라는 언어를 표현하는 데에도 여러 가지의 케이스가 나뉜다.

| myImage | camel case | 카멜 케이스 |
| --- | --- | --- |
| my-image | kebab case | 케밥 케이스 |
| my_image | snake case | 스네이크 케이스 |

다만, 관례가 모두 다르기 때문에 관례를 따라 주는 것이 좋으며,

적절하게 섞어서 쓰는 게 좋다.

자바 스크립트에서는 kebab case를 사용하면 안 된다.

`class 속성의 이름`을 지을 때는 `kebab case`를 선호하고,

`id 속성의 이름`을 지을 때는 `camel case`를 선호한다.

`파일명의 이름`을 지을 때는 `snake case`를 선호한다.

CSS의 font-style, font-height 등 속성은 모두 kebab case로 되어 있다.

<br>

---

# 👍 Block Element (블록 요소)

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
        /* 선을 만들 때 쓰는 속성*/
        #imagePanel{
            border-color: blue;
            border-width: 2px;
            border-style: solid;
        }
    </style>
</head>
<body>
    <div>div 요소는 주로 문단을 나타낼 때 사용합니다.</div>
    <div>div 요소는 주로 다른 요소를 포함하는 용도로 사용합니다.</div>
    <div>div 요소는 폭을 100% 차지하는 block element입니다.</div>
    <div id="imagePanel">
        <img src="images/kim1.png">
        <img src="images/rabbit_1.png">
    </div>
</body>
</html>
```

![Untitled](https://ifh.cc/g/J7vPmG.png)

위와 같이 div 요소는 웹 브라우저의 폭을 100% 차지하며, 높이는 필요한만큼만 차지하는 Block 요소이다. `<div id=”imagePanel></div>` 안의 이미지 두 장이 들어가 있듯이, div 요소는 주로 다른 요소를 포함하는 용도로 사용된다. id 속성을 이용해 선을 만들어서 가로폭이 웹 브라우저의 100%라는 것을 증명하고 있다. div가 기본적으로 가지고 있는 속성은 `display: block; margin: 0px; padding: 0px;` 이다.

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
    <!-- h요소들은 따로 CSS를 적용해 주지 않아도 기본적으로 가지고 있는 CSS가 있다. -->
    <h1>대제목</h1>
    <h2>중제목</h2>
    <h3>소제목</h3>
    <h4>hn 요소도 block Element이다.</h4>
    <h5>h1 ~ h6까지 있다.</h5>
    <h6>h6</h6>

    <!-- p요소는 기본 CSS로 16px의 글자 크기를 가지고 있고, 마진이 1em만큼 적용되어 있다. -->
    <p>p 요소는 주로 문자열 단락(paragraph)를 구성할 때 사용한다.</p>
    <p>동해물과 백두산이 마르고 닳도록</p>
    <p>하나님이 보우하사 우리 나라 만세</p>
</body>
</html>
```

![Untitled](https://ifh.cc/g/TN3MqW.png)

h요소는 주로 `제목을 표현할 때 쓰는 요소`이기 때문에, 기본적으로 가지고 있는 CSS가 있다. h1 요소의 기본 CSS를 살펴 보자.

![Untitled](https://ifh.cc/g/dRNVCc.png)

이와 같이 기본적으로 `margin-top`, `margin-bottom`, `font-weight`, `font-size` 의 값이 설정되어 있는 것이 보인다. 

<br>

---

# 👍 Inline Element (인라인 요소)

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
    <h1>inline 요소에 대해 알아보자.</h1>
    <!-- span을 사용하는 것과 그냥 작성하는 것과 보여지는 것의 차이는 없지만
				"둘" 이라는 글자에만 색상을 넣거나 디자인을 넣고 싶을 때에 사용을 해야 한다.
				문장의 흐름에 영향을 주지 않고 디자인을 변경할 수 있다. -->

    <span>하나</span><span class="color-red">둘</span><span>셋</span>
    <br>
    하나둘셋
    <p>span 요소는 <span class="color-red">inline</span> 요소이다.</p>

    <h2>기본 스타일을 가지고 있는 인라인 요소</h2>
    <!-- b 요소는 단순히 굵은 글씨이다. -->
    <p> 동해물과 <b>백두산이</b> 마르고 닳도록</p>
    <!-- strong 요소는 굵은 글씨 + 강조 의 의미도 가지고 있다. -->
    <p> 하나님이 <strong>보우하사</strong> 우리나라 만세</p>

    <!-- i 요소는 단순히 이태릭체 -->
    <p> 무궁화 <i>삼천리</i> 화려강산</p>
    <!-- em 요소는 이태릭체 + 강조 의 의미도 가지고 있다. -->
    <p> 대한 사람 <em>대한으로</em> 길이 보전하세</p>

    <!-- padding: 안쪽 여백 / border: 경계선 / margin: 외부 여백 -->

</body>
</html>
```

![Untitled](https://ifh.cc/g/9W2Tsy.png)

| i | 이태릭체 |
| --- | --- |
| em | 이태릭체 + 강조 |
| b | 굵은 글씨 |
| em | 굵은 글씨 + 강조 |

보여지는 차이는 없지만, 스크린 리더(Screen Reader)에서 강조의 의미가 있는 요소는 강조해서 읽어준다. `필요한 만큼만 공간을 차지`하고, 기본 CSS가 적용되어 있지 않기 때문에 디자인에 영향을 주지 않는다. span을 모두 엔터로 나누어 줄바꿈을 할 시에 웹 브라우저에는 `띄어쓰기가 되어 표시`된다.

그 예시를 보자.

<br>

### 👌 **span 활용 예시**

<br>

**span 속성 줄바꿈으로 작성**

<br>

```html
<body>
    <span>HELLO</span>
    <span>MY</span>
    <span>WORLD</span>
</body>
```

결과

```html
HELLO MY WORLD
```

<br>

**span 속성 줄바꿈 없이 작성**

<br>

```html
<body>
    <span>HELLO</span><span>MY</span><span>WORLD</span>
</body>
```

결과

```html
HELLOMYWORLD
```

---

# 👍 위치에 대한 이해

<br>

![Untitled](https://ifh.cc/g/YsTNPw.png)

`margin`(외부 여백), `padding`(내부 여백), `border`(경계선) 의 값을 설정해 줄 때 원하는 위치에만 값을 설정해 줄 수 있는 위치이다. `top / right / bottom / left` 로 이루어져 있으며, **시계 방향**으로 알아두면 좋다.

<aside>
💡 **h1~h6과 같이 자동적으로 CSS가 작성되는 요소가 아닌 경우엔, 기본적으로 `font-size: 16px;` 이다. 참고하면 좋다.**

</aside>

---