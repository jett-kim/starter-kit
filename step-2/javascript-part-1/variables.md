# Variables

### Creating variables

우리는 생성한 값에 이름을 붙여서 사용/재사용할 수 있습니다. 이것을 가능하게 해주는 것이 바로 변수(variable)입니다. 자바스크립트에서 변수를 선언하는 방법에는 세 가지(`var`, `let`, `const`)가 있습니다. 우리는 주로 `let`과 `const`를 이용한 변수 선언을 사용할 예정입니다.

```javascript
// #1. var를 이용한 변수 선언
var one = 1;
var myFirstName = 'Ken';

// #2. let을 이용한 변수 선언
let two = 2;
let myLastName = 'Ken';

// #3. const를 이용한 변수 선언
const two = 2;
const myAge = 20;
```

> 자바스크립트에서 `=`의 의미는 `=`를 기준으로 오른쪽에 위치한 값을 왼쪽의 변수에 대입/할당 한다는 의미입니다.

### Identifiers

변수를 선언할때 지어주는 이름을 Identifier라고 부릅니다. 자바스크립트에서 Identifier는 몇 가지 규칙을 반드시 따라야합니다.

{% hint style="info" %}
* 숫자, 알파벳, `$`, `_`가 사용될 수 있다. 단, 숫자로 시작할 수는 없다.
* Javascript Keyword(Reserved Words)는 Identifier가 될 수 없다.
{% endhint %}

```javascript
let foo;  // valid
let _bar123;  // valid
let $1234337;  // valid
let 7seven;  // invalid
let function;  // invalid
```

### Reserved Words

자바스크립트 [예약어 목록](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Reserved\_Words)에 포함되어 있는 단어들은 변수명(Identifier: 식별자)로 사용이 불가능합니다.

### Key Take-aways

자바스크립트에서 `hello`라는 단어는 아무런 의미가 없는 단어입니다. 왜냐하면 Reserved Words가 아니기 때문입니다. 우리가 `hello`라는 이름의 변수를 만든다는 것은, `hello`라는 단어가 존재하도록 만들어 주는 것입니다. 선언하지 않은 변수명, Reserved Words가 아닌 단어는 기본적으로 자바스크립트에서 사용할 수 없습니다. 이 점을 반드시 명심하시기 바랍니다.

Example 1.

```javascript
alert(hello); // hello가 뭐지? 무슨 뜻인지 모르겠는데..?! -> Error
```

Example 2.

```javascript
const hello = 'Greeting!';
alert(hello); // hello가 뭐지? 아, 위에 만들어진 단어구나. hello는 'Greeting!'이라는 의미를 갖고 있구나. -> No Error
```

### 추가 학습 자료

* [Javascript Variables - W3Schools](https://www.w3schools.com/js/js\_variables.asp)
* [Data type & Variable - PoiemaWeb](https://poiemaweb.com/js-data-type-variable)
