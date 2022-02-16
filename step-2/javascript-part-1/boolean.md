# Boolean

### Boolean 소개

자바스크립트에는 Boolean(불리언)이라는 종류의 값들이 있습니다. 가장 이해하기 쉽고 간단한 종류입니다. Boolean에는 `true` 혹은 `false` 단 두 가지의 값만 존재합니다. 사실이냐 거짓이냐 단 두 가지 의미만 가질 수 있는 종류의 값입니다.

```javascript
const s = true;
const h = false;

console.log(s === h); // false
```

> 혹시라도 위 코드 예제가 완전히 이해되지 않았더라도 너무 걱정하지 마세요. 앞으로 나올 레슨에서 차근차근 설명드릴 하겠습니다.

### 주의할 점

```javascript
const o = new Boolean(true);  // 이렇게 만들어 사용하지 마세요.
const t = true; // 항상 이렇게 만들어 사용하세요.
```

위 두 가지의 차이점은 코스 후반부에서 설명드리도록 하겠습니다.

### 추가 학습 자료

* [Javascript Booleans - W3Schools](https://www.w3schools.com/js/js\_booleans.asp)
* [Boolean - MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global\_Objects/Boolean)
* [Boolean - PoiemaWeb](https://poiemaweb.com/js-data-type-variable#113-boolean)
