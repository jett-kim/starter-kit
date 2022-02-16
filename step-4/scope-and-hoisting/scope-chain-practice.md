# Scope Chain Practice

### Quiz #1

```javascript
/*

  < Scope Chain basic 1 >

  💬 를 적절한 값으로 고쳐주세요!

*/

const name = "Jett";

function foo() {
  const name = "Justin";

  if (name === 💬) {
    alert("🎉");
  }
}

foo();
```

[Codepen으로 직접 해보기](https://codepen.io/vanillacoding/pen/GROJWLN)



### Quiz #2

```javascript
/*

  < Scope Chain basic 2 >

  💬 를 적절한 값으로 고쳐주세요!

*/

const name = "Jett";

function foo() {
  if (true) {
    const name = "Justin";
  }
	
  if (name === 💬) {
    alert("🎉");
  }
}

foo();
```

[Codepen으로 직접 해보기](https://codepen.io/vanillacoding/pen/QWObpPQ)



### Quiz #3

```javascript
/*

  < Scope Chain basic 3 >

  💬 를 적절한 값으로 고쳐주세요!

*/

let result = "";

function parent() {
  const role = "Parent";

  result += role;

  function child() {
    const role = "Children";

    result += role;
  }

  child();
}

parent();

if (result === 💬) {
  alert("🎉");
}
```

[Codepen으로 직접 해보기](https://codepen.io/vanillacoding/pen/dyZovEY)



### Quiz #4

```javascript
/*

  연어가 힘차게 강물을 거슬러 올라가듯,

  스코프 체인도 하위에서 상위 체인으로 거슬러 올라가며 값을 탐색합니다.

  각 river1, river2, river3 이라는 강물에 거주하고 있는 연어의 수가 다릅니다

  총 연어의 수가 몇 마리인지 💬 를 적절한 값으로 고쳐주세요!

*/

function river1 () {
  const salmon1 = 3;

  function river2 () {
    const salmon2 = 7;

    function river3 () {
      const salmon3 = 13;
      const result = (salmon1 + salmon2 + salmon3);

      if (result === 💬) {
        alert("🎉");
      }
    }
  
    river3();
  }
  
  river2();
}

river1();
```

[Codepen으로 직접 해보기](https://codepen.io/vanillacoding/pen/gOXpmNm)
