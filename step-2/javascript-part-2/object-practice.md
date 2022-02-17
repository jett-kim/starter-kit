# 🖋  Object Practice

### Quiz #1

```javascript
/*

  < Object basic 1 >

  💬 를 적절한 값으로 고쳐주세요!

*/

const person = {
  age: 30,
  name: "Jett",
  address: "Seoul"
};

const name = person["name"];
const age = person.age;

const result = `${name} ${age}`;

if (result === 💬) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/gOGJjJz)



### Quiz #2

```javascript
/*

  < Object basic 2 >

  💬 를 적절한 값으로 고쳐주세요!

*/

const person = {
  age: 35,
  name: "Justin",
  address: "Busan"
};

delete person.address;

const result = person.address;

if (result === 💬) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/rNGgrEO)



### Quiz #3

```javascript
/*

  < Object basic 3 >

  💬 를 적절한 값으로 고쳐주세요!
	
  console.log(`Person age 30`);
  console.log(`Person name Jett`);
  console.log(`Person address Seoul`);
	
*/

const person = {
  age: 30,
  name: "Jett",
  address: "Seoul"
};

for (const prop in person) {
  console.log(`Person ${prop} ${💬}`);
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/gOGJjNK)



### Quiz #4

```javascript
/*

  < Personal Inforamtion >

  바닐라코딩의 전산오류로 인해 수강생의 개인정보에 오류가 생겼네요

  오류 정보의(errorInfo)의 key value 값을 수정하여 올바른 정보(correctInfo)와 

  값이 같아질 수 있도록 💬 를 적절한 값으로 고쳐주세요 !

*/

let isInfoValid = true;

const correctInfo = {
  name: "Jett",
  age: 30,
  isVacoder: true
};

const errorInfo = {
  name: "Jett",
  age: 20,
  habit: "Running",
};

errorInfo.💬 = 30;
errorInfo.💬 = true;
delete 💬;

for (const prop in errorInfo) {
  if (errorInfo[prop] !== correctInfo[prop]) {
    isInfoValid = false;
  }
}

if (isInfoValid) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/eYGajqN)

