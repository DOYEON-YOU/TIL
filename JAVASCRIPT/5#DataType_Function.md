# 👍 함수를 만드는 방법

javascript에서 함수는 객체이다. 따라서 다른 객체와 마찬가지로 넘기거나 할당할 수는 없다. 함수 식별자 뒤에 `( )`를 붙이지 않는다면 `함수를 호출하지 않고 참조하는 것`이 되며, 함수는 시행되지 않는다. 함수를 실행하기 위해서는 `함수 이름 뒤에 ( )를 명시해 함수를 호출한다는 것`을 명시해 줘야 한다. 간단하게 예제를 통해 살펴보겠다.

```jsx
<script>
          console.log("javascript가 로딩 중입니다.");
          
          let f1=function(){
               console.log("f1 호출됨");
          };

          function f2(){
               console.log("f2 호출됨");
          };

</script>
```

<br>

함수를 만드는 데에는 **두 가지의 방법**이 있다.

`첫 번째는 이름이 없는 익명 함수`를 만들어 참조값을 얻어낸 후 변수에 할당하는 방법이다. 이는 실행 순서가 와야 만들어질 수 있는 함수이고, 메모리를 별로 차지하지 않아 자주 쓰인다. 정확히는 이 방식으로 하면 `호출 위치 이전에 반드시 선언`해 주어야 하는데 한 번 실행하고 나면 메모리에서 내려가기 때문에 `함수를 자주 쓰지 않는다면 메모리 관리가 편해지기 때문`이다. 익명 함수는 1회성으로 쓰이는 함수에 많이 쓰인다.

> 함수의 이름이 없기 때문에 함수를 변수에 할당해 쓰고 있다.
<br>let 변수명=function( ){ };

<br>

반면 `두 번째`의 방식은 `위치에 상관없이 선언하여 쓸 수 있는 기명 함수`다. 얼핏 들으면 위치에 상관 없이 계속 선언하여 쓸 수 있으니 더 좋은 게 아닌가 하고 생각할 수 있지만, 메모리에서 내려가는 것이 아닌 `메모리를 계속 잡아먹고 있기 때문에 메모리 관리가 힘들어질 수 있다.` 참조하는 방법도 똑같고, 호출하는 방법도 똑같기 때문에 `같다고 봐도 무방`하지만, 딱 하나 다른 점이 있다면 두 번째의 기명 함수는 `실행 순서가 오지 않아도 실행할 준비`를 하고 있다.

> function 함수명( ){ };

<br>

---

# 👍 함수의 호출/참조/반환

<br>

함수를 호출한 그 위치는 `반드시 어떤 값으로 바뀐다.` return이라는 예약어 뒤에 `반환값을 명시하거나, 예약어를 사용하지 않을 경우 undefined가 호출`된다.

> 함수를 `호출`하기: function 함수명( );
> <br>함수를 `참조`하기: function 함수명;

<br>

함수로 호출하는 목적이 때로는 `어떤 값을 호출한 그 위치로 가지고 오기 위해서 호출하는 경우`도 있다. 아래 예제는 `999라는 값`을 가지고 오기 위해 호출한 경우다. 

```jsx
let getNumber=function(){
console.log("getNumber() 호출됨.")
return 999;
};
```

![Untitled](https://ifh.cc/g/nGP8wW.png)

함수가 `종료`되는 것을 <`함수가 return 된다`>라고도 하는데, 위 함수에서 return의 밑으로 함수값이 적혀 있으면 `그 함수값들은 실행이 되지 않는다.` 변수를 `선언`만 하고 `값`을 넣지 않으면 반환값에는 자동으로 `undefined`가 들어간다. 함수를 호출하게 되면 그 위치는 반드시 어떠한 값으로 바뀌기 때문에, 반환값이 없다면 undefined라는 `아무것도 정의되지 않은 상태를 의미하는 데이터`가 나오게 되는 것이다. 반환값에는 undefined를 `명시적`으로 넣어줄 수도 있는데, 굳이 undefined; 를 넣을 필요 없이, `let 변수명;` 을 선언만 해도 된다.

<br>

```jsx
function returnFunc( ){
	return 123;
	console.log("1234"); // return에서 함수가 끝났기 때문에 실행되지 않는다.
```

아래와 같이 반환값이 있는 경우에는 `console.log(”1234”)` 뿐만이 아닌 `모든 함수가 실행되지 않는다.`

<br>

---

# 👍 예제를 통한 실습

```jsx
<script>
          //원숭이를 냉장고에 밀어넣는 함수
          let pushMonkey=function(){
               console.log("냉장고 문을 여세요.");
               console.log("원숭이를 넣으세요.");
               console.log("냉장고 문을 닫으세요.");
          };

          let getNumber=function(){
               console.log("getNumber() 호출됨.")
               return 999;
          };

          let getGreet=function(){
               console.log("getGreet() 호출됨.")
               return "hello~";
          };

					// 변환값의 타입 찾아보기

          let a=pushMonkey(); // what Type?
          let b=getNumber(); // what Type?
          let c=getGreet(); // what Type?
</script>
```

가장 마지막에 적혀 있는 변수 a, b, c의 `데이터 타입(Data Type)`을 알아보겠다. 위에서부터 차근차근 내려오며 분석해 보면, pushMonkey( )에 console.log가 3개 적혀 있는 것이 보인다. 하지만 return으로 시작하는 `변환자`는 보이지 않는다. 그렇기 때문에 `let a=pushMonkey( );`은 아무것도 정의되지 않은 상태인 `undefined type`일 것이다.

두 번째 getNumber( )를 살펴보면 호출되었다는 console.log 다음 줄에 `return 999; 라는 변환값`이 있다. 이는 `변환값이 999인 Number Type`이다.

마지막으로 세 번째 getGreet( )를 살펴보면, 두 번째 줄과 비슷하게 console.log 다음 줄에 `return “hello~”; 라는 변환값`이 있다. 이는 `변환값이 “hello~”인 String Type`이다.

이와 같이 변환자 return의 Data Type을 알아보았는데, 두 눈 부릅뜨고 쳐다보기만 하면 타입은 정말 찾기 쉽다.