# Primitive and Reference Quiz

{% tabs %}
{% tab title="JavaScript" %}
```javascript
const person = {
  age: 30
};

const something = person.age;

person.age = 50;

console.log(something); // ?
```

위 예제의 콘솔 출력 결과는?
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="JavaScript" %}
```javascript
let one = { name: "one" };
const two = { name: "two" };

const something = one;

one = { name: "ONE" };

console.log(something); // ?
```

위 예제의 콘솔 출력 결과는?
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="JavaScript" %}
```javascript
let one = 1;
const two = 2;

const something = one;

one = 101;

console.log(something); // ?
```

위 예제의 콘솔 출력 결과는?
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="JavaScript" %}
```javascript
let ken = {
  name: "ken",
  age: 30
};

const wan = {
  name: "wan",
  age: 35
};

const people = [ ken, wan ];

ken = {
  name: "KEN",
  age: 38
};

console.log(people);  // ?
console.log(ken === people[0]);  // ?
```

위 예제의 콘솔 출력 결과는?
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="JavaScript" %}
```javascript
var secret = {
  data: "I am secret"
};

function destroy (stuff) {
  stuff = null;
}

destroy(secret);

console.log(secret); // ?
```

위 예제의 콘솔 출력 결과는?
{% endtab %}
{% endtabs %}

