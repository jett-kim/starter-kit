# Function Practice

### Quiz #1

```javascript
/*

  < Function basic 1 >

  💬 를 적절한 값으로 고쳐주세요!

*/

function sayHello(name) {
  return `Hello, ${💬}`;
}

const result = sayHello("Jett");

if (result === "Hello, Jett") {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/ff557febf996cb0a0b8b3e5ee0b72975)



### Quiz #2

```javascript
/*

  < Function basic 2 >

  💬 를 적절한 값으로 고쳐주세요!

*/

function greetingMaker(greet, name) {
  return `💬`;
}

const hello = greetingMaker("Hello", "Jett");
const goodBye = greetingMaker("Goodbye", "Justin");

const result = (hello === "Hello, Jett") && (goodBye === "Goodbye, Justin");

if (result) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/xxXNJLG)



### Quiz #3

```javascript
/*

  < Function basic 3 >

  💬 를 적절한 값으로 고쳐주세요!

*/

function findStaff(name) {
  if (name === "Jett") {
    return "Staff";
  }

  if (name === "Leo") {
    return "Staff";
  }

  return "Spy";
}

const isFound1 = findStaff("Leo");
const isFound2 = findStaff("Jett");

const result = (isFound1 === isFound2);

if (result === 💬) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/zYEQLEO)



### Quiz #4

```javascript
/*

  < Making Hamburger with Functions >

  햄버거를 만들어 먹으려고 합니다. 현재는 토마토가 빠져있네요 🍅

  완성된 햄버거와 동일하도록 💬 를 적절한 내용으로 고쳐주세요!

*/

let myBurger = "Hamburger";

const addCheese = function (burger) {
  const cheese = " with Cheese";

  return burger + cheese;
};

const addPatty = function (burger) {
  const patty = " with Patty";

  return burger + patty;
};

const addTomato = 💬;

myBurger = addCheese(myBurger);
myBurger = addPatty(myBurger);
myBurger = addTomato(myBurger);

if (myBurger === "Hamburger with Cheese with Patty and Tomato") {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/53d82a88cffdcd23fbb84e54b7df74ce)



### Quiz #5

```javascript
/*

  < Simple subtraction function >
  
  두 가지 인자를 받아 큰 수에서 작은 수를 빼주는 함수를 작성해주려고 합니다. 

  아래 조건이 통과할 수 있도록 💬 를 적절한 내용으로 고쳐주세요!

*/

const subtraction = 💬;

const sum1 = subtraction(10, 3);
const sum2 = subtraction(7, 12);

const result = sum1 + sum2;

if (result === 12) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/jOGopZQ)

