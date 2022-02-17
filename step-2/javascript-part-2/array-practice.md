# 🖋  Array Practice

### Quiz #1

```javascript
/*

  < Arrays basic 1 >

  💬 를 적절한 값으로 고쳐주세요!

*/

const fruitList = ["Apple", "Lemon", "Banana", "Melon"];
const fruitLength = fruitList.length;

if (fruitLength === 💬) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/mdBYjLB)



### Quiz #2

```javascript
/*

  < Arrays basic 2 >

  💬 를 적절한 값으로 고쳐주세요!

*/

const foodList = ["Pizza", "Hamburger", "Chicken", "Steak"];

const food1 = foodList[0];
const food2 = foodList[foodList.length - 1];

const result = food1 + food2;

if (result === 💬) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/eYGajrq)



### Quiz #3

```javascript
/*

  < Arrays basic 3 >

  💬 를 적절한 값으로 고쳐주세요!

*/


const fruitList = ["Apple"];

fruitList.push("Lemon");
fruitList.push("Mango");

const fruit1 = fruitList[1];
const fruit2 = fruitList.pop();

const result = fruit1 + fruit2;

if (result === 💬) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/zYEQLLG)



### Quiz #4

```javascript
/*

  < Arrays basic 4 >

  💬 를 적절한 값으로 고쳐주세요!

*/

const animalList = ["Dog", "Cat", "Lion", "Koala"];
let result = "";

for (let i = 0; i < animalList.length; i++) {
  result += 💬;
}

if (result === "DogCatLionKoala") {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/oNGRMMB)



### Quiz #5

```javascript
/*

  음료 자판기(machine)에 4가지 종류의 음료 중에 "Sprite"가 빠져있네요

  창고(storage)에서 부족한 음료의 종류를 찾아 자판기의 마지막 요소로 채워질 수 있도록

  💬 를 적절한 값으로 고쳐주세요!

*/

const machine = ["Coke", "Pepsi", "Fanta"];
const storage = ["Pepsi", "Coke", "Sprite", "Fanta"];

for (let i = 0; i < storage.length; i++) {
  if (machine.indexOf(storage[i]) === 💬) {
    machine.push(storage[i]);
  }
}

const result =  machine[machine.length - 1];

if (result === "Sprite") {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/MWEdBBM)

