# Logical Operators Practice

### Quiz #1

```javascript
/*

  < Logical operators basic 1 >

  💬 를 적절한 값으로 고쳐주세요!

*/

const seven = 7;
const trueOrFalse = !!"";

const result = (seven && trueOrFalse);

if (result === 💬) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/02028834dbdfd5267d841e332f040809?editors=0010)



### Quiz #2

```javascript
/*

  < Logical operators basic 2 >

  💬 를 적절한 값으로 고쳐주세요!

*/

const empty = null;
const trueOrFalse = !0;
const str = "Vanillacoding";

const result = (empty || trueOrFalse || str);

if (result === 💬) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/ced6acd5a93e18a273b931dd8309da15?editors=0010)



### Quiz #3

```javascript
/*

  < Logical operators basic 3 >

  💬 를 적절한 값으로 고쳐주세요!

*/

const trueOrFalse = !null;
const zero = 0;
const str = "Vanillacoding";

const result = (trueOrFalse && zero && str);

if (result === 💬) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/98b6514ef92496137c7af9d42ae3ea3e?editors=0010)



### Quiz #4

```javascript
/*

  Ken은 토론회에 참석하였습니다.

  두 가지 의견의 토론 결과는 logical operator에 따라 결정됩니다.

  토론의 최종 결과가 truthy 값이 되도록 💬 를 적절한 값으로 고쳐주세요!

*/

const Ryan = false;
const Blake = true;
const Scott = false;
const Ken = true;

const result = (Ryan || Blake) 💬 (Scott && Ken);

if (result) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/9b2fb3a309605e295f86d173749d71d9?editors=0010)



