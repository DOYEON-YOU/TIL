**배열 속 객체를 다루기 전, 타입에 대한 정리를 한 번 더 하고 시작하겠다.**

<br>

<aside>
💡 **number type**: `산술 연산`이 가능한 데이터
**string type**: `문자 표현`이 가능한 데이터
**boolean type**: `참과 거짓이 표현`이 가능한 데이터
**object type**: `순서가 중요치 않은 여러 개의 데이터`를 하나의 묶음으로 관리 가능한 데이터
**array type**: `순서가 중요한 여러 개의 데이터`를 하나의 묶음으로 관리 가능한 데이터
**function type**: `특정 시점에 일괄 실행할 javascript`를 여러 줄 모아 놓을 수 있다. `호출`은 무조건 반드시 함수만 할 수 있다.
**undefined type**: `아무것도 정의되지 않은 상태`를 의미하는 데이터

</aside>

<br>

## 👍 배열 속 객체 (Object In Array)

 

```jsx
					let nums=[10, 20, 30, 40, 50];
          let names=["김구라", "해골", "원숭이", "오랑우탄", "고릴라"]
          let data=[true, true, false, false, true]
```

> 1 -> 번호<br>
>"권도연" -> 이름<br>
>173 -> 키<br>
>연 -> 별명?<br>
>true -> 여자인지 여부?

<br>

이러한 데이터는 `Array Type`이 아닌 `Object Type`으로 다루는 것이 좋다. 무엇을 나타내는지 정확히 모르기 때문이다. 하지만 한 사람 한 사람의 데이터를 모두 object type으로 적는다면 object가 너무 많아진다.

<br>

배열 안에는 객채를 담을 수 있다. 그 예시로는 `회원 목록, 글 목록, 상품 목록` 등이 있다. 배열은 `let 배열명=[index0, index1, index2]`의 형식으로 실행 되는데 배열 안에 `object의 참조값`이 들어 있기 때문에 `index를 사용해 오브젝트를 선택하고 오브젝트의 값을 불러올 수 있는 것`이다. 세 개의 오브젝트는 heap 영역에 배열로 묶여서 실제 데이터 파일로 저장되어 있다.

<br>

`ex) [{첫 번째 오브젝트}, {두 번째 오브젝트}, {세 번째 오브젝트}]`

<br>

그렇다면 바로 예시로 넘어가 살펴보겠다.

```jsx
<script>
let members=[
          {num:1, name:"권도연", addr:"서울시"},
          {num:2, name:"장준", addr:"강남구"},
          {num:3, name:"이름", addr:"개포동"}
		        ];
</script>
```

<br>


위 예시에서 `members[1].num`은 무엇일 것 같은가? 세 개의 오브젝트는 각각 0, 1, 2의 index를 사용해 선택할 수 있다. 1번 index의 number 값은 2이기 때문에, `members[1].num=2;` 가 된다. 이렇게 타입의 구분을 통해 원하는 값을 바로 찾아낼 수 있어야 한다.

<br>

```jsx
				//members라는 변수는 object 3개가 합쳐진 배열이기 때문에 변수 a는 array type이다.
				//참조값이 표현되어 있기 때문에 값을 표현할 수 없다.
        //array type value= 알 수 없다.
        let a=members;

        //배열의 첫 번째는 object type이기 때문에 변수 b는 object type이다.
				//참조값이 표현되어 있기 때문에 값을 표현할 수 없다.
        //object type value= 알 수 없다.
        let b=members[0];

        //배열의 첫 번째 오브젝트 속 값이 1인 number type이다. c의 값은 1이다.
				//(값을 표현할 수 있는 타입은 숫자, 문자열, 불리언 타입이다.)
        //number type1 value=1
        let c=members[0].num;

        //string type1 value="권도연"
        let d=members[0].name;

        //string type2 value="서울시"
        let e=members[0].addr;
```