# Loops Practice

### Quiz #1

```javascript
/*

  < Loops basic 1 >

  💬 를 적절한 값으로 고쳐주세요!

  console.log(slogan[0]);
  console.log(slogan[1]);
  console.log(slogan[2]);
  console.log(slogan[3]);
  console.log(slogan[4]);
  console.log(slogan[5]);
  ...
  ...
  ...
  console.log(slogan[20]);
  console.log(slogan[21]);
  console.log(slogan[22]);

*/

const slogan = "Progress Not Perfection";

for (let i = 0; i < slogan.length; 💬) {
  console.log(slogan[i]);
}

alert("🎉");
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/b157e4743dd1ae297eecfc28886af5fb?editors=0010)



### Quiz #2

```javascript
/*

  < Breaking the for loop >

  바닐라코딩의 슬로건에서 문자 n을 찾아내려고 합니다.

  n을 발견하면 반복문을 멈춰주기 위해 💬 를 적절한 값으로 고쳐주세요!

*/

const slogan = "Progress, not perfection";
let result = null;

for (let i = 0; i < slogan.length; i++) {
  result = slogan[i];

  if (slogan[i] === "n") {
    💬;
  }
}

if (result === "n") {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/05435c17533bb9498b7db05ddf094c01?editors=0010)



### Quiz #3

```javascript
/*

  < Skipping the for loop >

  이번에는 n, o, t 가 나오면 반복문 실행을 건너뛰어서

  결과에 추가되지 않도록 하려고 합니다.

  💬 를 적절한 값으로 고쳐주세요!

*/

const slogan = "Progress, not perfection";
let result = "";

for (let i = 0; i < slogan.length; i++) {
  if (slogan[i] === "n" || slogan[i] === "o" || slogan[i] === "t") {
    💬;
  }

  result += slogan[i];
}

if (result === "Prgress,  perfeci") {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/34037032b1c757e8a2438974420c3963?editors=0010)



