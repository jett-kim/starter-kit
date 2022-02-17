---
description: '기간: 최대 3일'
---

# 🖋  Background Changer

### Quiz #1

```javascript
/*

  다음과 같은 조건을 만족하는 화면을 만들어 주세요!
  
  📌 버튼 클릭시 랜덤한 HEX CODE가 배경 색으로 변경되어야 합니다.
  📌 현재 HEX CODE가 <p> 태그의 텍스트로 표시되어야 합니다.

*/
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/XWzNyYx)



{% hint style="info" %}
**Hex Code란?**

0\~9까지의 숫자와 A\~F까지의 알파벳이 랜덤하게 구성되어 이루는 6자리 코드를 의미합니다. \
예를 들면 000000, 3474FF 등 모두 유효한 Hex Code입니다. \
CSS에서는 Hex Code앞에 **#**_를 붙여 색상값으로 이용할 수 있습니다._ \
_예) #3474FF_
{% endhint %}

{% hint style="danger" %}
랜덤한 Hex code를 생성하는 함수를 작성하도록 **스스로 시도해본 후**, 너무 어려울 경우 아래 함수를 사용하세요.
{% endhint %}

{% tabs %}
{% tab title="Hex code generator" %}
```javascript
function hexGenerator() {
  const hexNumbers = [
    0,
    1,
    2,
    3,
    4,
    5,
    6,
    7,
    8,
    9,
    'A',
    'B',
    'C',
    'D',
    'E',
    'F'
  ];

  let result = "#";
  
  for (var i = 0; i < 6; i += 1) {
    const randomIndex = Math.floor(Math.random() * hexNumbers.length);
    result += hexNumbers[randomIndex];
  }
  
  return result;
}
```
{% endtab %}
{% endtabs %}

