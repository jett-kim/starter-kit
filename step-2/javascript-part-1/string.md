# String

### 1. 문자열(String) 소개

이전 레슨에서 잠시 보여드렸던 코드를 다시 한번 보여드리겠습니다.

```javascript
var a = typeof 3;
console.log(a); // "number"
```

위 코드 예제에서 `a` 변수에 담기는 값은 `"number"`라는 값입니다. 따옴표로 감싸져 있는 number라는 텍스트입니다. 단순히 텍스트 값들을 저장하는 것이라고 생각하시면 됩니다. 자바스크립트에서 이런 종류의 값들은 문자열 혹은 String(스트링)이라고 부릅니다.

다시 한번 위 예제에서 콘솔에 나타나는 값을 정의하자면, number라는 문자열이라고 말할 수 있습니다.

```javascript
var number = 30;
var something = typeof number;

console.log(number === something); // false
```

* 위 코드 첫 번째 줄에서 `number`라는 변수에 30이라는 값을 담습니다.
* 두 번째 줄에서는 `number`라는 변수에 담겨있는 값의 종류를 담습니다. `typeof` 연산의 결과값은 항상 문자열입니다. 현재 예제에서는 `"number"`가 됩니다.
*   마지막 줄에서는 `number`라는 변수의 값과 `something`이라는 변수의 값을 비교합니다. `number`라는 변수에 담긴 값은 숫자 30이고, `something`이라는 변수에 담긴 값은 문자열 `"number"`입니다. 고로 `30 === "number"`를 비교하는 것이고, 두 가지 값은 다르기 때문에 결과적으로 콘솔에는 `false`가 나타나게 됩니다.

    > 따옴표에 감싸져 있는 문자열 `"number"`와 변수 `number`의 차이를 확실히 판별할 수 있으셔야 합니다. 문자열을 사용할 때는 쌍따옴표나 홑따옴표를 선택적으로 사용할 수 있습니다.

### 2. 문자열 붙이기

```javascript
var s1 = "something";
var s2 = "else";
var result = s1 + s2;

console.log(result); // "somethingelse"
```

위와 같이 우리는 문자열을 붙일 수 있습니다. 숫자들을 더할 때와 마찬가지로 `+` 기호를 사용하지만, 문자열에서는 더한다는 의미보다는 붙인다는 의미가 더 적절할 것 같습니다.

### 3. 문자열 비교

문자열은 아래와 같이 같고 다름을 비교할 수 있습니다.

```javascript
var s1 = "abc";
var s2 = "abc";

var result1 = s1 === s2;  // s1과 s2가 같은지 확인하고 그 결과를 result1 변수에 담습니다.
console.log(result1); // true


var s3 = "abc ";  // 유의: 문자열 끝자리에 공백이 붙어있습니다.
var s4 = "abc";

var result2 = s3 !== s4;  // s3과 s4가 다른지 확인하고 그 결과를 result2 변수에 담습니다.
console.log(result2); // true
```

### 4. 문자열 길이

`.length`를 이용하여 모든 문자열은 그 길이에 대한 정보를 알 수 있습니다.

```javascript
var str1 = "abc";  // 3개의 텍스트를 포함하고 있는 문자열
console.log(str1.length); // 3

var str2 = "   ";  // 공백 3개
console.log(str2.length); // 3

console.log("graph-ql".length); // 8
```

### 5. 문자열 인덱스

문자열 종류의 값들은 인덱스 정보를 이용할 수 있습니다. 인덱스라는 정보는 간략하게 말하면 위치/순서를 의미하는 것과 비슷하다고 생각하시면 됩니다. `"abcdef"`라는 문자열이 있다면, a - b - c - d - e - f의 순서로 만들어져 있습니다. 이런 정보를 담고 있는 것이 인덱스입니다.

한 가지 명심할 점은, 인덱스는 항상 0부터 시작하게 됩니다. 위의 `"abcdef"` 문자열을 예로 보면, 0번째 인덱스에는 a라는 문자가 있고, 1번째 인덱스에는 b, 2번째 인덱스에는 c, ... , 5번째 인덱스에는 f가 있는 것입니다.

코드 상으로는 아래와 같이 인덱스를 이용할 수 있습니다.

```javascript
var str = "abcdef";
console.log(str[0]); // "a"

console.log("cde"[2]); // "e"
```

### 6. 문자열 메서드

문자열에는 다양한 기능(메서드)가 있습니다. 메서드가 무슨 뜻인지 아직 정확히 모르더라도, **아래 코드들을 하나씩 콘솔에서 실행시켜보며 각 메서드가 어떤 기능을 하는지에 대해 자세히 살펴보시기 바랍니다.**

```javascript
'6'.repeat(3);
'hi ken'.includes(' ke');
'what are you doing?'.startsWith('what ');
'I am doing FiNe'.endsWith('iNe');
'Are you sure?'.indexOf(' yo');
'Yeah I am sure'.slice(2, 5);
'I?doubt?that'.split('?');
'Why would you doubt my word?'.split('');
'You hAve BeEn DiSHonest'.toLowerCase();
'No wAy!'.toUpperCase();
```

### 추가 학습 자료

* [Javascript String - W3School](https://www.w3schools.com/jsref/jsref\_obj\_string.asp)
* [Javascript String Methods - W3Schools](https://www.w3schools.com/js/js\_string\_methods.asp)
* [문자열 제대로 다루기 - MDN](https://developer.mozilla.org/ko/docs/Learn/JavaScript/First\_steps/Useful\_string\_methods)
