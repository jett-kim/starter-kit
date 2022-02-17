# 📗  null & undefined

자바스크립트에는 `null`과 `undefined`라는 값이 존재합니다.

두 가지 모두 무언가 "없다"라는 표현을 할 때 사용되곤 합니다. 비슷한 의미를 가진 값이지만, 자바스크립트 개발자들은 보통 두 가지의 용도를 구분해서 사용합니다.

```javascript
const nothing1 = null;
console.log(nothing1 === null); // true

const nothing2 = undefined;
console.log(nothing2 === undefined); // true

console.log(nothing1 === nothing2); // false
```

### `undefined` vs `null` 용도의 차이

`undefined`라는 단어의 의미는 말 그대로, "정의되지 않음"이라는 뜻입니다. 예를 들면, 우리가 어떤 변수를 만들고 그 값을 정의해주지 않았을때 사용되곤 합니다. 값이 대입되지 않은 상태를 위해 많이 사용됩니다.

```javascript
// 변수를 생성하고, 아무 값도 지정(정의)해주지 않았습니다.
let k;
console.log(k); // undefined

// 위의 코드처럼 아무 값도 대입해주지 않으면 기본으로 undefined라는 값이 대입되기 때문에,
// 아래 코드처럼 undefined를 명시적으로 대입해주는 코드는 잘 사용하지 않습니다.
let o = undefined;
console.log(o); // undefined
```

`null`이라는 값은 `undefined`와는 다르게 **의도적으로** 값이 없음을 표현하고 싶을때 대입해주곤 합니다.

```javascript
let title = "Bootcamp";

// 위 title를 이용한 작업을 실행함.. Blah Blah....

// title를 이용한 작업이 모두 종료되고,
// 더 이상 사용하지 않을 계획이라 title를 의도적으로 없다고 표현함
title = null;
```

### 추가 학습 자료

* [null - MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global\_Objects/null)
* [undefined - MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global\_Objects/undefined)
