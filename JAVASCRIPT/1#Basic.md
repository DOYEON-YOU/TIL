# 👍 JavaScript 찍먹 해 보기

<br>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Step01_hello.html</title>
    <style>
        /* 여기는 css 영역입니다. 별표는 css 영역의 주석*/
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
    <script>
        //여기는 JavaScript 영역이다.
        console.log("하나");
    </script>
</head>
<body>
    <script>
        //여기도 JavaScript 영역이다.
        console.log("둘");
    </script>
    <h1>대제목입니다.</h1>
    <p>단락입니다.</p>
    <script>
        //여기도 JavaScript 영역이다.
        console.log("셋");
        alert("안녕하세요!");
    </script>
</body>
</html>

```

 

<br>

---

<br>

**위의 코드에서 `console.log`가 적용된 모습**

![Untitled](https://ifh.cc/g/qSFj2H.png)


<br>

---

<br>

**위의 코드에서 `alert`가 적용된 모습**

![Untitled](https://ifh.cc/g/J2AOoy.png)

---

<br>

대체적으로 `console.log`는 프로그래머가 자바스크립트가 잘 적용 되었는지 테스트할 때 사용한다.
웹브라우저에 접속해 F12를 누르면 저렇게 Console창을 확인할 수 있는데, 웹브라우저에서 바로바로 자바스크립트 언어를 입력할 수 있게끔 되어 있다.

또한, alert는 위 예제와 같이 `alert("안녕하세요!");` 라는 코드를 입력했을 때, 알림창에 내용이 도출되는 것을 볼 수 있다.

웹 브라우저에 직접 언어를 입력하면 엔터를 누르는 순간 바로 적용이 되지만, 편집기에 언어를 입력하면 저장 후 새로고침까지 끝내야 적용이 되는 모습을 볼 수 있다.

<br>

---

<br>

## 👌 **JavaScript가 들어가는 영역**

JS를 웹 브라우저에서 해석할 때에는 head 안에 작성한 내용부터 차례로 내려오며 해석한다.

<br>

---

<br>

요소 안에 위치하는 글자는 Inner Text라고 통칭한다.

> <p>`InnerText`</p>