# Scope Quiz

아래 예제 코드를 보고 어떤 결과가 나올지 스스로 추측하고 탐구 해보세요.

{% tabs %}
{% tab title="JavaScript" %}
{% code title="Quiz 1" %}
```javascript
function foo () {
  var a = 5;

  for (var i = 0; i < a; i++) {
    console.log(a);
  }

  console.log(i);  // 무엇이 출력될까요?
}

foo();
```
{% endcode %}

#### Q1. Line 8에서 출력되는 값은?

1. `0`
2. `5`
3. `4`
4. `undefined`
5. `Error`
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="JavaScript" %}
{% code title="Quiz 2" %}
```javascript
var a = 1;

function bar () {

  function foo() {
    console.log(a);  // ?
  }

  foo();
}

bar();
```
{% endcode %}

#### Q2. Line 6에서 출력되는 값은?

1. `1`
2. `undefined`
3. `Error`
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="JavaScript" %}
{% code title="Quiz 3" %}
```javascript
var a = 1;

function bar () {

  function foo() {
    console.log(a);  // ?
  }
  
  a = 2;

  foo();
}

bar();
```
{% endcode %}

#### Q3. Line 6에서 출력되는 값은?

1. `1`
2. `2`
3. `undefined`
4. `Error`
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="JavaScript" %}
{% code title="Quiz 4" %}
```javascript
function foo() {
  var a = 1;

  function bar () {
    a = 2;
  }

  console.log(a); // ?
  bar();
}

foo();
```
{% endcode %}

#### Q4. Line 8에서 출력되는 값은?

1. `1`
2. `2`
3. `undefined`
4. `Error`
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="JavaScript" %}
{% code title="Quiz 5" %}
```javascript
var x = 1; 
  
function foo () { 
    if (x > 1) { 
        var x = 2; 
    } 
  
    console.log(x); 
} 
  
foo(); 
```
{% endcode %}

#### Q5. Line 8에서 출력되는 값은?

1. `1`
2. `2`
3. `undefined`
4. `Error`
{% endtab %}
{% endtabs %}
