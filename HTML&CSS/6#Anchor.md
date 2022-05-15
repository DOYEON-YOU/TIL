# 👍 a href

a(anchor) 요소는 `하이퍼링크, 책갈피, javascript` 등을 수행할 때 사용한다. inline 요소는 block 요소를 자식 요소로 가질 수 없지만, **a 요소만 예외적으로 inline 요소이지만 block 요소를 자식 요소로 가질 수 있다.** a는 가장 중요한 `href` 속성을 가지고 있는데, 이 속성은 하나의 페이지에서 다른 페이지를 연결할 때 사용하는 하이퍼  링크인 a 태그에서 `링크의 목적지를 가리키는 속성`이다.

<br>

- 주로 사용되는 a 태그의 속성
    
    ⭐ download: 사용자가 하이퍼링크를 클릭했을 때 해당 대상으로 연결되지 않고 대신 해당 콘텐츠가 다운로드됨을 명시한다.
    
    ⭐ href: 링크된 페이지의 URL을 명시한다.
    
    ⭐ rel: 현재 문서와 링크된 문서 사이의 연관 관계를 명시한다.
    
    ⭐ target: 링크된 문서를 클릭했을 때 문서가 열릴 위치를 명시한다.
    
<br>

---
<br>


## 👌 Step 1. 하이퍼링크 속성

a 태그로 링크된 하이퍼 링크는 모든 브라우저에서 다음과 같은 기본 스타일을 가지게 된다.

<aside>
💡 아직 방문하지 않은 링크(unvisited link) : 밑줄, 파란색(blue)

방문했던 링크(visited link) : 밑줄, 보라색(purple)

활성화된(현재 마우스가 클릭하고 있는) 링크(active link) : 밑줄, 빨간색(red)

</aside>

<br>

⛏ **Code**

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

    <h1>a(anchor) 요소는 하이퍼링크, 책갈피, javascript 등을 수행할 때 사용한다.</h1>
    <a href="hello.html">눌러보세요</a> <!-- Screen Reader focus도 받을 수 있다. -->
    <a href="https://daum.net">daum으로 이동</a>
    <a href="https://naver.com">naver로 이동</a>
    <a href="hello.html">
        <img src="../JavaScript/images/kim1.png">
    </a>
    <a href="hello.html">
        <div>
            <h3>안녕하세요</h3>
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

🎨 **Result**

![Untitled](https://ifh.cc/g/X0QZmV.png)

기본적으로 `<a href=”링크”>누르면 이동<a>` 의 형식을 가지고 있다. 링크가 작성되어지는 부분에는 직접적인 `웹 페이지 링크`가 들어갈 수 있고, `컴퓨터에 저장되어 있는 html 파일`의 경로를 입력하여 해당 html로 바로 이동할 수 있다.

<br>

---

<br>

## 👌 Step 2. 목차 설정

아래 예제를 통해 a href로 목차를 만드는 법을 마스터해 보자.

<br>

⛏ **Code**

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
            /* margin: auto; 기능은 자주 활용됨. */
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
        <h1>동일한 페이지 내에서의 이동(목차)</h1>
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

🎨 **Result**

![Untitled](https://ifh.cc/g/xlJYH0.png)

위 코드를 정리해 보자. 

**우선 css 부분을 살펴보겠다.**

 `spacer`라는 `class`는 중간에 여백을 주기 위해 임의로 설정된 div이며, 위 css를 보면 높이가 500px 이고 antiquewhite 색상을 가진 여백이다. `container`라는 `class`는 `body의 자식 요소`로, 모든 div 요소들을 감싸주고 있다. 즉, `홈페이지에 표시되는 모든 요소들의 부모 요소`라는 것이다. 블록 요소인 div의 가로폭을 제한하기 위해서 div에 직접 class를 적용해 `가로폭을 768px로 제한`하고 있는 것을 확인할 수 있다. `margin-left`와 `right`를 `auto`로 설정하게 되면 웹 브라우저의 크기를 줄였다 늘렸다 반복하여도 `container라는 class에 속해 있는 정보는 중앙 정렬` 되어 표시된다.

<br>

**그렇다면 목차를 어떻게 작성했을까?**

 `문단(p)들에 각자 id를 부여`하고 `목록을 만들어 주는 li 속성을 사용`해 해당 목차의 이름을 각각 `one, two, three로 설정하여 나열`한 뒤 하이퍼링크를 작성할 수 있는 a 요소에 p 요소, 즉 각자의 id가 있는 p 요소로 바로 넘어갈 수 있는 `href 속성을 작성`하여 해당 목차로 바로바로 넘어갈 수 있게끔 한 것이다.

<br>

---

<br>

## 👌 Step 3. anchor의 또 다른 기능

<br>

a 요소에는 또 다른 기능이 있다. 밑의 예시를 보며 익혀 보자.

<br>

> a href=”`javascript:alert(Hi);`”

```html
<a href="javascript:alert(Hi);">눌러 보세요</a>
```

**a 속성에 직접 javascript를 적용하여 눌러 보세요 라고 적혀져 있는 링크를 눌렀을 때 Hi라는 팝업 알림이 뜨게끔 한다.**

<br>

---

<br>

> a href=”`tel:010-0000-0000`”

```html
<a href="tel:010-5647-9689">전화</a>
```

**a 속성에 [tel:전화번호] 를 입력하게 되면 링크를 눌렀을 때 해당 전화번호로 전화를 연결할 수 있다.**

<br>

---

<br>

> a href=”`malito:email@email.com`”

```html
<a href="malito:doyeonyou@naver.com">이메일</a>
```

**a 속성에 [malito:이메일] 을 입력하게 되면 링크를 눌렀을 때 해당 이메일로 이메일을 작성할 수 있다.**