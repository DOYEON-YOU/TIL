# 👍 예제를 통한 응용방법 #1

```coffeescript
<script>

// object와 fuction의 작성법을 잘 구분해야 한다.
let getData = function () {
     let obj = {
          // object의 작성법인 key : value, 만 지켜주면 된다.
          num: 1,
          name: "권도연",
          sing: function () {
               alert("노래해요!");
          } //세미콜론 붙이면 안 됨.
     };
     return obj;
};

//a에는 object type의 참조값이 들어 있다
let a = getData();
//b에도 object type의 참조값이 들어 있다
let b = getData();
//실제로 a와 b는 각자 다른 데이터를 가지고 있고 주소만 같은 것이기 때문에 다르다.
let result = a == b; // false

</script>
```

위 예제를 살펴보면 `getData라는 변수`에 익명함수를 담고 그 안에 obj라는 object type을 넣어 주었다. `a라는 변수에 getData 함수를 호출`하고, `b라는 변수에 getData 함수를 호출`하였을 때 a와 b는 똑같은 값을 가지지만 각 변수는 `다른 데이터를 가지고 있다.` getData(); 라는 데이터를 표현하는 주소의 방식만 같은 것이지, getData()를 불러오기 위한 데이터는 따로 저장되는 것을 잊으면 안된다.

<br>

---

# 👍 예제를 통한 응용방법 #2

```coffeescript
<script>
    // 함수 안에 배열이 있고 배열 안에 오브젝트가 있다.
    // getFriends()[0].num => 함수 안에 배열이 있고 배열 안에 오브젝트가 있고 오브젝트 안에 문자열이 있음.
    let getFriends = function () {
         let friends = [];
         //push를 사용해 friends라는 배열에 세 가지의 오브젝트를 넣은 것이다.
         friends.push({
              num: 1,
              name: "권도연",
              addr: "서울시"
         });
         friends.push({
              num: 2,
              name: "장준",
              addr: "강남구"
         });
         friends.push({
              num: 3,
              name: "땃쥐",
              addr: "개포동"
         });
         return friends;
         // friends라는 변수 안에 들어있는 배열의 참조값을 반환해준다는 의미이다.
         // 배열을 반환해준 것
    };

    //a는 array type
    let a = getFriends();

    // getFriends라는 key에 getFriends라는 value를 넣은 것이다.
    // value getFriends는 function type이다.
    let util = {
         getFriends: getFriends
    };
</script>
```

<br>


getFriends라는 변수에 익명함수를 넣어 friends라는 배열을 만든 후 push를 이용해 friends라는 배열에 세 가지의 오브젝트를 넣은 것이다. 이 배열은 총 세 개의 오브젝트가 들어가 세 명의 정보를 나타낼 수 있다. 마지막 return friends; 로 인해 아래와 같이 getFriends() 를 호출했을 때 friends 배열의 값들이 콘솔창에 나타나게 된다.

![Untitled](https://ifh.cc/g/kAxQk2.png)

<br>

friends 배열을 반환값에 넣었기 때문에 getFriends()를 호출하였을 때 friends 배열이 나온다. 그렇기에 a라는 변수를 만들어 getFriends라는 함수를 호출하였을 때도 콘솔창에 a를 입력하면 총 세 개의 배열이 입력되며, a[0]과 같이 인덱스를 불러올 수 있는 것이다.

![Untitled](https://ifh.cc/g/xQngwb.png)

<br>

util이라는 변수에는 key:value 의 모습을 한 Object type으로 작성이 되어 있다. Object type이기 때문에 getFriends라는 Object를 만들어 getFriends라는 함수를 참조한 것이기 때문에, util이라는 변수를 콘솔 창에 불러왔을 때에는 아래와 같은 결과를 띄게 된다.

![Untitled](https://ifh.cc/g/ky2oHa.png)