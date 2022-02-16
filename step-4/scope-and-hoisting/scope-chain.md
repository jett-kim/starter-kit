# Scope Chain

### Example 1

아래 코드를 한번 살펴보세요.

{% tabs %}
{% tab title="JavaScript" %}
{% code title="Example 1" %}
```javascript
var a = 1;

function foo () {
  console.log(a); // 로그 #1
}

foo();
```
{% endcode %}

#### Execution Order Summary

1. \[Line 1] 변수 `a`를 선언하고 1이라는 숫자값을 해당 변수에 할당합니다.
2. \[Line 3-5] 함수 `foo`를 생성합니다. (`foo`라는 단어는 이제 이 함수를 가르키게 됩니다.)
3. \[Line 7] 함수 `foo`를 실행합니다.
4. \[Line 4] `foo` 함수 내부 코드가 실행됩니다.
5. \[Line 4] `a`를 출력합니다.
   * 변수 `a`의 값을 출력하기 위해 `a`라는 변수의 값을 찾습니다.
   * 현 실행문(`console.log(a);`)와 같은 Scope인 `foo` 함수 Scope 내부에서 먼저 `a`라는 변수를 찾습니다만, `a`를 찾지 못합니다.
   * `foo` 함수 Scope에서 한 단계 바깥 Scope로 나가서 `a`라는 변수를 찾습니다. (아래 그림 참고)
   * Line 1에서 `a`라는 변수가 선언된 것을 찾고, 그에 해당하는 값인 1을 사용할 수 있습니다.
   * `a`의 값인 1을 출력하게 됩니다.
6. \[Line 4] `foo` 함수의 실행이 종료됩니다.
7. \[Line 7] `foo` 함수 실행문의 종료를 끝으로 우리 프로그램도 종료됩니다.
{% endtab %}
{% endtabs %}

### Scope Chain

![https://www.learnsimpli.com/scope-chain-in-javascript/](../../.gitbook/assets/3-2.png)

Scope란 위 그림처럼 계층 구조로 형성됩니다. 어떤 함수로도 둘러싸여 있지 않은 가장 최상위 Scope는 Global Scope라고 부릅니다. 그리고 그 하위엔 함수 생성을 기준으로 Scope가 형성됩니다.

위 그림에서는 가장 최상위에 Global Scope가 존재하고, 그 하위에 `Person` 함수 Scope가 존재하고, `Person` 함수 Scope 내부에 `displayName`이라는 함수의 Scope가 존재합니다.

**\[상위]** `Global Scope` - `Person Scope` - `displayName Scope` **\[하위]**

**이런 Scope 계층에서 가장 중요한 특징은 상위에서 하위 Scope 내부 정보를 접근할 수 없다는 점입니다. 하위에서 상위 Scope의 정보는 접근 가능합니다.**

**그리고 실행문의 위치를 기준으로 하위 Scope부터 시작하여 원하는 값을 찾을때까지 상위로 탐색합니다.**

추가 예제와 함께 더 자세히 살펴보도록 하겠습니다.

### Example 2

{% tabs %}
{% tab title="JavaScript" %}
{% code title="Example 2" %}
```javascript
var a = 1;

function foo () {
  var a = 2;
  console.log(a); // 로그 #1
}

foo();
```
{% endcode %}

위 예제에서 Line 5의 콘솔 메시지는 어떤 값을 출력할까요? 정답은 **2**입니다.

어떤 변수에 대한 정보를 필요로 할때 자바스크립트는 현 실행문의 위치를 기준으로 하위 Scope부터 시작하여 해당 변수의 값을 찾아나갑니다.

#### Execution Order Summary

* Line 5에서 `a`라는 메시지를 출력하는 실행문이 실행됩니다.
* 현 실행문의 위치는 Line 5입니다. 즉, `foo` 함수 Scope 내부에서 시작하여 해당 변수를 찾기 위한 탐색이 시작됩니다.
* `foo` 함수 Scope 탐색 결과, Line 4에 있는 (값이 2인) `a` 변수를 찾습니다.
* Line 5의 콘솔 출력문은 2를 출력합니다.
{% endtab %}
{% endtabs %}

### Example 3

{% tabs %}
{% tab title="JavaScript" %}
{% code title="Example 3" %}
```javascript
var a = 1;

function foo () {
  var a = 2;
  console.log(a); // 로그 #1
}

foo();
console.log(a);   // 로그 #2
```
{% endcode %}

위 예제에서 Line 5와 9의 콘솔 메시지는 어떤 값을 출력할까요? 정답은 **2**와 **1**입니다.

#### Execution Order Summary  - Line 5

* Example 2의 예제 코드와 동일한 이유로 2가 출력됩니다.

#### Execution Order Summary - Line 9

* 현재 실행문의 위치는 Global Scope입니다. 그리하여 자바스크립트는 Global Scope를 시작점으로 하여 `a` 변수의 위치를 찾습니다. (더 이상 탐색할 상위 Scope는 존재하지 않습니다.)
* Line 1에 `a` 변수가 선언되어 있음을 찾고, 1이라는 값임을 알게 됩니다.
* Line 9의 콘솔 메시지는 1을 출력하게 됩니다.

상위 Scope에서 하위 Scope 내부 정보를 탐색할 수는 없습니다. 즉, Line 1의 `a` 변수 선언문이 없었다고 하더라도 Line 4의 `a` 변수 정보를 찾을 수는 없는 상황이었습니다.
{% endtab %}
{% endtabs %}

### Example 4

{% tabs %}
{% tab title="JavaScript" %}
{% code title="Example 4" %}
```javascript
function foo () {
  var a = 2;
  console.log(a); // 로그 #1
}

foo();
console.log(a);   // 로그 #2
```
{% endcode %}

위 예제에서 Line 3와 7의 콘솔 메시지는 어떤 값을 출력할까요? 정답은 **2**와 **에러**입니다.

#### Execution Order Summary - Line 3

* Example 2, 3의 예제 코드와 동일한 이유로 2가 출력됩니다.

#### Execution Order Summary - Line 7

* 현재 실행문의 위치는 Global Scope입니다. 그리하여 자바스크립트는 Global Scope를 시작점으로 하여 `a` 변수의 위치를 찾습니다. (더 이상 탐색할 상위 Scope는 존재하지 않습니다.)
* Global Scope에서 `a` 변수가 존재하는지 찾지만, 찾을 수 없습니다.
* 자바스크립트 입장에서 `a`라는 명칭은 알 수 없는 문자입니다. 결국 에러가 발생하게 됩니다.

Line 7의 실행문은 Global Scope에서 실행되었기 때문에 상위 Scope가 존재하지 않습니다.

**만약 현재 Scope에서 원하는 정보를 찾지 못하고 상위 Scope가 존재한다면, 상위 Scope를 탐색합니다. 상위 Scope에서 원하는 정보를 찾지 못하고 한 단계 더 상위 Scope가 존재한다면, 한 단계 더 상위 Scope를 탐색합니다. 이런 방식으로 Global Scope까지 탐색을 계속하며, 원하는 정보를 찾으면 탐색을 멈춥니다.**
{% endtab %}
{% endtabs %}

{% hint style="danger" %}
변수를 선언할때, 해당 변수가 사용되는 스코프를 잘 판단하여 불필요하게 상위 스코프에 선언하지 않도록 해야 합니다.
{% endhint %}
