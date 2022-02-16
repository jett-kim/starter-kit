# Function

### Function(함수) 소개

함수라는 단어는 수학 시간에 이미 많이 들어보셨을 겁니다. 프로그래밍에서 함수라는 단어가 뜻하는 바도 결국 비슷한 의미입니다만, 여러 개의 코드 구문들을 하나의 단위로 묶어 실행할 수 있는 것을 의미합니다.

우리는 코드를 작성하며 여러 가지 실행문을 작성하게 됩니다. 우리가 작성하는 실행문은 반복되기도 하고 혹은 작업 내용에 따라 연관성이 생길 수도 있습니다. 이런 경우에 우리는 함수를 이용하여 조금 더 깨끗하고 정리된 코드를 작성할 수 있습니다.

#### 함수 선언

```javascript
// 함수 선언 (생성)
function add (x, y) {
  var result = x + y;
  console.log(result);
  return result;
}
```

위 코드 예제는 `add`라는 이름의 함수를 선언하는 코드입니다. 즉, `add`라는 단어의 의미가 저 함수가 되도록 설정한다는 뜻입니다. 기본적으로 자바스크립트에서 `add`라는 단어는 아무런 의미가 없는 단어입니다. 하지만 저 함수를 선언해줌과 동시에 우리는 `add`라는 단어를 사용할 수 있게 되고, 자바스크립트 실행 엔진도 `add`라는 단어가 곧 저 함수를 의미한다는 것을 알게 됩니다.

{% tabs %}
{% tab title="JavaScript" %}
```javascript
// Function Declaration (함수 선언식)
function foo () {
  // function body..
}

// Function Expression (함수 표현식)
const foo = function () {
  // function body..
};
```

Function (함수)는 위와 같이 크게 두 가지 방법으로 선언하여 만들 수 있습니다.

각자 선호하는 방식으로 선언하여 사용해도 무관하지만, 단일 프로젝트 내에서 일관된 스타일을 유지하는 것은 중요하므로, 한 가지 방식을 선택하여 사용하셔야 합니다.

또한 두 가지 선언 방식에는 **기능적인 차이**가 있습니다. 추후 알려드릴 내용이기에 자세한 내용은 설명하지 않겠지만, 기능적인 차이에 대해서는 반드시 숙지하고 있어야 합니다.
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="JavaScript" %}
```javascript
function foo () {
  for (let i = 1; i <= 3; i++) {
    console.log(i);
  }
}
```

우리는 함수 내부에 우리가 원하는 실행문을 넣을 수 있습니다.

위 예제에서 주의깊게 보셔야 할 부분은, **위 함수는 선언만 되었을 뿐 실행되지는 않았습니다.** 즉 함수를 만들어놓기는 했지만, 사용하지는 않았다는 것입니다. **함수가 실행되지 않았다는 것은 함수 내부의 코드가 실행되지 않았음을 의미합니다.**
{% endtab %}
{% endtabs %}

#### 함수 실행

{% tabs %}
{% tab title="JavaScript" %}
```javascript
function foo () {
  for (let i = 1; i <= 3; i++) {
    console.log(i);
  }
}

// 함수 실행
foo();
```

함수는 위와 같이 함수명 뒤에 소괄호(`()`)를 이용하여 실행할 수 있습니다. 함수 실행문 뒤에는 세미콜론을 붙여야 합니다.

**함수를 실행한다는 의미는 함수 내부의 코드가 실행된다는 의미입니다.**
{% endtab %}
{% endtabs %}

**함수를 "선언"하는 것과 함수를 "실행"하는 것을 혼돈하지 마세요.**

> 함수를 선언한다는 의미는 여러분이 어떤 설계도를 만들어 놓는 행위라고 생각하시면 됩니다. 함수를 실행한다는 의미는 그 설계도를 갖고 실제 작업을 진행한다는 의미입니다. 함수를 실행하기 전까지는 함수 내부의 코드 구문들은 실행되지 않습니다.

{% hint style="info" %}
자바스크립트에서 세미콜론은 필수가 아니지만, 일반적으로 세미콜론을 생략하는 경우는 잘 없습니다.

설사 세미콜론을 생략하는 방식을 선호하더라도 세미콜론을 어느 위치에 붙여야 하는지는 꼭 숙지하고 있어야 하기 때문에, 여러분께서는 바닐라코딩에서 진행하는 모든 과제 및 프로젝트는 세미콜론을 필수적으로 사용해주시기 바랍니다.
{% endhint %}

#### 매개 변수

아래에 작성된 함수 `add`를 살펴보겠습니다.

```javascript
// 함수 선언 (생성)
function add (x, y) {
  var result = x + y;
  console.log(result);
  return result;
}

// 함수 실행
add(3, 5);
```

첫 번째 줄에 보면, `add`라는 이름 오른쪽에 위치한 소괄호 안에 `x`와 `y`가 있습니다. 이것들을 우리는 **"매개 변수"**라고 부릅니다. 쉽게 생각하자면, 여러분이 작성하는 함수(설계도)에 필요한 요소들을 "정의"하는 것이라고 생각하시면 됩니다. 어떠한 요소들이 필요한 지는 상황에 따라 다르겠지만, 여러분이 작성하는 코드의 목적에 따라 자유롭게 선언하여 주시면 됩니다.

함수를 **선언**하고, 그 함수에 대한 매개 변수를 **선언**하는 것은 매개 변수의 값을 정해주지 않습니다. **매개 변수의 정확한 값은 함수를 실행하는 순간에 결정됩니다.**

위의 예제에서 `add(3, 5);`라고 함수를 실행했습니다.(함수명 뒤에 소괄호를 붙여주게 되면 함수가 실행됩니다.)

실행하는 실행문 소괄호 안에 3과 5를 쉼표로 구분하여 넣었습니다. 3이 첫번째로 들어갔기 때문에 `x`라는 매개 변수에 3이 대입되고, 5가 두 번째로 들어갔기 때문에 `y`라는 매개 변수에 5가 대입됩니다. **3과 5처럼 함수를 실행할때 넘겨지는 정보들을 인자(argument)라고 부릅니다.** 지금같은 경우, 3과 5가 `add` 함수의 인자라고 할 수 있습니다.

그리고 함수를 실행했기 때문에, 아래와 같은 함수 내부의 코드가 실행됩니다.

```javascript
var result = x + y;
console.log(result);
return result;
```

1. `result` 변수가 선언됩니다.
2. `x + y`를 연산하고 8이라는 결과를 얻습니다.
3. 8이라는 결과값을 `result` 변수에 할당합니다.
4. 콘솔에 `result` 변수의 값을 로그합니다.
5. `result` 변수의 값을 반환(return)합니다.

{% tabs %}
{% tab title="JavaScript" %}
```javascript
for (let i = 1; i <= 3; i++) {
  console.log(i);
}

for (let j = 1; j <= 5; j++) {
  console.log(j);
}

for (let k = 1; k <= 7; k++) {
  console.log(k);
}
```

여러분께서 이와 같은 코드를 작성했다고 생각해보세요.

위 예제 코드에서 중복되는 부분은 꽤 명백하게 보입니다. 중복되는 부분은 함수를 이용해 개선할 수 있습니다.

어떤 부분이 중복되고 있나요?

**반복적으로 로그를 출력하는 행위가 반복**되고 있습니다. 그렇다면 우리가 작성하는 함수는 반복문을 이용하여 로그를 출력하는 행위를 하도록 만들면 됩니다. 하지만, 반복하는 횟수(3, 5, 7)가 매번 다릅니다. 중복되는 행위 속에서 조금씩 차이가 있습니다. 이럴 경우 **우리는 함수의 "매개변수"(parameter)를 이용하여 함수 선언 시에는 결정할 수 없지만, 함수 실행 시점에 사용자(함수를 실행하는 주체)가 원하는 값으로 정확히 지정하여 사용**할 수 있도록 설정할 수 있습니다.
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="JavaScript" %}
```javascript
function repeatLog (count) {
  for (let i = 1; i <= count; i++) {
    console.log(i);
  }
}

// 1~3 출력
// repeatLog 함수 내부에서 `count`라는 변수는 3을 가르킵니다.
repeatLog(3);

// 1~5 출력
// repeatLog 함수 내부에서 `count`라는 변수는 5을 가르킵니다.
repeatLog(5);

// 1~7 출력
// repeatLog 함수 내부에서 `count`라는 변수는 7을 가르킵니다.
repeatLog(7);
```

위 예제에서 `repeatLog`라는 함수는 `count`라는 매개변수를 선언하여 사용하도록 선언되었고, 함수 실행 시에 해당 매개변수의 값을 지정하여 사용하도록 변경되었습니다.

매개변수란 말 그대로 변수입니다. 다만 함수를 선언할때 유동적으로 함께 선언해줄 수 있는 특별한 변수라고 생각하시면 좋을것 같습니다.
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="JavaScript" %}
```javascript
function foo (a, b, c, d, e) {
  // code..
}
```

매개변수는 선언할 수 있는 갯수 제한이 없습니다. 여러분이 필요한 만큼 선언할 수 있습니다.
{% endtab %}
{% endtabs %}

#### Return Statement

함수 내부에서는 `return` 구문을 사용할 수 있습니다.

반드시 항상 모든 함수에 `return` 구문이 있어야 하는 것은 아닙니다. 상황에 따라서 있을 수도 있고, 없을 수도 있습니다. 다만 `return` 구문은 몇 가지 특별한 기능이 있으니, 잘 염두하고 작업해야만 합니다.

**1. 함수 종료**

함수 내부에서 `return` 구문이 실행될 경우, 해당 함수가 종료됩니다.

```javascript
function doSomething () {
  console.log('start!');
  var a = 3;
  var b = 2;

  if (a > b) {
    console.log('a is bigger than b!');
    return;
  }

  console.log('I am the last console.log!');
}

doSomething();
```

위 예제를 실행할 경우, 세번째 콘솔 메시지는 나타나지 않습니다. 왜냐하면 `if` 구문 내부가 실행되면서 `return` 구문이 실행됐기 때문입니다. `return` 구문은 해당 함수를 종료시키게 됩니다. 현재 `return` 구문이 속해있는 함수는 `doSomething`이기 때문에 `doSomething` 함수의 모든 코드 실행은 종료됩니다.

**2. 값 반환**

`return`이라는 단어는 "반환하다"라는 의미의 영어 단어입니다. 함수를 종료하는 기능과 더불어 어떠한 값을 "반환"할 수 있게 해줍니다. 정확히 "반환"이라는게 어떤 의미인지 예제를 통해 알아보도록 하겠습니다.

```javascript
var a = 1;
console.log(a);
```

위 코드에서 우리는 `a`라는 변수에 1이라는 숫자값을 담아서 콘솔에 나타나도록 로그하였습니다. 이와 "사실상 동일한" 코드를 다른 방식으로 써보자면, 아래와 같이 표현할 수도 있습니다.

```javascript
function getA () {
  return 1;
}

var a = getA();
console.log(a);
```

위 예제의 첫번째 부분에서 우리는 `getA`라는 함수를 선언했습니다. 그리고 변수 `a`를 선언하고 `getA()`라는 값을 대입해주었습니다. 그렇다면 `getA()`라는 표현의 값은 무엇일까요?

`getA()`라는 함수 실행문을 살펴보자면, 소괄호를 이용한 것을 알 수 있습니다. 즉, `getA`가 함수여야 한다는 뜻입니다. 그리고 실제로 우리 예제 코드에서는 `getA`라는 함수가 존재합니다.

**함수 실행문이 있는 자리는 해당 함수의 반환값으로 대체됩니다.**

현재 `getA`라는 함수의 반환값은 1입니다. 왜냐하면, 함수 내부에 위치한 `return 1;`이라는 코드 때문입니다. `return`이라는 단어 뒤에 어떤 값을 작성해주게 된다면 해당 값이 함수에서 반환됩니다.

종합하여 생각해본다면, 우리 예제 코드에서 `getA()`라는 실행 구문은 `getA` 함수의 반환값(1)으로 대체되는 것입니다.

```javascript
var a = getA(); // var a = 1;
```

즉, `a`라는 변수에는 1이 대입됩니다.

그렇다면 아래와 같은 경우에는 어떻게 될까요?

```javascript
function doSomething () {
  var a = 3;
  var b = 2;

  if (a > b) {
    return;
  }

  return 3;
}

var a = doSomething();
console.log(a);
```

위 코드에서는 결과적으로 `undefined`가 콘솔에 출력됩니다.

`doSomething` 함수 내부에는 `return` 구문이 두 개 존재합니다. 하지만 두번째 `return` 구문은 실행되지 않습니다. 왜냐하면 `if` 구문 내부에 있는 첫번째 `return` 구문이 함수를 종료시키게 되기 때문입니다.

첫번째 `return` 구문을 자세히 살펴본다면, `return`이라는 단어 뒤에 그 어떤 값도 지정해주지 않았습니다. 이럴 경우, 기본적으로 `undefined`가 반환되게 됩니다. 이와 마찬가지로 `return`되는 값을 지정해주지 않고 종료되는 함수의 경우에도 기본적으로 `undefined`가 반환되게 됩니다.

{% tabs %}
{% tab title="JavaScript" %}
```javascript
function foo (a, b) {
  if (a < b) {
    return a;
  }
}

const result1 = foo(10, 20);
const result2 = foo(20, 20);

console.log(result1); // ?
console.log(result2); // ?
```

함수에 `return` 구문이 없거나 실행되지 않을 경우, `undefined`가 결과값이 됩니다.
{% endtab %}
{% endtabs %}

### 추가 학습 자료

* [Functions - W3Schools](https://www.w3schools.com/js/js\_functions.asp)
* [Functions - Learn-js](https://www.learn-js.org/en/Functions)
* [Functions - Javascript Info](https://javascript.info/function-basics)
* [Functions - MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Functions)
* [Functions - Eloquent Javascript](https://eloquentjavascript.net/03\_functions.html)
