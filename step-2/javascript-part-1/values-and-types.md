# Types

프로그래밍을 하는 행위는 기본적으로 다양한 값들을 다루는 일입니다. 주어진 값을 변형하거나 조합하여 새로운 결과값을 도출하는 행위가 우리의 일상이 됩니다.

> 간단하게 설명하자면, 우리가 변수에 담을 수 있는 존재는 모두 "값"이라고 할 수 있습니다.

자바스크립트에서 우리가 다루는 값들은 여러 가지 종류가 있고, 그 종류에 따라 우리는 아래와 같이 7가지로 분류할 수 있습니다. 즉, 자바스크립트에서 모든 값들은 아래 7가지 종류 중 하나입니다.

### 1. String Type (문자열)

* 따옴표를 이용해 표현합니다.
* 문자열은 더 할 수 있습니다. 예) `"a" + "b" === "ab"`
* 문자열은 유사배열입니다.
  * Index를 이용해 각 문자열에 접근할 수 있습니다.
  * `.length` 속성이 있습니다. 예) `"abc".length === 3`

### 2. Number Type (숫자)

* 숫자는 여러분이 이미 알고 계신 그대로 숫자일 뿐입니다.
* 더하기, 빼기, 곱하기, 나누기 등의 연산이 가능합니다.
* `Infinity` 혹은 `-Infinity` 등과 같이 무한대를 표현하는 숫자값도 있습니다.
* `NaN`이라는 값 또한 숫자입니다.
  * **"Not A Number"**를 의미합니다.
  * 주로 숫자가 아닌 값을 숫자로 치환할때 의도치않게 자주 나타나는 값입니다. 예) `Number("abc")`

### 3. Boolean Type

* `true`, `false` 두 가지 값이 있습니다.

### 4. Undefined Type

* "없음"을 의미합니다.
* `undefined`라는 값이 있습니다.
* 초기값이 할당되지 않은 변수나 매개변수 등은 모두 `undefined` 값을 기본값으로 합니다.
* 객체에서 없는 속성을 접근하는 경우, `undefined` 값이 결과로 도출됩니다.

```javascript
// 초기값이 할당되지 않은 변수
let a;
console.log(a); // undefined

// 초기값이 할당되지 않은 매개변수
function foo (a, b) {
  console.log(a); // 1
  console.log(b); // undefined
}
foo(1);

// 객체에서 존재하지 않는 속성을 접근하는 경우
const something = {
  name: 'Ken'
};
console.log(something.age); // undefined
```

### 5. Null Type

* "없음"을 의미합니다.
* `null`이라는 값이 있습니다.
* 명시적으로 "값이 없음"을 나타낼때 주로 사용됩니다.
* 간혹 혼돈하시는 분들을 위해 명시하자면, `null === null` 은 `true`입니다.&#x20;
* 비록 `undefined`와 같이 "없음"을 나타내는 값일지라도, 대입한 적 없는 변수 혹은 속성과 명시적으로 "없음"을 나타내는 경우를 구분을 할 수 있어야 코드의 의미가 명확해 질 것입니다. `undefined`는 전자, `null`은 후자의 경우에 많이 쓰입니다.

```javascript
let bar = [ 1, 2, 3 ];
bar = null; // bar라는 변수에 "값이 없음"이라고 표기함
```

### 6. Object Type

* 일반 객체 뿐 아니라, 배열과 함수도 객체에 포함됩니다.

```javascript
const person = {};            // 빈 객체 생성
person.name = 'ken';        // 객체 내 Key, Value 생성
console.log(person.name);   // 'ken'
console.log(person);        // { name: 'ken' }
console.log(typeof person); // 'object'

const list = [1, 2, 3];
console.log(typeof list);   // 'object'

function foo () {}
console.log(typeof foo);    // 'function' (이상한 자바스크립트..)
```

### 7. Symbol Type (new in ES2015, the least of your concern)

* 지금은 크게 신경쓰지 마시고, 시간 나실 경우에 한번 조사해보세요.
