

`✔ 웹브라우저가 해석하는 문자열의 형식`

> **`HTML`**: 정보, DATA, 약간의 디자인적인 요소이다. **뼈대**와 같은 역할.
<br>
> **`CSS`**: 디자인적인 요소를 원하는대로 변경할 수 있다. **살**과 같은 역할.
<br>
> **`JAVAScript`**: 웹브라우저의 동작을 프로그래머가 의도하는대로 설정할 수 있다. **머리**와 같은 역할.

<br>

---

<br>

# 👍 HTML 구조에 대한 이해

<br>

```html
<html>
<!DOCTYPE html><!-- html5 형식의 문자열 이라고 웹브라우저에 알리는 선언부이다. -->
<html lang="ko"><!-- html 요소는 head 요소와 body 요소로 구성되어 있다.-->
<head>
    <!-- head 안에는 여러가지 설정 정보가 들어간다. -->
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- title 요소 안에는 웹페이지의 제목을 적는다(탭의 제목) -->
    <title>제목</title>
</head>
<body><!-- body 요소 안에는 웹브라우저에 표시할 내용을 주로 작성한다 -->
<!-- 위 코드에서 보이는 것처럼 h1은 대제목, h2는 중제목, h3는 소제목, p는 단락, div는 문단, i는 이태릭체로 나타나고 있다. -->
    <h1>안녕하세요</h1>
    <h2>중제목입니다</h2>
    <h3>소제목입니다</h3>
    <p>단락입니다</p>
    <div>문단입니다</div>
    <i>이태릭체입니다</i><br>
    <img src="<http://pics.gmarket.co.kr/pc/single/kr/common/image__logo.png>" width="240" height="113" alt="G마켓" class="image__logo">
    <!-- 이미지의 위치가 어디에 있는지(인터넷에 올려져 있다면 링크 첨부, 컴퓨터 폴더에 있다면 위치 작성) 알려주기 위함이다.
    예제로 지마켓 로고를 가져왔다.-->
</body>
</html>

```

<br>

---

<br>

`- br이 작성되지 않았을 때 -`

![Untitled](https://ifh.cc/g/Dqha9b.png)

<br>

---

<br>

`- br이 작성되었을 때 -`

![Untitled](https://ifh.cc/g/5XX37w.png)

<br>

---

<br>

이 둘의 차이는 확연하다. 지마켓 로고가 밑으로 가느냐, 아니면 보기 다소 불편한 위치에

있느냐인데 이 둘의 차이는 br이 있느냐 없느냐에 따라 갈린다.

`✔ br은 줄바꿈 요소`로, 로고가 이태릭체의 밑으로 가게끔 이태릭체 옆에

br 요소를 붙여주면 로고가 보기 좋게끔 밑으로 이동한다.

<br>

---

<br>

# 👍 요소에 대한 이해

html, head, body, meta, title, h1~h6은 모두 <code>`요소명`</code>으로 통칭된다.

✔ 블록 요소(block element) = `한 줄을 모두 차지한다. (가로폭을 100% 차지한다.)`
===> `h1~h6, p, div` 등이 포함되어 있다.

✔ 인라인 요소(inline element) = `필요한 만큼의 공간만 차지한다.`
===> `i, img, span` 등이 포함되어 있다.

<br>

---

<br>

# 👍 css에 대한 이해

<br>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Step01_hello.html</title>
    <!-- css 영역은 style 요소를 이용해서 만든다.-->
    <style>
        /* 여기는 css 영역이다. /*는 css 영역의 주석 */
        /*
            선택자(div, p, h1, etc, span...){
                css 속성: 값;
                css 속성2: 값;
                css 속성3: 값; <값을 입력한 이후 세미콜론은 무조건 필수>
      		스타일을 적용하기 위해 불러오는 모든 요소 (Element)들은 선택자 역할을 함.
            }
                - 사용할 수 있는 css 속성은 이미 정해져 있다. (마음대로 지어낼 수 없음)
                - css 속성에 적용할 값은 이미 정해진 카테고리 내에서 고르는 것도 있고,
                또는 크기나 색상같은 값은 정해진 단위에 맞춰서 원하는 값을 지정하면 된다.
        */
        h1{
            color: red;
            background-color: yellow;
        }
        p{
            color: blue;
            background-color: beige;
            font-size: 50px;
        }
    </style>
</head>
<body>
    <h1>대제목입니다.</h1>
    <p>단락입니다.</p>
</body>
</html>

```

![Untitled](https://ifh.cc/g/CdQ9Sj.png)

위 결과물을 확인해 보면 블록 요소인 h1, p로 이루어져 있어 가로폭을 100% 차지하는 것이 보인다. 따로 width, height를 설정해 주지 않으면 가로폭을 항상 100% 차지한다.

<br>

---

<br>

![Untitled](https://ifh.cc/g/jRZ6Nv.png)

위에서 보는 바와 같이, 내가 설정한 font-size는 50px이다.
font-size의 1배가 1em이라는 단위이며, 1em은 즉 50px이므로 margin-top, margin-bottom은 각각 50px이 된다.
그렇다면 2em, 3em은 각각 몇 px일까?

1em = `font-size*1` 이므로 2em = font-size*2, 즉 100px이 되고, 3em은 150px이 된다.