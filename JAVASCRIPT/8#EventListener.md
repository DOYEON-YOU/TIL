# 👍 addEventListener

<br>

```jsx
<button onclick="clicked()">눌러보세요.</button>
<button id="myBtn">눌러보세요.</button>
```

```jsx

    let clicked = function () {
        alert("버튼을 누르셨네요?");
    };

    document.querySelector("#myBtn").addEventListener("click", function () {
        alert("버튼을 누르셨네요?");
    });
```

위 코드를 확인해 보면, `버튼에 직접 onclick이라는 이벤트 리스너를 입력`해 적용해 준 경우도 있고, `버튼에 myBtn이라는 id를 부여해 JavaScript Area에서 이벤트 리스너를 입력`해 주어 적용한 경우도 있다. 버튼에 직접 Event Listener를 입력하는 경우에는 저번에도 다뤄 봤기 때문에, 이번에는 querySelector를 이용해 Event Listener를 입력하는 경우를 살펴보겠다.

<br>

`document.querySelector(”#id명/.class명”).addEventListener(”event”, 호출 예정 함수(){});` 의 형식으로 사용되며, clicked 함수와 addEventListener을 사용한 함수는 같은 역할을 한다. 같은 역할을 하지만 모양만 다르게 생겼다고 생각하면 이해가 쉽다.

<br>

---

<br>

## 👌 addEventListener의 활용

<br>

```jsx
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Step02_event2.html</title>
    <style>
        .box {
            width: 300px;
            height: 300px;
            border: 1px solid red;
        }
    </style>
</head>

<body>
    <div class="box" id="myDiv">box</div>
</body>
</html>
```

위 div에 `“mousedown” 이벤트가 일어났을 때 div의 배경색이 노란색`으로 바뀌고, `“mouseup” 이벤트가 일어났을 때 div의 배경색이 흰색`으로 바뀌게끔 코딩해 보자. 

<br>

```jsx
// mousedown 이벤트가 일어났을 때 div의 배경색이 노란색으로 바뀐다.
document.querySelector("#myDiv").addEventListener("mousedown", function(){
			document.querySelector("#myDiv").style.backgroundColor="yellow";
}

// mouseup 이벤트가 일어났을 때 div의 배경색이 흰색으로 바뀐다.
document.querySelector("#myDiv").addEventListener("mouseup", function(){
			document.querySelector("#myDiv").style.backgroundColor="white";
}
```

위의 div에 `“mousemove” 이벤트가 일어날 때마다 해당 마우스의 좌표를 div의 innerText로 출력`하도록 해 보자. 출력 형식은 `x좌표: x, y좌표: y`의 형식이어야 한다.

<br>

---

<br>

## 👌 X와 Y의 좌표를 나타내는 메서드

<br>

```jsx
document.querySelector("#myDiv").addEventListener("mousemove", function(e){
		let info = "x좌표 " + e.offsetX + " y좌표: " + e.offsetY;
		document.querySelector("#myDiv").innerText = info;
});
```

<br>

>가로, 세로 좌표를 제공하는 메소드를 사용하였다. 이는 클라이언트 영역 내에서의 좌표를 제공하며, 여기서 클라이언트의 영역은 현재 보이는 브라우저 화면이 기준이 된다.<br><br><br>
>**`clientX, clientY`** : 브라우저 페이지에서의 X좌표, 또는 Y좌표의 위치를 반환하나 스크롤은 무시하고 해당 페이지의 상단을 0으로 측정합니다.<br><br>
>**`offsetX, offsetY`** : 이벤트 대상 객체에서의 상대적 마우스 x좌표나 y좌표의 위치를 반환합니다.<br><br>
>**`pageX, pageY`**: 브라우저 페이지에서의 x좌표나 Y좌표의 위치를 반환합니다.<br>
>**`screenX, screenY`**: 전체 모니터 스크린에서의 x좌표나 y좌표의 위치를 반환합니다.

<br>

---

<br>

## 👌 같은 class인 div 중에서 특정 div만 변경해 보기

<br>

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Step02_event3.html</title>
    <style>
        .box {
            width: 100px;
            height: 100px;
            border: 1px solid red;
            cursor: pointer;
        }

        .box:hover {
            background-color: yellow;
        }
    </style>
</head>

<body>
    <div class="box">div1</div>
    <div class="box">div2</div>
    <div class="box">div3</div>
    <div class="box">div4</div>
    <div class="box">div5</div>
    <div class="box">div6</div>
    <div class="box">div7</div>
    <div class="box">div8</div>
    <div class="box">div9</div>
    <div class="box">div10</div>
    <script>
        for (let i = 0; 1 < divs.length; i++) {
            divs[i].addEventListener("click", function () {
                divs[i].innerText = "clicked!";
            });
        }
    </script>
</body>

</html>
```

위에 box라는 하나의 클래스로 묶인 총 10개의 div가 있다. 10개의 div 중에서 `클릭한 div의 innerText를 clicked! 로 변경`하는 프로그래밍을 해 보자.

<br>

```jsx
let divs = document.querySelectorAll(".box");

for (let i = 0; 1 < divs.length; i++) {
    divs[i].addEventListener("click", function () {
        divs[i].innerText = "clicked!";
    });
}
```

위 방법은 divs라는 하나의 변수를 만들어 box라는 class의 div 요소들을 모두 담아주어 `divs를 array type`으로 만든 뒤, for문을 이용해 `divs 배열의 인덱스가 클릭되면 innerText가 바뀌는 프로그래밍`을 한 것이다.