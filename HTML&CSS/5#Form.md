## 👍 폼(Form) 요소 작성하기

`<form>` 태그는 서버에 전송할 양식이다. **`action="서버에 전송할 경로"`** 의 형식으로 서버에 전송이 되는데, 현재는 서버가 없기 때문에 action을 테스트할 수는 없다.

양식 작성법만 학습해 보자.

<br>

**Form 요소에 사용할 수 있는 요소**

```html
<button>
<fieldset>
<input>
<label>
<option>
<optgroup>
<select>
<textarea>
```

<br>

⛏  **Code**

```html
<form>
        <label for="email">이메일</label>
        <input type="text" id="email" name="email">
        <br>
        <label for="pwd">비밀번호</label> 
        <input type="password" id="pwd" name="pwd">
        <button type="submit">로그인</button>
</form>
```

<br>

🎨 **Result**

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/75caf629-c864-4297-bf12-8c4773407c71/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T184951Z&X-Amz-Expires=86400&X-Amz-Signature=66cd1c851befaf0b2ad2e794433eb93527e1396a2c5f6e6f71d2bf19cd85af9c&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

위 결과물에서 보이는 것과 같이, 위에 입력한 코드로 인해 로그인 창이 만들어졌다. 

<br>

---

<br>

### 👌 label& input

> label에 대해

`<label>` 태그는 사용자 인터페이스(UI) 요소의 `라벨(label)`을 정의할 때 사용한다.  `<label>` 요소는 for 속성을 사용하여 `다른 요소와 결합`할 수 있으며, 이때 `<label> 요소의 for 속성값`은 결합하고자 하는 요소의 `id 속성값`과 **같아야 한다.** label의 특성은 **모든 사용자의 입력의 용도** 또는 **역할에 대한 설명**이라고 할 수 있다.

- label 요소와 결합할 수 있는 요소
    ```
    <button>, <input>, <meter>, <output>, <progress>, <select>, <textarea>
    ```

> input에 대해
> 

`<input>` 태그는 사용자로부터 입력을 받을 수 있는 `입력 필드(input filed)`를 정의할 때 사용한다. `<input>` 요소는 사용자가 데이터를 입력할 수 있는 입력 필드를 선언하기 위해 `<form> 요소 내부`에서 사용되며,  이러한 입력 필드는 `<input>` 요소의 `type 속성값`을 달리함으로써 여러 가지 모양으로 나타낼 수 있다. `<input>` 요소는 Close Tag가 필요 없는  `빈 태그(empty tag)`이며, `속성만을 포함`하고 있다.

- input 요소가 나타낼 수 있는 타입 속성
    
    button, checkbox, color, date, datetime-local, email, file, hidden, image, month, number, password, radio, range, reset, search, submit, tel, text, time, url, week
    

<br>

---
<br>


그렇다면 실습을 통해 label과 input의 관계성을 알아보자. 위 예제에서 텍스트창이 이메일과 비밀번호로 나누어져 있다. 위 코드를 바탕으로 만들어진 입력창에 이메일과 비밀번호를 입력해 보겠다.

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/dd3405bd-fafa-403d-ab4b-7931b14eea1f/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T185006Z&X-Amz-Expires=86400&X-Amz-Signature=6a0e605599c0c2f63706ca474651d229f999b3251c6b63713a4326d092d595ce&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

이와 같이 `이메일은 정상 표시` 되고, `비밀번호는 표시되지 않는 것`을 볼 수 있다. 코드를 하나하나 살펴보며 분석해 보겠다.

<br>

---


# 👍 Input Field

## 👍 입력 필드(Input Field)

```html
<label for="id명">역할</label>
<input type="입력 필드" id="id명" name="서버에 전송될 내용">

or

<label>
				역할 <input type="입력 필드" id="id명" name="서버에 전송될 내용">
</label>
```

```html
<label for="email">이메일</label>
<input type="text" id="email" name="email">
```

```html
<label>
    이메일<input type="text" id="email" name="email">
</label>
```

분리되어 있던 label과 input 속성을 `label로 input 속성을 감싸 간단`하게 표현하고 있다. label의 속성을 하나하나 적어야 할 때가 분명 오지만, 지금은 간단한 방식으로 사용하는 게 좋을 것 같다.

<br>

---

<br>

### 👌 text

```html
<label for="email">이메일</label>
<input type="text" id="email" name="email">
```

이메일 텍스트 창을 만들어준 코드이다. `input type을 text로 정의`해 주어 웹 브라우저에 **이메일**이라는 이름을 가진 텍스트창이 생성된 것이다.

<br>

### 👌 password

```html
<label for="pwd">비밀번호</label> 
<input type="password" id="pwd" name="pwd">
```

비밀번호 텍스트 창을 만들어준 코드이다. `input type을 password`로 정의해 주어 웹 브라우저에 **비밀번호**라는 이름을 가진 텍스트창이 생성된 것이다.

<br>

### 👌 radio

```html
<label> 
<input type="radio" name="gender"
value="man" checked> 남자
</label>
<label>
<input type="radio" name="gender"
value="woman"> 여자
</label>
```

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/8f9e3934-7ff2-473b-ab17-26a64a318c02/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T185213Z&X-Amz-Expires=86400&X-Amz-Signature=f873229a705faa4c164649be4485f43477ba75f19d3d457cad7e6349fe78c3af&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

**`복수 선택이 불가`**하다. 같은 그룹 내에서 하나의 선택지만 선택할 수 있다. name이라는 속성에 같은 값을 입력하면 `같은 그룹으로 지정`할 수 있다. 원하는 radio에 checked라는 값을 입력해 주면 위와 같이 웹페이지가 로드될 때 체크가 되어 표시된다.

⇒ 같은 그룹 내에서 택1

<br>

### 👌 checkbox

```html
<label>
<input type="checkbox" name="hobby"
value="soccer"> 축구
</label>
<label>
<input type="checkbox" name="hobby"
value="baking"> 베이킹
</label>
```

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/e156ac10-31e3-446c-98cf-bfcb2b0fc712/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T185228Z&X-Amz-Expires=86400&X-Amz-Signature=4401ceafa28f754a9b32d735779330eeb6afd3dcb45a020c2dd6ab690e99bdb4&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

`복수 선택이 가능`하다. 같은 name으로 설정하여도 `같은 그룹으로 묶이지 않는다.` 마찬가지로 checked라는 값을 입력해 주면 웹페이지가 로드될 때 체크가 되어 표시된다.

⇒ 그룹이 묶이지 않으며 택多

<br>

### 👌 button type=”submit”

```html
<button type="submit">로그인</button>
```

로그인 버튼이다. `button type을 submit`의 용도로 정의하여 서버에 입력값을 전송할 수 있게 해준다. ~~input type 속성은 아니지만, 이메일과 비밀번호를 입력하는 창에는 제출 버튼이 필수적이다.~~

<br>

---

## 👍 html5에서 추가된 입력 필드(Input Field)

현재 지원이 되는 브라우저도 있고 안 되는 브라우저도 있어서 `범용적으로 사용할 수는 없지만`, 참고로 알아놓으면 좋다. 크롬과 엣지에서는 적용이 잘 되고, 지원하지 않는 브라우저에서는 `input type="text"`로 인식하게 된다.

<br>

### 👌 color

```html
<label for="color">
색상 선택
<input type="color" id="color" name="color">
</label>
```

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/86b59652-b447-4c7a-bf69-ac453485186b/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T185239Z&X-Amz-Expires=86400&X-Amz-Signature=d6048ac2ec5ef0ddebe413d1ffa622a4ad308092099cc9a609921b709a5fe01a&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

색상을 직접 선택할 수 있는 `색상 피커`가 표시된다.

<br>

### 👌 range

```html
	<label for="range">
	범위
	<input type="range" id="range"
	name="range" min="10" max="100"
	step="1" value="10">
	</label>
```

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/d80e6cdc-fc27-4021-bda5-92ebc8f3b8bd/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T185246Z&X-Amz-Expires=86400&X-Amz-Signature=a28a94804d0002ca406cd20088b02bed1338b711db56a31f6c1ac35f17ee4192&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

범위를 선택할 수 있는 `슬라이드 바`가 표시된다. 기본 범위는 0부터 100까지이지만, 다음 속성들과 함께 사용하면 그 범위를 설정할 수 있다.

<br>

### 👌 date


```html
<label for="date">
날짜
<input type="date" id="date" name="date">
</label>
```

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/7af24efd-a46d-40bb-b47d-04a42423d51d/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T185255Z&X-Amz-Expires=86400&X-Amz-Signature=c8db66a3bb2c0c4e0306049773c29f4e35d2317e10792764264ace76bd700ba0&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

날짜를 입력할 수 있는 `텍스트 필드`와 날짜를 직접 선택할 수 있는 `특별한 입력기`가 함께 표시된다.

<br>

### 👌 time

```html
<label for="time">
시간
<input type="time" id="time" name="time">
</label>
```

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/f7f653c5-1719-48ee-8eac-8ccabdabbfb3/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T185304Z&X-Amz-Expires=86400&X-Amz-Signature=65ff42d8526a0aebe8de8c443284e66dcfdb01a69253848f7d03b9b11f93e595&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

시간을 직접 입력할 수 있는 `텍스트 필드`와 시간을 선택할 수 있는 `특별한 입력기`가 표시된다.

<br>

### 👌 number

```html
	<label for="number">
	숫자
	<input type="number" id="number"
	name="number" min="10" max="100"
	step="1" value="10">
	</label>
```

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/e58c90b6-d320-42d4-825c-8b8cc97b4b44/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T185316Z&X-Amz-Expires=86400&X-Amz-Signature=aeab2adf68a8d94ea61b4283a9d117d1e81a8c491aea3c62dff4b53748e689bb&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

*숫자를 보다 쉽게 입력할 수 있는 `텍스트 필드`와 `화살표`가 있다.*

<br>

### 👌 file

```html
<label>
첨부파일 <input type="file" id="myFile"
name="myFile">
</label>
```

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c0247b70-b30e-423c-b49b-05ad327a7af0/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T185331Z&X-Amz-Expires=86400&X-Amz-Signature=bc600260de9f159fdd19fdbaec0382881949048d845a858ce323cde1d34fd935&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

웹페이지에서 사용자의 `로컬 파일`을 입력받기 위한 속성이다.  accept에 입력받을 수 있는 파일의 유형을 지정할 수 있다.

EX)`<input type="file" id="myFile"
name="myFile" accept="jpg,png,psd">`  

<br>

> 시각 장애인의 접근성
> 

시각 장애인이 Screen Reader를 사용하여 Tab을 눌렀을 때 Focus되는 부분은 `input, button`이다. `input의 id 속성`과 `label의 for 속성`은 <이메일> 이라는 `글자를 가리키기` 때문에 시각장애인이 Screen Reader를 통해 웹브라우저를 접했을 때에는 이메일이라는 음성이 출력된다.

<br>

---

# 👍 Select

⛏ **Code**

```html
<select name="job" id="job">
    <option value="slc">select</option>
    <option value="one">1</option>
    <option value="two">2</option>
    <option value="three">3</option>
    <option value="four">4</option>
</select>
```

🎨 **Result**

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/8eef946d-bf11-40a4-acb3-bbbae823400b/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T185341Z&X-Amz-Expires=86400&X-Amz-Signature=a72248e5d79c98d064377c95998cd1bb87a7c89ae85b5005883089942ea43112&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

위 코드를 분석해 보면 select 요소는 아래로 펼쳐지는 목록 상자, 즉 `선택지`의 역할을 하며, option은 선택지 내에서 `선택할 수 있는 요소`이다. option을 그룹으로 묶을 수 있는 `optgroup`은 선택할 수 있는 요소들을 `특정 주제로 분류하고 싶을 때 사용`한다. 또한, option 요소는 `단독 사용이 불가능`하기 때문에 무조건 select를 부모 요소로 삼아야 한다.

<br>

---

## 👌 option

option value의 value는 클라이언트가 그 값을 선택하였을 때 서버로 전송되어 오는 값인데, option 에 value가 없으면 innerText 가 전송된다. 해당 요소를 `선택했을 때 서버로 전송되어 오는 값`을 살펴보자.

```html
<form>
	<select name="fruit" id="fruit">
	<option value="">-- 좋아하는 과일 선택 --<option> => fruit=-- 좋아하는 과일 선택 --
	<option value="strawberry">딸기</option> => fruit=strawberry
	<option value="banana">바나나</option> => fruit=banana
	<option value="grape">포도</option> => fruit=grape
	</select>
</form>
```

### 👌 optgroup

이번엔 `optgroup`의 예제를 살펴보겠다.

⛏ **Code**

```html
<select name="lunch" id="lunch">
            <optgroup label="분식">
                <option>라면</option>
                <option>쫄면</option>
                <option>김밥</option>
            
            </optgroup>
            <optgroup label="중식">
                <option>자장면</option>
                <option>짬뽕</option>
                <option>군만두</option>
            </optgroup>
        </select>
```

🎨 **Result**

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/54ac0e40-d4ff-4675-81d4-3faf10f92f92/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T185356Z&X-Amz-Expires=86400&X-Amz-Signature=1d25401f029ca83125fd8e7d7633ddce45334d7e22944a4ba6327f3ffb754a6a&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

위와 같이 `option을 묶어주는 카테고리`와 같은 역할을 한다. `라면, 쫄면, 김밥은 분식` / `자장면, 짬뽕, 군만두는 중식` 으로 나뉘어져 한 그룹으로 묶여져 있는 선택 목록들이 어떤 카테고리에 속해 있는지 표현할 수 있다.

<br>

---

# 👍 textarea

input type의 속성값인 text와는 다른, `textarea`라는 요소이다. input type=”text”라는 텍스트 입력 필드는 `한 줄 작성`만 가능하지만 textarea 요소는 텍스트를 `한 줄이 아닌 여러 줄로 작성`할 수 있다는 특성이 있다. 이 요소는 개행 기호의 영향을 받지 않아 자유롭게 개행을 할 수 있다는 장점이 있지만, 서버에 전송되어 서버에서 읽어낼 때에는 개행 기호를 `₩n` 으로 해석하게 된다. 쉽게 이해하기 위해 예제를 활용해 보자.

```html
<textarea name="texttest" id="texttest" cols="30" rows="10"></textarea>
```

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/b9c3e9ee-b176-4b32-95a1-69dae2252b91/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T185404Z&X-Amz-Expires=86400&X-Amz-Signature=8bbbb1d225e5b241ceca30dd113a79939523c35f62bed9aa4fa55b6030f7c63b&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

위와 같이 입력 후 서버에 전송되었을 때, 서버에서는 위와 같은 text를 `AB₩nCD` 로 해석한다.