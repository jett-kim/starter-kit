# 🖋  Hoisting Practice

### Quiz #1

```javascript
/*

  < Hoisting basic 1 >

  💬 를 적절한 값으로 고쳐주세요!

*/

function foo() {
  if (result === 💬) {
    alert("🎉");
  }

  var result = "something"; // const, let, var의 차이는 무엇일까요 ?
}

foo();
```

[Codepen으로 직접 해보기](https://codepen.io/vanillacoding/pen/QWObpem)



### Quiz #2

```javascript
/*

  < Hoisting basic 2 >

  💬 를 적절한 값으로 고쳐주세요!

*/

let aomething = "Something";
let result = null;

function foo () {
  if (something === "Something") {
    result = "Is something";
  }
  
  var something = "Else";
}

foo();

if (result === 💬) {
  alert("🎉");
}
```

[Codepen으로 직접 해보기](https://codepen.io/vanillacoding/pen/abVOJee)



### Quiz #3

```javascript
/*

  아래 코드에서 "bar 🎉" 성공 알림창 나타날 수 있도록 만들어주세요!

*/

foo();
bar(); // bar 함수 실행문의 위치를 옮겨주세요.

function foo() {
  console.log("foo 🎉");
}

const bar = function () {
  alert("bar 🎉");
};
```

[Codepen으로 직접 해보기](https://codepen.io/vanillacoding/pen/ZEaGKzV)
