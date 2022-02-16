# Numbers

### Numbers

자바스크립트에서 가장 흔하게 다루는 종류의 값은 바로 숫자입니다. 프로그래밍 언어에서의 숫자는 우리가 일반적으로 알고 있는 숫자와 그 성격이 사실상 동일합니다. 우리는 숫자를 이용하여 덧셈(`+`)/뺄셈(`-`)/곱셈(`*`)/나눗셈(`/`)등의 연산을 할 수 있습니다.

#### 1. 숫자를 변수에 담기

```javascript
var num = 1;
```

위 코드는 `num`이라는 변수를 생성하고, 1이라는 값을 할당하는 코드입니다. `num`이라는 변수를 생성하기 전까지는 자바스크립트에서 `num`이라는 단어는 인식되지 않는 명령어입니다. 하지만 우리가 `num`이라는 변수를 생성함으로 해서, 인식 가능한 단어로 바뀌었고 해당 단어가 의미하는 값은 `1`이 되었습니다.

#### 2. 숫자 연산하기

```javascript
var num2 = num * 2;
```

위 코드는 `num2`라는 변수를 생성하고, `num * 2`라는 값을 할당하는 코드입니다. 그렇기에 우리는 `num * 2`라는 연산을 먼저 실행한 후, 해당 값을 `num2`라는 변수에 담게됩니다. 자바스크립트가 `num`이라는 단어를 읽게 되면, 해당 단어가 무슨 뜻인지(어떤 값인지)를 판별하게 됩니다. `num`이라는 변수는 위 예제에서 `1`이라는 값을 대입해놓았습니다. 그렇기에 `num * 2`라는 코드는 `1 * 2`가 되는 것이고, 연산한다면 그 결과는 `2`가 됩니다. 고로 `num2`라는 변수에는 2가 담기게 됩니다.

위와 같이 모든 숫자는 `+`, `-`, `/`, `*`를 할 수 있습니다.

```javascript
var remainder1 = 30 % 4;
console.log(remainder);  // 2 : 30을 4로 나눈 나머지

var remainder2 = 100 % 5;
console.log(remainder2); // 0 : 100을 5로 나눈 나머지
```

위 코드에서 사용한 `%`는 Modulo Operator입니다. 이미 눈치 채 셨을 수도 있겠지만, 나머지 값을 구할 수 있는 연산 기호(연산자) 입니다.

#### 3. 연산 우선 순위

수학에서 배운 것과 동일한 방식으로 곱하기와 나누기가 더하기와 빼기보다 더 우선시 됩니다.

```javascript
var result = 3 + 7 * 2;
console.log(result); // 17
```

#### 4. 비교

아래와 같이 부등호를 이용하여 숫자의 크고 작음을 비교할 수 있습니다.

```javascript
var result = 3 > 7;
console.log(result); // false

var result2 = 3 >= 1;
console.log(result2); // true
```

#### 5. 같은 수 판별

아래와 같이 `===`를 이용하여 같은 수인지에 대한 정보를 확인할 수 있습니다.

```javascript
var one = 5;
var two = 5;

console.log(one === two); // true
```

> `==`나 `!=`는 사용하지 마시고, 항상 `===`나 `!==`를 사용하세요. 자세한 차이점은 나중에 학습하시더라도 습관은 반드시 처음부터 잡으시기 바랍니다.

#### 6. 증가시키기

```javascript
var a = 1;
a = a + 1;
```

1. 첫 번째 줄: 우리는 `a`라는 변수를 만들고 `1`이라는 값을 대입해주고 있습니다.
2. 두 번째 줄: 등호를 기준으로 오른쪽의 값을 왼쪽의 변수에 대입하고 있습니다. 그렇기에 오른쪽의 값을 **먼저** 연산하게 됩니다. 오른쪽의 값은 `1 + 1`로 결국 `2`라는 결과가 도출됩니다. 그리고 우리는 오른쪽의 변수 `a`에 `2`라는 값을 대입합니다.

위에서와 같이 `a`라는 변수의 값을 1만큼 증가시키고 싶을 때는 아래와 같이 더욱 짧게 표현할 수 있습니다.

```javascript
a += 1;  // a = a + 1
a += 2;  // a = a + 2
a -= 1;  // a = a - 1
a *= 3;  // a = a * 3
a /= 2;  // a = a / 2 

a++;     // a = a + 1
a--;     // a = a - 1
a**      // 유효하지 않은 코드
a//      // 유효하지 않은 코드
```

#### 7. 유효하지 않은 숫자 연산

만약에 아래와 같은 코드를 실행한다고 생각해보세요.

```javascript
var a = 0;
var b = 0;
var c = a / b;

console.log(c);
```

위 코드를 실행한다면, 콘솔에는 `NaN`이라는 값이 표기됩니다. 즉, `c`라는 변수에 담긴 값은 `NaN`이라는 의미입니다.

> `NaN`: "Not A Number"라는 의미를 가진 특수한 값입니다. 유효하지 않은 숫자 연산을 실행했을때 생성되곤 합니다.

만약 어떤 값이 `NaN`인지 판별하고 싶다면 아래와 같이 [isNaN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global\_Objects/isNaN)이라는 함수를 사용하여 아래와 같이 판별할 수 있습니다.

```javascript
var a = isNaN(3);
console.log(a); // false

var b = 10;
var c = isNaN(b);
console.log(c); // false

var d = NaN;
var e = isNaN(d);
console.log(e); // true
```

#### 8. 숫자 판별하기

자바스크립트에서 우리에게 주어지는 기능들 중 [typeof](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Operators/typeof)라는 연산자가 있습니다. 이 연산자는 어떤 종류의 값인지를 판별할때 사용될 수 있습니다.

```javascript
var a = typeof 10;
console.log(a);  // "number"  <- 따옴표를 잘 기억하세요. 다음 레슨에서 설명드릴 예정입니다.

var b = 20;
var c = typeof b;
console.log(c);  // "number"
```

### 추가 학습 자료

* [Javascript Numbers - W3Schools](https://www.w3schools.com/js/js\_numbers.asp)
* [Javascript Number Methods - W3Schools](https://www.w3schools.com/js/js\_number\_methods.asp)
* [Number - MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global\_Objects/Number)
