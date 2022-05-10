# 👍 반복문의 종류

반복문에는 총 다섯 가지의 종류가 있다.

>for문<br>
while문<br>
do while문<br>
for/in문<br>
for/of문

<br>

## 👍 for문이란?

기본적으로 for문 선언은 `for(let i=0; i<10; i++){}`의 형식으로 한다. 이 뜻은 i가 0이며, i는 10보다 작고 i를 1씩 더하여 i가 9가 될 때까지 1을 더하는 것을 반복하겠다는 의미이다.

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/f622b3a6-0582-4406-97db-1cf99101b69d/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T192855Z&X-Amz-Expires=86400&X-Amz-Signature=6ece0eced1fe0e48c151f97124e46021adc233172ff1e58004c614ab5b743cc8&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

위의 예시를 토대로 설명하면, let i=0은 초기식에 해당되며, 표현식은 i<10에 해당되고 증감식은 i++에 해당된다. 여기서 명령문이란 중괄호{} 안에 포함되어 있는, 표현식의 결과가 참인 동안 반복적으로 실행하고자 하는 실행문이다. for문을 사용했을 때에는 어떠한 상황보다 더 간결한 반복문을 작성할 수 있어 간편하다는 장점이 있다.

<br>

## 👍 while문이란?

while문이란 특정 조건을 만족할 때까지 계속해서 주어진 실행문을 반복 실행하는 반복문이다. while문은 선언할 때 초기식과 증감식을 사용하지 않는데, while문은 우선 표현식이 참인지를 판단하여 참이면 내부의 실행문을 실행한다. 내부의 실행문을 전부 실행하고 나면, 다시 표현식으로 돌아와 또 한 번 표현식이 참인지를 판단하게 된다.

```jsx
let i=1; //i의 초기값 선언
while(i<10) { //i가 10보다 작을 경우 while문 반복
//실행문
i++ // false값을 나타내기 위한 표현식
}
```

![Untitled](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/a1fa31d8-6112-4f5a-8d06-c314bbea8466/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220510%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220510T192905Z&X-Amz-Expires=86400&X-Amz-Signature=a5ee457fa8b7e8d212c4b6ab8cce5ebe7ceae559e4e87e1f0f31fc8aadfe2275&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

while문은 표현식의 결과를 변경하는 실행문이 존재하지 않을 경우 프로그램은 루프를 영원히 반복하게 되기 때문에, while문을 사용할 때에는 표현식의 결과가 어느 순간에는 거짓을 갖도록 표현식을 변경하는 실행문을 반드시 포함하여야 된다.