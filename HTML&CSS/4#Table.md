## 👍 표 형식으로 정보를 출력하기

테이블(Table)이란 여러 종류의 데이터(data)를 보기 좋게 **정리하여 보여주는 표**를 의미한다. 

아래의 코드로 만들어낸 표를 사용해 3가지 형태로 분석해 보겠다.

⛏ **Code**

```html

    <h1>표 형식으로 정보를 출력하기</h1>
    <table>
        <tr>
            <th>번호</th>
            <th>이름</th>
            <th>주소</th>
        </tr>
        <tr>
            <td>1</td>
            <td>김구라</td>
            <td>노량진</td>
        </tr>
        <tr>
            <td>2</td>
            <td>해골</td>
            <td>행신동</td>
        </tr>
    </table>
    <table border="1">
        <tr>
            <th>번호</th>
            <th>이름</th>
            <th>주소</th>
        </tr>
        <tr>
            <td>1</td>
            <td>김구라</td>
            <td>노량진</td>
        </tr>
        <tr>
            <td>2</td>
            <td>해골</td>
            <td>행신동</td>
        </tr>
    </table>
    <table border="1" id="one">
        <tr>
            <th>번호</th>
            <th>이름</th>
            <th>주소</th>
        </tr>
        <tr>
            <td>1</td>
            <td>김구라</td>
            <td>노량진</td>
        </tr>
        <tr>
            <td>2</td>
            <td>해골</td>
            <td>행신동</td>
        </tr>
    </table>
```

🎨 **Result**

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/8d3f50a8-7113-4530-ad68-80835a6119fd/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T183949Z&X-Amz-Expires=86400&X-Amz-Signature=af7b01f11bb7d9d5f217e151729f7e09770a35eb884b72ca55941c5574d188e5&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

<br>

---

<br>

### 👌 Step 1. 테두리가 없는 표

⛏ **Code**

```html
<table>
        <tr><!-- 첫 번째 -->
            <th>번호</th>
            <th>이름</th>
            <th>주소</th>
        </tr>
        <tr><!-- 두 번째 -->
            <td>1</td>
						<td>김구라</td>
						<td>노량진</td>
        </tr>
        <tr><!-- 세 번째 -->
            <td>2</td>
            <td>해골</td>
            <td>행신동</td>
        </tr>
    </table>
```

<br>

🎨 **Result**

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/868e6fd3-e730-4aee-99a9-ac59f67781bb/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T184002Z&X-Amz-Expires=86400&X-Amz-Signature=93d1ddeea936aeacbc41a12eb1c7ec6a307fef43b33084e15f6804d25477d20a&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

위 표를 확인했을 때 행과 열이 어떻게 나뉘는지, 표의 헤드라인이 어떻게 만들어지는지 파악할 수 있어야 한다. `Table`이라는 부모 요소에 `tr`과 `th`,  `td` 라는 자식 요소와 자손 요소들을 볼 수 있다. border 속성값을 따로 명시하지 않으면 해당 테이블은 언제나 빈 테두리를 가지게 되는데 border 속성값을 작성하지 않았으므로 위 표는 테두리가 없다.

이 코드와 결과물을 보고 알 수 있는 사실은 세 가지가 있다.

1. th Table Head / 표의 헤더, 카테고리

첫 번째 주석을 보자. <tr> 태그 안에 <th> 태그로 번호, 이름, 주소와 같은 것들이 적혀 있다. 결과를 보면 번호와 이름, 주소의 글씨가 굵다. 즉, `표의 헤더`라는 것이다. 큰 부류의 **카테고리**를 적을 수 있다.

```html
th {
  display: table-cell;
  vertical-align: inherit;
  font-weight: bold;
  text-align: center;
}
```

## td Table Data / 열

<br>

전체적인 코드의 흐름을 보고, 두 번째 주석을 확인해 보자. tr 속 자식 요소인 td 태그의 Inner Text를 확인해 보고 결과물을 확인해 보면 **td 태그의 Inner Text는 모두 가로로 나열되는 것**이 보인다. 표의 열을 만든다는 것이다. 그렇기에 td는  `td = Table Data`, 즉 **표의 열**이다.

```html
td {
  display: table-cell;
  vertical-align: inherit;
}
```

## tr Table Row / 행

<br>

tr은 어떤 역할을 할까? 두 번째와 세 번째 주석을 보면, td(열) 요소를 모두 tr이 품고 있다. 그렇기에  `tr = Table Row`, 즉 **표의 행이다.**

```html
tr {
  display: table-row;
  vertical-align: inherit;
  border-color: inherit;
```

<br>


---
<br>

### 👌 Step 2. 테두리가 두 겹인 표

<br>
 

⛏ **Code**

```html
<table border="1">
        <tr>
            <th>번호</th>
            <th>이름</th>
            <th>주소</th>
        </tr>
        <tr>
            <td>1</td>
            <td>김구라</td>
            <td>노량진</td>
        </tr>
        <tr>
            <td>2</td>
            <td>해골</td>
            <td>행신동</td>
        </tr>
</table>
```
<br>

🎨 **Result**

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/58f7c631-71c1-4824-a441-299507803f64/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T184015Z&X-Amz-Expires=86400&X-Amz-Signature=583b2ce38f5d31b231cf94bb44167a2be3b1898901e8494fc84d1546f562b014&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

위 표는 테두리가 두 겹이다. 위의 예제에서 테이블의 테두리(border)가 두 줄씩 나타나는 이유는 `<table>`태그와 `<th>`태그, `<td>`태그가 모두 **자신만의 테두리를 가지고 있기 때문**이다. 그렇다면 테두리가 **실선으로만 이루어진 표**는 어떻게 만들까?

<br>

---
<br>

### 👌 Step 3. 테두리가 실선인 표
<br>

⛏ **Code**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        #one{
            border-collapse: collapse;
        }
    </style>
</head>
<body>
    <table border="1" id="one">
        <tr>
            <th>번호</th>
            <th>이름</th>
            <th>주소</th>
        </tr>
        <tr>
            <td>1</td>
            <td>김구라</td>
            <td>노량진</td>
        </tr>
        <tr>
            <td>2</td>
            <td>해골</td>
            <td>행신동</td>
        </tr>
    </table>
</body>
</html>
```
<br>

🎨 **Result**

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/94fd9ade-8438-4273-94aa-9f36887832ce/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T184026Z&X-Amz-Expires=86400&X-Amz-Signature=6b7ed6dcd53f8d53d2ec40e88ab423a4298d139a785608de9574e585926d1ab3&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

테두리가 두 겹인 표와 실선으로 이루어진 표의 차이점은 단 한 가지이다. CSS area에 `border-collapse: collapse;` 가 있느냐 없느냐의 차이인데, border-collapse 속성값을 collapse로 설정하면 해당 테이블의 테두리는 한 줄로 표현된다. 이 속성을 명시하지 않으면 해당 테이블은 기본 설정으로 테이블 요소별 테두리를 모두 표현하게 된다.

<br>

---
<br>

## 👍 Table 요소 사용하기
<br>

⛏  **Code**

```html
<table border="1">
        <caption>GS25 현금, 카드 매출 내역</caption>
        <colgroup>
            <col width="200"><!-- 1열 -->
            <col width="100"><!-- 2열 -->
            <col width="100"><!-- 3열 -->
        </colgroup>
        <thead>
            <tr>
                <th>상품명</th>
                <th>현금</th>
                <th>카드</th>
            </tr>
        </thead>
        <tfoot>
            <tr>
                <th>합계</th>
                <td>4,300원</td>
                <td>800원</td>
            </tr>
        </tfoot>
        <tbody>
            <tr>
                <td>삼각김밥</td>
                <td>800</td>
                <td>0</td>
            </tr>
            <tr>
                <td>도시락</td>
                <td>3,500</td>
                <td>0</td>
            </tr>
            <tr>
                <td>박카스</td>
                <td>0</td>
                <td>800</td>
            </tr>
        </tbody>
    </table>
```
<br>

🎨 Result

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/8b75a0e0-9ac8-4a33-a29b-6479ece54a84/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T184037Z&X-Amz-Expires=86400&X-Amz-Signature=194536b2b1fcc182508f6bb37ffb8284b392fc3670edc615f0eb337f566bd533&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

---

위에 짜여진 코드를 보면, 1열이 가장 폭이 넓고, 2열과 3열은 폭이 같다. 

이는 `**<colgroup>**` 요소 때문인데, 테이블에서 서식 지정을 위해 하나 이상의 열을 그룹으로 묶을 때 사용한다. `<colgroup> 요소는 <table> 요소의 자식 요소`로, 모든 `<caption> 요소보다 뒤`에 위치해야 하며 모든 `<thead>, <tbody>, <tfoot>, <tr> 요소보다는 앞`에 위치해야 한다.

`**thead, tbody, tfoot**` 요소는 table 요소의 자식 요소이며, `<caption>과 <colgroup> 요소보다 뒤`에 위치해야 한다. `**thead`는 위에서 배운 `th`**와 같고, `**tbody`는 `td`**와 같다. 그렇다면 tfoot은 뭘까?

`**<tfoot>**` 태그는 HTML Table에서 푸터 콘텐츠(footer content)들을 하나의 그룹으로 묶을 때 사용한다.  또한 <tfoot> 요소는 반드시 `**하나 이상의 <tr> 요소를 포함**`하고 있어야 한다. tfoot 요소는 어디에 작성하더라도 `표의 가장 아래행을 차지`하는데, `thead 요소보다는 뒤에 위치`해야 한다. 위 결과물에서 합계와 같이 결과를 알아보기 쉽게 해주는 요소이다.

- 요약
  
    ```html
    caption ⇒ 표의 제목
    colgroup ⇒ 열을 그룹으로 묶을 때 사용
    thead ⇒ 표의 가장 윗부분 (주제)
    tbody ⇒ 표에서 정보를 나타내는 부분
    tfoot ⇒ 합계와 같은 결과를 나타낼 수 있는 부분
    ```  
    
<br>

---
<br>

## 👍 Column / Row 합치기

여기 기본 스타일의 Table이 있다.

⛏ **Code**

```html
    <table border="1">
        <tr>
            <td>1</td>
            <td>2</td>
            <td>3</td>
            <td>4</td>
            <td>5</td>
        </tr>
        <tr>
            <td>6</td>
            <td>7</td>
            <td>8</td>
            <td>9</td>
            <td>10</td>
        </tr>
        <tr>
            <td>11</td>
            <td>12</td>
            <td>13</td>
            <td>14</td>
            <td>15</td>
        </tr>
    </table>
```
<br>

🎨 **Result**

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/724e6f76-21fb-4809-a207-b39ea25ca72b/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T184047Z&X-Amz-Expires=86400&X-Amz-Signature=04ca577e15e7379f9ed73fa021e3593f66bab9f1990ef378b436bc910a9d356b&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

이 테이블에서 1과 2의 칼럼을 합치거나, 1과 6의 로우를 합치거나, 1과 2, 6, 7을 모두 합칠 수 있다. 예제로 바로 알아보자.

<br>

---
<br>

### 👌 colspan


Column(열)을 합치기 위해서는 `**colspan**`이라는 새로운 속성이 필요하다. 원리만 보면 행을 합친다고 하기 보다는, **특정 열을 선택해 폭을 늘리는 것**이기 때문에 그 원리를 잘 알고 있어야 한다. colspan 속성은 아래와 같이 쓸 수 있으며, 몇 개의 열을 차지할 것인지 n에 값을 적어줘야 한다.

```html
<table>
    <tr>
        <td colspan="n"></td>
    </tr>
</table>
```

바로 실습해 보고, 예제를 통해 쉽게 알아보겠다.

<br>

⛏ **Code**

```html
<table border="1">
        <tr>
            <td colspan="4">1</td>
            <td>2</td>
            <td>3</td>
            <td>4</td>
            <td>5</td>
        </tr>
        <tr>
            <td>6</td>
            <td>7</td>
            <td>8</td>
            <td>9</td>
            <td>10</td>
        </tr>
        <tr>
            <td>11</td>
            <td>12</td>
            <td>13</td>
            <td>14</td>
            <td>15</td>
        </tr>
    </table>
```

<br>

🎨 **Result**

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/560ff3e6-62e5-4063-9d68-a1dbb358361b/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T184101Z&X-Amz-Expires=86400&X-Amz-Signature=e79c2ae8c4f98c5f21cbaa2123a6bef188aa184bc10c133599895bfe759aa8ef&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

위 예제를 보면 어딘가 엉성하다. 1이라는 숫자를 4열까지 폭을 늘렸더니 3, 4, 5가 오른쪽으로 밀려났다. 위에서 이야기 했듯이 행을 합친다고 하기 보다는 특정 열을 선택해 폭을 늘리는 것이기 때문에 그렇다. 그렇다면 밀려나온 3, 4, 5를 없애 깔끔하게 정리해 주겠다.

<br>

⛏ **Code**

```html
<table border="1">
        <tr>
            <td colspan="4">1</td>
            <td>5</td>
        </tr>
        <tr>
            <td>6</td>
            <td>7</td>
            <td>8</td>
            <td>9</td>
            <td>10</td>
        </tr>
        <tr>
            <td>11</td>
            <td>12</td>
            <td>13</td>
            <td>14</td>
            <td>15</td>
        </tr>
    </table>
```

<br>

🎨 **Result**

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c1bd35c8-2814-4377-9aca-3878068890ec/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T184116Z&X-Amz-Expires=86400&X-Amz-Signature=5e7156942afda7b850af34f4184a02c4bdb1675ec34128e57ede3144690cca91&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

이제 보기좋게 열이 합쳐졌다. 1열의 열을 4열까지 늘리고, 2~4 열을 삭제해 주었다.

<br>

---
<br>

### 👌 rowspan

Row(행)을 합치기 위해서는 `**rowspan**`이라는 또 다른 속성이 필요하다. colspan과 흡사한 점이 아주 많은데, rowspan은 colspan과 마찬가지로 **특정 행을 선택해 폭을 늘리는 것**이다. rowspan 속성은 아래와 같이 쓸 수 있으며, 몇 개의 행을 차지할 것인지 n에 값을 적어줘야 한다.

```html
<table>
    <tr>
        <td rowspan="n"></td>
    </tr>
</table>
```

rowspan도 똑같이 실습하여 1번과 6번 행을 하나로 합쳐 보겠다.

<br>

⛏ **Code**

```html
<table border="1">
        <tr>
            <td rowspan="2">1</td>
            <td>2</td>
            <td>3</td>
            <td>4</td>
            <td>5</td>
        </tr>
        <tr>
            <!-- <td>6</td> -->
            <td>7</td>
            <td>8</td>
            <td>9</td>
            <td>10</td>
        </tr>
        <tr>
            <td>11</td>
            <td>12</td>
            <td>13</td>
            <td>14</td>
            <td>15</td>
        </tr>
</table>
```

<br>

🎨 **Result**

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/6ad70871-2f2f-40b9-a506-d7aee506cadb/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T184129Z&X-Amz-Expires=86400&X-Amz-Signature=020937ede47cc81ccac0e7b6528b2457d218825ae291a5305b525a7e012dfc8f&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

1열 1행의 1번을 1열 2행인 6번의 자리까지 옮겼다. 대부분 깔끔하게 정리하기 위해서는 쓰지 않는 코드는 삭제해 주는 게 좋지만, 주석 처리를 해도 상관 없다. 이처럼 colspan과 rowspan은 공통적으로 `**td의 속성**`이며, colspan은 오른쪽 전진 rowspan은 아랫쪽 전진인 것을 확인할 수 있다.

<br>

---

<br>

### 👌 colspan&rowspan 섞어 써보기

colspan과 rowspan을 적절히 섞어 사용하면 복잡한 형태의 표도 쉽게 만들 수 있다. colspan과 rowspan이 전진하며 차지하는 방향을 잘 생각해 보며 코드를 작성해야 한다. 위 기본 스타일 표에서 1, 2, 3, 6, 7, 8을 모두 하나로 합쳐 보겠다.

<br>

⛏ **Code**

```html
<table border="1">
        <tr>
            <td rowspan="2"
								colspan="3">
								1</td>
            <td>2</td>
            <td>3</td>
        </tr>
        <tr>
            <td>7</td>
            <td>8</td>
        </tr>
        <tr>
            <td>11</td>
            <td>12</td>
            <td>13</td>
            <td>14</td>
            <td>15</td>
        </tr>
```

<br>

🎨 **Result**

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/24e9a8b6-e7e2-46b3-b47d-37e9c65a271e/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T184140Z&X-Amz-Expires=86400&X-Amz-Signature=b422174895e25fc6f78301273880f287e50da5ba013155ca49310c0dd8b55bbe&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

위처럼 단순한 코드 조합으로 1번이 오른쪽으로 3칸, 밑으로 2칸을 차지하였다. 이처럼 rowspan과 colspan은 아주 쉽게 원하는 형태의 표를 만들 수 있도록 하는 속성이다.