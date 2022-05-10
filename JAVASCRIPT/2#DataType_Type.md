# ❓ 변수(let)에 대하여

```jsx
let a = 10
```

변수는 **어떤 값을 기억할 수 있는 이름 지어진 기억 공간**이다.

`let 변수명(key) = 값(value);`

let = 의 `=(equal)` 은 같다의 의미가 절대 아니며, `값을 변수명에 대입하라` 라는 의미이다.

예시로 [`박스에 사과를 넣어`] 를 프로그래밍 언어로 표현하면 [`박스 = 사과`] 가 된다.

따라서 위 `let a=10;`의 의미는 `a라는 이름의 기억 공간을 만들어서 10이라는 숫자를 대입해라` 라는 의미이다.

<br>

---

<br>

# ❓ Type에 대하여

<br>
데이터 타입은 **프로그래밍 언어에서 사용할 수 있는 데이터 (숫자, 문자열, 불리언 등)의 종류**
를 말한다. 밑에서 더 자세히 알아보겠다.

<br>

---

<br>

# 👍 기본 타입

<br>

## 👌 Number Type (숫자 타입)

```jsx
let num1 = 1
let num2 = 2
let num3 = 3
```

number type은 `숫자를 이용한 사칙연산`이 가능하다. 위 예시에서 num1, num2, num3라는 변수명을 지어 각 변수에 붙여주었다. 이 변수들로 연산을 하려면 어떻게 해야 할까? 밑에서 알아보겠다.

<br>

```jsx
let num4 = num1 + num3
```

num4라는 변수를 새로 만들어 num1과 num3을 더해 주었다. num1의 값은 1, num3의 값은 3이기 때문에 num 4는 4가 된다. 직접 확인해 보자.

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/ec38eea5-6ac0-488e-bf10-c72fdf53784e/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T190421Z&X-Amz-Expires=86400&X-Amz-Signature=ca7ffdacb964ba0d2e4433d90836c70ecb20c829b806b84ff269a4200f405a5a&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

num1~num3의 변수를 이미 만들어둔 상황에서 num4라는 변수를 새로 선언했다. num4의 값은 역시나 4가 나왔다. 위 변수를 다시 해석해 보면 **1을 num1이라는 변수에 대입**하고, **2를 num2라는 변수에 대입**하고, **3을 num3이라는 변수에 대입**하라는 뜻이다. 그렇기 때문에 `num4`는 `1과 3을 더한 숫자를 대입하라는 뜻`이기에 `4를 num4라는 변수에 대입`하여 `num4라는 변수의 값은 4`가 되는 것이다.

숫자 타입과 관련된 연산자는 이렇게 있다. 산술 연산은 프로그래밍도 수학과 똑같기 때문에 어렵지 않다.

> 산술 연산자:
> <br>더하기(+),
> 빼기(-),
> 곱하기(\*),
> 나누기(/)
> <br><br>
> 대입 연산자:
> <br>대입(=)

<br>

---

<br>

## 👌 String Type (문자열 타입)

<br>

```jsx
let myName = '권도연'
let isHer = '은 여자다'
```

string type은 `변수의 값이 문자열인 경우`이다. 변수의 값이 문자열인 경우 반드시 `따옴표(” or ‘)나 백틱(`)`이 붙으며 숫자들을 더할 때와 마찬가지로 아래와 같이 `+ 기호를 사용하여 문자열을 붙일 수 있다.` 위의 두 변수를 이용해 권도연은 여자다 라는 문자열을 만들고 싶을 때는 아래와 같이 하면 된다.

```jsx
myName+isHer; = "권도연" + "은 여자다"
```

string type은 입력할 수 있는 방법이 총 세 가지로 나뉘는데, `작은 따옴표와 큰 따옴표, 백틱`으로 나뉘어 있다. 밑의 예제를 통해 자세히 알아보자.

```jsx
let str1 = '1234'
let str2 = '안녕하세요'
let str3 = `안녕하세요2`
let str4 = `
            안녕하세요
            좋은 하루예요
				`
```

작은 따옴표, 큰 따옴표, 백틱으로 확연하게 나뉘어 있는데 `백틱은 여러 줄의 문자열이 작성`되어 있다. 이것은 작은 따옴표와 큰 따옴표는 적용되지 않지만 백틱을 이용했을 때에 `개행 기호를 사용`할 수 있어 문자열을 편하게 작성할 수 있다는 장점이 있다. str4라는 이름을 가진 변수를 콘솔 창에 입력해 값을 출력해 보면

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/976ac34f-ac1c-48fc-a864-b986afe45f6b/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T190440Z&X-Amz-Expires=86400&X-Amz-Signature=2367bc80d97e330a8e52424fa89f49acb3da099e011e1878bbc381f9cc2b5df4&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

이와 같이 `백틱, 개행 문자, Tab이 모두 표현되어 있는 것`이 보인다.

str1을 보면 `숫자`만 입력이 되어 있는 것이 보인다. 숫자가 값인 변수는 number type이라고 하였는데, 어째서 string type에 숫자값도 포함인 걸까? `string type을 다룰 때에는 숫자를 문자열`로 본다. 즉, `사칙연산이 되지 않는다`는 뜻이다. 밑에서 다뤄보겠다.

```jsx
let a = 1
let b = 2
let c = a + b //즉 a+b, 1+2를 대입한 것이 변수 c의 값이다. 따라서 c 변수의 값은 3이다.

let str1 = '12'
let str2 = '34'
let str3 = str1 + str2 //문자열 12와 문자열 34가 더해지면 연산이 되어 46이 되는 것이 아닌
//1234로 문자열이 붙여진다. 문자열과 문자열이 더해진 것이기 때문이다.
```

이와 같이 문자열과 문자열의 합쳐짐은 연산이 아닌 문자열의 조합이다.

<br>

---

## 👌 Boolean Type (논리형 타입)

```jsx
let result = 10 < 1
let result2 = 10 > 1
let result3 = 10 == 10
let result4 = 10 != 10
let result5 = 'kim' == 'lee'
let result6 = 'kim' != 'lee'
```

위의 코드를 잘 보면, 모두 왼쪽과 오른쪽의 값을 비교한다. boolean type의 값은 논리적 `참과 거짓`을 나타내는 `true/false` 뿐이다. 위 예제를 잘 보면 result라는 변수에 맞지 않는 공식이 적혀 있다. 이러한 값을 false, 즉 거짓이라고 표현하며 result2라는 변수에는 맞는 공식이 적혀 있기 때문에 이러한 값을 true, 즉 참이라고 표현한다.

이를 비교할 때 사용하는 연산자를 비교 연산자라고 하는데, 비교 연산자에는 이런 것이 있다.

<aside>
💡 모든 것은 맞으면 true, 틀리면 false로 값이 표현된다.

`>` 왼쪽이 오른쪽보다 큰지 비교하기

`<` 왼쪽이 오른쪽보다 작은지 비교하기

`>=` 왼쪽이 오른쪽보다 크거나 같은지 비교하기

`<=` 왼쪽이 오른쪽보다 작거나 같은지 비교하기

부등 연산자 `!=` 양쪽의 값이 다른지 비교하기

불일치 연산자 `!==` 양쪽의 타입과 값이 모두 다른지 비교하기 ("1234" !== 1234 -> true / "1234" !== "1234" -> false)

동등 연산자 `==` 양쪽의 값이 같은지 비교하기

일치 연산자 `===` 양쪽의 타입과 값이 모두 같은지 비교하기 ("1234" === 1234 -> false / "1234" === "1234" -> true)

</aside>

boolean type 데이터가 들어가는 변수의 이름은 대화식으로 지으면 가독성이 좋다.

`isXXX, canXXX`

예시)

```jsx
let isRun = true // 달릴 것인지
let isWait = false // 기다릴 것인지
let canRun = true // 달릴 수 있는지
let canWait = false // 기다릴 수 있는지
```

<br>

실전에서 비교해 보기

```jsx
//왼쪽이 오른쪽보다 큰지 비교하기 ; true
let result = 10 > 1

//왼쪽이 오른쪽보다 작거나 같은지 비교하기 ; false
let result2 = 10 <= 1

//양쪽의 값이 같은지 비교하기 ; true
let result3 = 10 == 10

//양쪽의 값이 다른지 비교하기 ; false
let result4 = 10 != 10

//양쪽의 값이 같은지 비교하기 ; false
let result5 = 'kim' == 'lee'

//양쪽의 값이 다른지 비교하기 ; true
let result6 = 'kim' != 'lee'

//양쪽의 값과 타입이 같은지 비교하기 ; true
let result7 = 'kim' === 'kim'

//양쪽의 값과 타입이 다른지 비교하기 ; true
let result8 = '10' === 10
```

<br>

---

# 👍 참조 타입

<br>

## 👌 Object Type (객체 타입) ⭐

```jsx
let num = 1
let name = '권도연'
let isMan = false
```

<br>

object type은 데이터와 그 데이터에 관련한 동작(절차, 방법, 기능)을 모두 포함할 수 있는 개념적 존재이다. jsx는 `객체 기반의 스크립트 언어`로써 jsx를 이루고 있는 거의 모든 것이 `객체`이다. 원시 타입을 제외한 나머지 값들(배열, 함수, 정규표현식 등)은 모두 객체이다. 기본 타입으로 분류 되는 숫자, 문자열, 불린 값, undefined, null 값을 제외한 모든 값은 객체로 취급한다. 또한 **객체는 `참조에 의한 전달` (pass-by-reference)방식으로 전달된다.**

위의 값을 한 명의 회원 정보라고 가정했을 때, `번호, 이름, 성별` 의 정보를 자바스크립트에 담아 보자. 그런데, 위의 회원 정보가 1명씩 늘어나다 보면 점점 변수의 수가 많아진다. 그렇다면 한 개의 변수명으로 여러 개의 값을 한 번에 관리할 수는 없을까?

object 타입으로 관리할 수 있다. 여러 값을 하나의 묶음으로 관리하고자 할 때 사용하는 data type이 object type이다. object type은 중괄호를 열고 닫아 만들 수 있다. 중괄호 안에 작성하는 문법은 `key:value` 이다. 위 예제를 이용한 아래 예제를 통해 더 자세히 알아보고, 분석해 보자.

<br>

```jsx
let mem1 = { num: 1, name: '권도연', isMan: false }
let mem2 = { num: 1, name: '권도연', isMan: false }
let mem3 = { num: num, name: name, isMan: isMan }

let a = mem1 //mem1에 있는 object type의 값을 a에 복사함

//b는 number type
let b = mem1.num

//c는 string type
let c = mem1.name

//d는 boolean type
let d = mem1.isMan
```

mem1이라는 변수에서 num:1이라는 값을 가지고 오고 싶다면 mem1.num 을 콘솔 창에 입력하면 된다. [key:value = 저장소의 이름:데이터의 저장소] 라고 생각하면 쉽다. object type의 값 중 하나만을 불러올 수 있는 방법을 밑에 보기 쉽게 정리해 보겠다.

<br>

<aside>

`let a=mem1.num;` -> mem1.num의 값을 불러온 것이다. → let a=1;

`mem1.num=2;` -> 2를 mem1.num의 값에 덮어쓴 것이다. → num:2;

`alert(mem1.num);` -> mem1.num의 값을 불러와 알림창에 띄운 것이다. → alert(1);

`alert(mem1.num)+2;` -> mem1.num의 값은 1이기에 2를 더하면 3이 된다. → alert(3);

</aside>

<br>

하지만 이제부터 조금 헷갈린다.

```jsx
let obj1={name:"권"};
let obj2={name:"권"};
obj1==obj2 -> false
```

두 변수는 `타입이 같다.` 그런데 왜 `false`가 나올까? 그 이유는 두 변수가 `엄연히 다른 객체`이기 때문이다. 주소, 즉 눈에 보이는 모습은 같지만 두 변수의 실제 데이터는 다르다는 의미이다. 쉽게 예를 들어 설명해 보자면, 내가 iphone 13을 샀고, 친구가 iphone 13을 샀다. 기종은 같지만 `내 iphone과 친구 iphone의 type은 같지만 엄연히 다른 물건`이다.

더 쉽게 예를 들자면, 나는 iphone 13을 사서 `10번 사물함`에 넣어두고 10번 사물함 키를 들고 다니다가 핸드폰이 필요할 때마다 10번 사물함을 찾아가서 핸드폰을 사용한다. 하지만 친구는 iphone 13을 사서 `20번 사물함`에 넣어두고 20번 사물함 키를 들고 다니다가 핸드폰이 필요할 때마다 20번 사물함을 찾아가서 핸드폰을 사용한다.

위 사물함이라는 개념은 object type을 아주 잘 설명할 수 있는 개념이다.

```jsx
let obj1 = { name: '권' } //10번 사물함
let obj2 = { name: '권' } //20번 사물함
```

<br>

위 예제와 같이 object type은 중괄호를 열 때마다 새로운 사물함이 생기는 것과 같다. 즉, 중괄호를 열고 닫을 때마다 새로운 데이터가 생긴다는 말이다. 그렇다면 이제 사물함 열쇠를 복사하여 다른 사람에게 준다면 어떨까? 사물함의 개념으로 다른 예시를 들어보겠다.

나는 iphone 13을 사서 `30번 사물함`에 넣어두고 30번 사물함 키를 들고 다닌다. 또한 친구에게도 `같은 사물함 키를 복사`해주었다.

<br>

```jsx
let obj1 = { num: 1 }
let obj2 = obj1
let obj3 = obj1
obj1.num = 2
```

위와 같이 obj1이라는 변수를 obj2라는 변수에 대입하여 `obj2는 {num:1}` 이라는 number type의 값을 가지게 되었다. 사물함의 키를 함께 가지고 있다면 사물함의 내용도 함께 가지고 있을 것이다. 그렇기 때문에 obj1의 값을 바꾸게 되면(`중괄호가 포함되지 않은 산술 연산`이어야 한다.) `obj1과 obj2, obj3은 여전히 같은 값`을 지니게 된다.