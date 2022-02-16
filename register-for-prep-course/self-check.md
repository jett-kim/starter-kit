# 프렙 코스 신청 전 자가점검

{% hint style="danger" %}
**최소 Step 5이상의 사전준비를 진행하지 않은 분들에게는 스포일러가 될 수 있습니다. 다른 페이지로 이동하세요.**
{% endhint %}

{% hint style="info" %}
아래 내용은 절대적인 기준이 될 수 없으니, 참고용으로만 사용하세요.
{% endhint %}



![](../.gitbook/assets/image.png)

{% hint style="danger" %}
**Step 5 이상 진행하신게 확실할까요? 달력까지 만들어 보신거죠?**
{% endhint %}



별도의 준비시간이나 추가자료 없이 아래에 주어진 문제를 각각 제한시간 약 30분 내에 해결할 수 있고, 스코프/호이스팅/원시값/참조값 등의 자바스크립트 개념들을 문제풀이와 연결지어 어느정도 설명할 수 있는 수준이라면 프렙 코스 수강에 적합한 수준이라 판단할 수 있습니다.



```javascript
// 예시 문제 1

function add (num) {
  //  your solution
}

// 아래에 주어진 케이스에 대응할 수 있도록 `add` 함수를 작성해주세요.
// 주어진 두 가지 케이스 외에는 대응하지 않아도 됩니다.
const six = add(1)(2)(3);
const ten = add(2)(3)(5);

console.log(six); // 6
console.log(ten); // 10
```

```javascript
// 예시 문제 2
// Object 관련 메소드 사용 금지

function inverse (collection) {
  //  your solution
}

// 아래에 주어진 케이스에 대응할 수 있도록 `inverse` 함수를 작성해주세요.
// 주어진 두 가지 케이스 외에는 대응하지 않아도 됩니다.
const data1 = { a: 1, b: 2, c: 5 };
const data2 = { name: "ken", age: 30, city: "seoul" };

const result1 = inverse(data1);
const result2 = inverse(data2);

console.log(result1); // { '1': 'a', '2': 'b', '5': 'c' }
console.log(result2); // { 'ken': 'name', '30': 'age', 'seoul': 'city' }
```
