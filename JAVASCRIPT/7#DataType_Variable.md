```jsx
let num1 = 1234;

        function a() {
            let num2 = 1357

            function b() {
                let num3 = 2468
            };
        }
```

<br>

---

# 👍 전역 변수

함수 외부에서 선언된 변수로, `프로그램 전체에서 접근할 수 있는 변수`다. 위 예시에서 확인했을 때, `num1은 전역변수`이다. 함수 a의 입장에서 보면 num1은 그저 접근할 수 있는 하나의 외부 변수에 불과하지만, 함수 a에 들어있는 함수 b의 입장에서 보면 함수 b에서도 접근할 수 있는 변수이기에 num1은 그저 외부 변수가 아니게 되어 전역 변수가 된다. 물론 a의 입장에서도 전역 변수가 될 수 있다. 함수 a에서도 변수 num1에 접근할 수 있기 때문이다.

<br>

---

# 👍 외부 변수

전역 변수와 똑같이 `함수 외부에서 선언된 변수`로, 프로그램 전체는 아니지만 `함수 내부에서 함수 외부의 변수에 접근할 수 있는 변수`이다. 함수 내에서는 외부 변수에 접근하는 것뿐만이 아닌, **외부 변수를 수정**할 수도 있다. 위 예시에서 함수 a의 내부에는 num2라는 변수와 함수 b가 있다. 그렇다면 함수 b에서 접근할 수 있는 함수는 num2라는 변수이기 때문에, 함수 b의 입장에서 보았을 때 변수 num2는 외부 변수이다.

<br>

---

# 👍 지역 변수

`함수 내에서 선언한 변수`이며, `지역 변수는 함수 안에서만 접근`할 수 있다. 위 예시에서 지역 변수는 num3가 있다. **num3는 b라는 함수 내에서만 접근**할 수 있다. 외부에서 내부의 변수에 접근할 수는 없다.

<br>

---

# 👍 매개 변수

매개 변수를 이용하면 임의의 데이터를 함수 안에 전달할 수 있다. 밑의 예시를 확인해 보면, `let 변수명=function(매개변수){};` 의 형식으로 함수가 선언되어 있다. 함수 내부의 지역 변수에는 매개 변수를 이용한 변수가 선언 되어 있다. 매개 변수를 이용한 산술 연산이 가능하며, 매개 변수에 각 100, 200의 숫자가 들어있다고 가정하고 `showSum(100, 200)`을 호출하게 되면 `변수 result는 300이라는 값`을 가지게 되고, `console.log(100 과 200 의 합은: 300);` 이 되는 것이다. 반환(return)을 사용해 함수에 전달된 매개 변수의 합을 반환해 줄 수도 있다. 

```coffeescript
<script>
			    let showSum = function (num1, num2) {
			         let result = num1 + num2;
			         console.log(num1 + " 과 " + num2 + " 의 합은: " + result);
			    };
			
			    let getSum = function (num3, num4) {
			         let result2 = num3 + num4;
			         return result2;
			    };
</script>
```

<br>

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/551a97d5-cb2f-493e-8ead-398b095b3b16/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T192330Z&X-Amz-Expires=86400&X-Amz-Signature=5c3b6256f15717ed33f755658510654727cae4a4e051898b0c12eceb27e86724&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

더 이해하기 쉽도록 예시를 들어보겠다. 매개 변수에는 인자, 또는 인수를 넣을 수 있는데, 함수를 인자로 넣을 수도 있다.

<br>

```jsx
function useFunc(a, b) {
            console.log(a);
            b();
        }

        useFunc("권도연", function () {
            alert("함수의 인자로 전달한 함수가 호출된다.");
        });
```

useFunc라는 함수의 매개변수 a와 b에 문자열이나 함수와 같은 type을 작성하는 방법이다. 권도연이라는 문자열은 매개변수 a에 입력되고, function() 함수는 매개변수 b에 입력된다. 위 예시를 직접 코딩한다면 console 창에 "권도연"이라는 문자열이 출력될 것이고, `"함수의 인자로 전달한 함수가 호출된다" 라는 알림창`이 뜨게 될 것이다.