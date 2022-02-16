# Scope Introduction

{% hint style="danger" %}
Scope 관련 예제에서는 개념 설명을 위해 `var` 변수 선언 만을 이용하고 있습니다. `let`과 `const` 또한 기본적으로 유사하게 동작합니다만, 우선은 `var`를 기준으로 먼저 설명하고 추후 `let`과 `const`에 대해 설명하도록 하겠습니다.
{% endhint %}

### Definition

{% hint style="info" %}
Scope란, 우리가 작성하는 **코드의 접근 범위를 결정하는 개념**입니다.
{% endhint %}

예제 코드를 먼저 보여드리겠습니다.

{% tabs %}
{% tab title="JavaScript" %}
{% code title="Example 1" %}
```javascript
function foo () {
  var a = 1;
  
  console.log(a); // 로그 #1
}

foo();
```
{% endcode %}
{% endtab %}
{% endtabs %}

#### Execution Order Summary

위 예제 코드를 실행 순서에 따라 정리해보자면 아래와 같습니다.

1. **\[Line 1-5]** `foo` 함수를 생성합니다.
   1. 주의) Line 2-4는 `foo` 함수를 호출하기 전까지 실행되지 않습니다. 단지, `foo` 라는 함수의 존재에 대해 인식하게 되는 과정입니다.
2. **\[Line 7]** `foo` 함수를 실행합니다.
3. **\[Line 2]** `a` 라는 변수를 선언(생성)하고 1이라는 값을 해당 변수에 할당합니다.
4. **\[Line 4]** `a` 라는 변수를 출력하는 구문이 실행됩니다.
5. **\[Line 4]** 성공적으로 출력하기 위해서는 **** `a` 라는 변수의 존재를 찾아야 합니다.
6. **\[Line 2]** `a` 라는 변수가 선언된 것을 찾고, 그에 할당된 1이라는 값을 이용하게 됩니다.
7. **\[Line 4]** 1이라는 값이 성공적으로 출력됩니다.
8. **\[Line 4]** `foo` 함수의 실행문이 종료됩니다.
9. **\[Line 7]** `foo` 함수의 실행이 종료되었고, 더 이상 실행할 실행문이 없으므로 우리 프로그램은 종료됩니다.

### Function Scope

위 예제 코드의 Scope를 한번 살펴보도록 하겠습니다.

{% tabs %}
{% tab title="JavaScript" %}
{% code title="Example 1" %}
```javascript
function foo () {
  /* --- foo scope start --- */
  var a = 1;
  
  console.log(a); // 로그 #1
  /* --- foo scope end   --- */
}

foo();
```
{% endcode %}
{% endtab %}
{% endtabs %}

`var` 를 이용하여 선언한 변수는 **함수를 기준으로** 접근 범위가 결정됩니다.

#### Variable Scope Details

위 예제에서 우리는 `foo`라는 함수를 만들었습니다. 그리고 그 함수의 내부에서 변수 `a` 를 선언하였습니다. 현재 `a` 라는 변수를 사용하려고 시도한 곳은 "로그 #1" 부분입니다.

#### \[ 로그 #1 ]

"로그 #1"에서는 `a` 라는 변수의 값(1)이 성공적으로 출력됩니다. 그 이유는 자바스크립트에서 `var` 를 이용하여 선언한 변수는 **해당 변수 선언문을 감싸고 있는 함수를 기준으로 접근 범위가 설정되고 그 범위 내부에서는 자유롭게 접근하여 사용할 수 있기 때문**입니다.

위 예제 코드에서 **"foo scope start"** 부분부터 **"foo scope end"** 부분 내에서는 언제든지 자유롭게 `a` 라는 변수에 접근하여 사용이 가능한 것입니다. **이 부분을 우리는 `foo` 함수 Scope라고 부를 수 있습니다.**
