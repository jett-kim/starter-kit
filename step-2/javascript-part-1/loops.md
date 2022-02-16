# Loops

아래와 같은 문자열이 우리에게 주어졌다고 생각해보세요.

```javascript
var name = "ken";
```

우리는 이 문자열의 모든 글씨들을 하나씩 콘솔에 출력하고 싶습니다. 우선 아래와 같이 할 수 있겠죠?

```javascript
console.log(name[0]);
console.log(name[1]);
console.log(name[2]);
```

지금은 글씨가 세 개 밖에 없기 때문에, 크게 무리가 없었지만.. 만약 글씨가 100개 혹은 1000개.. 혹은 몇 개인지 정확히 모를 경우, 대처하기가 어려워지겠죠?

그런데 위 예제의 코드를 보면 반복되는 부분들이 보이시나요? 우리는 이렇게 어떤 특정 패턴의 코드를 반복할때 반복문(Looping Statement)를 사용하여 조금 더 유연한 코드를 작성할 수 있습니다.

우선 위 예제 코드의 내용을 반복문을 통해 조금 변경해보겠습니다.

```javascript
var name = "ken";

for (var i = 0; i < name.length; i++) {
  console.log(name[i]);
}
```

위의 반복문을 실행하게 되면, `name` 문자열의 첫 번째부터 세 번째까지 차례대로 출력하게 됩니다.

### 반복문의 구조

반복문을 한번 자세히 살펴보도록 하겠습니다.

for loop에는 세미콜론과 중괄호를 기준으로 크게 4가지 파트가 있습니다.

```javascript
for (1번 파트; 2번 파트; 4번 파트) {
  3번 파트
}
```

#### 1번 파트 (Initialization)

for loop의 초기 구동 코드입니다. for loop의 실행이 시작되는 시점에 가장 먼저 실행되는 부분이며, 단 한번만 실행됩니다. 일반적으로 for loop에서 사용되는 변수 선언을 하는 용도로 가장 많이 사용합니다.

#### 2번 파트 (Conditional)

for loop의 3번 파트(반복 구절)의 실행 여부를 결정하는 조건이 들어가는 부분입니다. 2번 파트의 조건이 성립하지 않는다면, for loop의 실행이 종료됩니다. 2번 파트의 조건이 성립 여부는 2번 파트의 결과값이 Truthy인지 Falsy인지를 의미합니다.

#### 3번 파트

반복하여 실행하는 로직을 써넣는 곳입니다.

#### 4번 파트 (Update)

3번 파트(반복 구절)의 실행이 끝난 후에 실행되는 구절입니다. 3번 파트가 여러번 실행된다면, 4번 파트 또한 여러번 실행됩니다. 3번 파트가 종료될때마다 매번 실행되기 때문입니다.

### 실행 순서

1\~4번 파트에 대한 상세 내용을 예제와 함께 살펴보겠습니다.

```javascript
for (let i = 1; i < 3; i++) {
  console.log(i);
}
```

1. 1번 파트(Initialization) 실행
   * 변수 `i`를 선언하고 1이라는 숫자값을 할당합니다.
2. 2번 파트(Conditional) 실행
   * `i < 3`를 실행하고, 현재 `i`는 1이므로 결과는 `true`입니다.
   * Truthy 값이 나왔으므로 4번 파트가 실행될 수 있습니다.
3. 3번 파트가 실행됩니다.
   * `i`의 값을 콘솔에 출력합니다.
   * 현재 `i`는 1이므로 1을 출력합니다.
4. 3번 파트가 끝났으므로 4번 파트가 실행됩니다.
   * `i++`를 실행하고, `i`의 값이 2로 증가합니다.
5. 2번 파트(Conditional) 실행
   * `i < 3`을 실행하고, 현재 `i`는 2이므로 결과는 `true`입니다.
   * Truthy 값이 나왔으므로 3번 파트가 실행될 수 있습니다.
6. 3번 파트가 실행됩니다.
   * `i`의 값을 콘솔에 출력합니다.
   * 현재 `i`는 2이므로 2을 출력합니다.
7. 3번 파트가 끝났으므로 4번 파트가 실행됩니다.
   * `i++`를 실행하고, `i`의 값이 3으로 증가합니다.
8. 2번 파트(Conditional) 실행
   * `i < 3`을 실행하고, 현재 `i`는 3이므로 결과는 `false`입니다.
   * Falsy 값이 나왔으므로 3번 파트가 실행될 수 없습니다.
9. for loop이 모두 종료됩니다.

#### 반복문 중단하기

`for loop` 내부에서 우리는 `break`라는 키워드를 사용할 수 있습니다. `break` 키워드는 4번 반복 구문 내부에서 사용할 수 있고, `break` 구문이 실행되게 되면, `for loop`이 종료되게 됩니다. 아래의 예제를 한번 살펴봅시다.

```javascript
console.log('before for loop');

for (var i = 1; i < 11; i += 2) {
  console.log(i);
}

console.log('after for loop');
```

위 예제를 실행하게 되면, 1부터 10까지 홀수가 콘솔에 나타나게 됩니다. 그렇다면 아래와 같이 변경하면 어떻게 될까요?

```javascript
console.log('before for loop');

for (var i = 1; i < 11; i += 2) {
  if (i === 7) {
    break;
  }

  console.log(i);
}

console.log('after for loop');
```

반복 구문 내부에 새로운 조건이 추가되었습니다. `i`의 값이 7과 같을 경우, `break`를 실행하게 됩니다. 그리고 더 이상 반복문은 실행되지 않고, `after for loop`이 콘솔에 나타났습니다. 즉, `break` 실행문이 실행되어 `for loop`이 **모두** 종료되게 된 것입니다.

#### 반복 구문 종료하기

위에서 말씀드린 `break` 구문은 반복문 전체를 종료시켰습니다. 이번에는 `continue`를 이용하여 반복 구문 단위로 종료시키는 방법을 살펴보겠습니다.

```javascript
console.log('before for loop');

for (var i = 1; i < 11; i += 2) {
  if (i === 7) {
    continue;
  }

  console.log(i);
}

console.log('after for loop');
```

위 예제 코드의 경우, 콘솔에 1, 3, 5, 9가 나타납니다. 7일 경우에는 `continue` 구문이 실행되었기 때문에 반복 구문을 종료하게 되었습니다. 하지만 전체 반복문을 종료시킨 것은 아닙니다. 그렇기에 다시 업데이트 구문 -> 조건 구문 -> 반복 구문이 실행되어 9가 콘솔에 나타나게 되었습니다.

#### Summary

위에서 살펴본 `for loop`은 가장 기본적인 형태의 반복문입니다. 이 외에도 다양한 반복문의 종류가 있습니다. 차차 알게되실테니, 우선은 기본적인 반복문을 잘 익혀보세요.

### 퀴즈

{% tabs %}
{% tab title="JavaScript" %}
```javascript
var name = "ken";

// 역순으로 한 글자씩 출력하는 반복문을 작성해보세요.
```

반복문을 이용하여 위에 주어진 문자열을 역순으로 출력하는 코드를 작성해보세요.
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="JavaScript" %}
```javascript
var longText = "0i1a2m3k4e5n";

// 홀수번째 글자만 출력하는 코드를 작성해보세요.
```

반복문을 이용하여 위에 주어진 문자열의 홀수번째 글자만 출력하는 코드를 작성해보세요.
{% endtab %}
{% endtabs %}

### 추가 학습 자료

* [Complete Guide - FreeCodeCamp](https://www.freecodecamp.org/news/the-complete-guide-to-loops-in-javascript-f5e242921d8c/)
* [Loops - Learn-js](https://www.learn-js.org/en/Loops)
* [Loops and Iteration - MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Loops\_and\_iteration)
