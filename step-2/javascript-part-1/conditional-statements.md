# Conditional Statements

### 조건문 소개

자바스크립트에서 우리는 어떤 조건에 의해 코드의 실행을 제어할 수 있습니다. 우선 아래의 예제를 볼까요?

```javascript
if (false) {
  console.log("Hello, World!");
}
```

위 코드를 실행하게 되면, 콘솔에 아무런 메시지도 나타나지 않습니다. `if` 구문이 주어진 조건에 의해 중괄호(`{}`) 내부 코드의 실행을 제어한 것입니다. 만약 위 코드의 조건이 `false`가 아니라 `true`였다면, 중괄호 내부 코드가 실행되었을 것입니다.

위와 같이 우리는 어떤 조건에 의해 코드의 실행을 제어하고 싶을때 `if` 구문을 사용할 수 있습니다.

```javascript
if (/* 조건 */) {
  // 실행문
}
```

### 기본 사용법

`if`라는 영어 단어가 뜻하듯 "만약에 A라면 B를 해주세요."라고 컴퓨터에게 명령을 내릴 수 있는 것입니다.

조금 더 생각을 해본다면, 아래와 같은 표현을 하고 싶을 수도 있습니다.

**"만약에 A라면 B를 해주세요. 그런데 만약에 C라면 D를 해주세요. 아니면 그냥 E를 해주세요."**

위와 같은 표현은 아래처럼 작성할 수 있습니다.

```javascript
// 아래의 코드에서 A와 C라는 것은 정의되지 않았기 때문에, 정상적으로 실행되지 않습니다. 비유적으로 A와 C의 존재가 있는 상황을 가정하여 작성한 것입니다.

if (A) {
  // B..
} else if (C) {
  // D..
} else {
  // E..
}
```

### 조건문의 중첩

`if` 구문은 여러분이 원하는 대로 중첩시켜서 사용하실 수 있습니다.

```javascript
var something = true;
var moreSomething = true;

if (something) {
  console.log("I am inside something");

  if (moreSomething) {
    console.log("I am inside moreSomething");
  } else {
    console.log("I never gets called.");
  }
} else {
  console.log("I never gets called either.");
}
```

### 유의할 점

만약 `if..else` 구문을 이용하여 아래와 같은 코드를 작성했다고 생각해보세요.

```javascript
if (A) {
  // one..
} else if (B) {
  // two..
} else if (C) {
  // three..
} else if (D) {
  // four..
} else if (E) {
  // five..
} else {
  // six..
}
```

위의 `if..else if`에서 보면, 6가지 조건이 있습니다. `A ~ E` 그리고 `else`가 있습니다.

유의하실 점은 항상 저 조건들 중, _단 한 가지의 조건부 코드만 실행된다는 것입니다._ 설사 A와 C가 모두 참이라 해도, A 조건에 해당하는 코드만 실행되고 C 조건에 해당하는 코드는 실행되지 않습니다. 이것은 `else if`라는 구문 때문입니다. `else`라는 단어는 "아니면\~"이라는 뜻이기 때문입니다.

### 퀴즈

{% tabs %}
{% tab title="JavaScript" %}
```javascript
// #1. 무엇이 출력될까요?
if (true) {
  console.log(1);
} else if (true) {
  console.log(2);
} else {
  console.log(3);
}

// #2. 무엇이 출력될까요?
if ("") {
  console.log(1);
} else if ("a") {
  console.log(2);
} else {
  console.log(3);
}

// #3. 무엇이 출력될까요?
if (null) {
  console.log(1);
} else if (5) {
  console.log(2);
} else {
  console.log(3);
}
```

Truthy 값이 조건으로 주어질 경우, 해당 조건문이 실행되고 그렇지 않을 경우 다음 조건으로 넘어갑니다.
{% endtab %}
{% endtabs %}

### 추가 학습 자료

* [if..else - MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/if...else)
* [switch - MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/switch) (`if` 구문과 비슷한 기능을 하는 `switch` 구문입니다. 한번 살펴보세요.)
* [Control Flow - PoiemaWeb](https://poiemaweb.com/js-control-flow#21-ifelse-%EB%AC%B8)
* [if..else - W3Schools](https://www.w3schools.com/js/js\_if\_else.asp)
