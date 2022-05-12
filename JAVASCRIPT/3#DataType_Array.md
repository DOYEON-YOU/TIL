# 👍 Array Type (배열 타입)

4월 1일에 배운 Object Type은 순서가 없는 데이터이다. 하지만 순서가 중요하고 필요한 데이터도 분명 있다. 예제를 들어 설명해 보겠다.

```jsx
let obj={name:"삼겹살", price:"10,000원", expireDate:"2022.06.10", num:1001};
//상품 하나의 정보라고 가정 (나열 순서가 중요치 않은 정보이다.)
```

```jsx
//내가 좋아하는 음식 순위
let foods=["연어초밥", "치킨", "김치찌개", "삼겹살", "냉면"]
// 왼쪽부터 차례대로 0, 1, 2, 3, 4 순서로 index가 붙는다.

// let foods2=Array("연어초밥", "치킨", "김치찌개", "삼겹살", "냉면");
// let foods3=new Array("연어초밥", "치킨", "김치찌개", "삼겹살", "냉면");
```

<br>

---

<br>

## 👌 배열 요소의 Type 구분해 보기

배열은 `정렬된 값들의 집합`으로 정의되며, Array 객체로 다루어진다. 밑의 예제를 확인하고 `배열과 각 배열 요소의 type를 구분`해 보자.

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/1a869c00-8a62-4ddc-be0d-66fbc1d40f63/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T191142Z&X-Amz-Expires=86400&X-Amz-Signature=0e1d4c4405c96d6f9cc28cd5de8d6e0818ab1869b031d5b9163532706fb96116&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

```jsx
<script>
		let test1= [10, "문자열", false];

		document.write((typeof test1) + "<br>");
		document.write((typeof test1[0]) + "<br>");
		document.write((typeof test1[1]) + "<br>");
		document.write(typeof test1[2]);
	</script>
```

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/70d41698-6487-4da1-8014-aeb6da1b525c/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T191200Z&X-Amz-Expires=86400&X-Amz-Signature=2a5f777aa09f94f76ee4c72f4c44188ddff0070e500b69b3946e9f79fb2e11fe&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

수업 중 선생님께서 직접 설명해 주신 Type 구분하는 방법이다.
직관적으로 설명을 잘 해 주셨으니 구분하는 방법을 확실히 배우자.

<br>

---

<br>

자바스크립트에서 배열을 만드는 방법은 `세 가지`로 나뉘어 있다.

<aside>
💡 1. let 배열명 = [배열요소1, 배열요소2,...];          *// 배열 리터럴을 이용하는 방법*

2. let 배열명 = Array(배열요소1, 배열요소2,...);     *// Array 객체의 생성자를 이용하는 방법*

3. let 배열명 = new Array(배열요소1, 배열요소2,...); *// new 연산자를 이용한 객체 생성 방법*

</aside>

  `[쉼표로 구분하여 순서대로 나열]` 해야 한다. array type을 밑에서 응용해 보겠다.

<br>

---

<br>

## 👌 let 응용

```jsx
				let a=foods[0];
				let b=foods[1];
```

a라는 변수에 foods라는 변수의 `첫 번째 값`(연어초밥)을 넣고, b라는 변수에 foods라는 변수의 `두 번째 값`(치킨)을 넣겠다는 의미이다. `배열의 특정 인덱스에 저장된 item을 참조해서 변수에 담는 것`이다.

```jsx
let 변수명=배열명[index];
```

<br>

---

<br>

## 👌 대입 응용

```jsx
				foods[0]="라면";
				foods[1]="짬뽕";

let foods=["라면", "짬뽕", "김치찌개", "삼겹살", "냉면"]
```

foods라는 변수의 `첫 번째 값(연어초밥)에 라면을 대입`하고, foods라는 변수의 `두 번째 값(치킨)에 짬뽕을 대입`하겠다는 의미이다. `배열의 특정 인덱스에 저장된 item을 수정하는 것`이다.

```jsx
배열명[index]="수정할 값";
```

<br>

---

<br>

## 👌 배열 요소 추가 함수

```jsx
				foods.push("피자");
				foods.push("햄버거");

let foods=["연어초밥", "치킨", "김치찌개", "삼겹살", "냉면", "피자", "햄버거"]
```

`배열의 마지막`에 피자와 햄버거라는 요소를 더 `추가`하겠다는 의미이다. `배열에 item을 추가하는 것`이다. 총 세 가지의 방법이 있는데, 밑에 예시 코드에서 알아보자.

```jsx
배열명.push("추가할 값");
배열명(배열명.length] = "추가할 값";
배열명[index] = "추가할 값";
```

⛏ **Code**

```jsx
<script>
		let test2 = [1, true, "Java"];
		test2.push("Script");				// push() 메소드를 이용하는 방법
		document.write(test2 + "<br>");

		test2[test2.length] = 100;			// length 프로퍼티를 이용하는 방법
		document.write(test2 + "<br>");

		test2[10] = "자바스크립트";		// 특정 인덱스를 지정하여 추가하는 방법
		document.write(test2 + "<br>");
</script>
```

🎨 **Result**

![Untitled](https://ifh.cc/g/btGwfb.png)

첫 번째 줄에서는 `1, true, "Java"` 라는 기본 배열에 push( ) 메소드를 이용하여 “Script” 라는 단어를 하나 더 추가시켰고, 두 번째 줄에서는 `test2.length`라는 길이 반환 함수로 `길이를 100으로 설정한 후 배열값에 100을 입력`했다.  마지막으로 세 번째 줄에서는 `10번 index`, 그러니까 `11번째에 “자바스크립트”라는 단어를 추가`했다. 마지막 줄의 쉼표는 10번 index를 선택하면서 선택받지 못한 `5, 6, 7, 8, 9 번 index가 빈자리로 남겨져 쉼표만 표시되는 것`이다.

<br>

---

<br>

## 👌 배열 길이 반환 함수

```jsx
				let size=foods.length;

let foods=["연어초밥", "치킨", "김치찌개", "삼겹살", "냉면"]
length: 5
```

foods 변수의 배열 요소의 `길이를 측정`하여 숫자로 나타낸다. `배열의 크기를 참조해서 변수에 담는 것`이다.

```jsx
let size=배열명.length;
```

<br>

---

<br>

## 👌 배열 요소 삭제 함수

```jsx
foods.splice(2, 1);

let foods=["연어초밥", "치킨", "삼겹살", "냉면"]
```

foods[2] 즉 김치찌개부터 1개의 배열 요소를 삭제하겠다는 의미로 김치찌개를 시작으로 첫 번째인 `“김치찌개”` 배열 요소가 삭제된다. `배열의 특정 인덱스에 저장된 item을 삭제하는 것`이다.

```jsx
배열명.splice(삭제를 시작할 index,몇 번째의 요소를 삭제할 것인지);
```

<br>

---

<br>

![Untitled](https://ifh.cc/g/3GlKdo.png)

보면서 push, length, splice와 같은 함수들을 모두 익혀두자.