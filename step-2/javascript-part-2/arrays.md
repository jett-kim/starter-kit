# Arrays

배열이란 어떠한 정보(값)들을 **순서대로** 저장할 수 있는 구조입니다. 아래와 같이 대괄호를 이용해 배열을 만들 수 있습니다.

```javascript
var fruits = [ 'apple', 'orange', 'grape' ];
```

배열 안에 들어있는 값들을 **요소(element, item, etc)**라고 합니다.

위의 `fruits` 변수에 담긴 배열의 경우, 첫 번째 요소는 `'apple'`(문자열 apple)이고, 두 번째 요소는 `'orange'`(문자열 orange), 세 번째 요소는 `'grape'`(문자열 grape)입니다. 그래서 `fruits` 변수에 담긴 배열은 3개의 요소를 갖고 있다고 표현할 수 있습니다. &#x20;

현재 위의 배열에서는 모두 문자열 요소들이 담겨있지만, 여러분이 원하는 어떤 값이라도 배열의 요소로 추가할 수 있습니다. 종류가 다른 값들도 함께 담을 수 있습니다.

```javascript
var arr = [ 1, '3', true ];
var arr1 = [ undefined, null, false, NaN, 1000 ];
```

#### 배열의 길이

모든 배열은 요소의 갯수에 대한 정보를 아래와 같이 `.length` 속성을 이용하여 제공해줍니다.

```javascript
var fruits = [ 'apple', 'orange', 'grape' ];
console.log(fruits); // [ 'apple', 'orange', 'grape' ]
console.log(fruits.length); // 3
```

이전 레슨에서 함수를 배웠으니, 배열의 길이를 반환해주는 함수를 한번 만들어볼까요?

```javascript
var fruits = [ 'apple', 'orange', 'grape' ];
function getNumOfFruits () {
  return fruits.length;
}
var numOfFruits = getNumOfFruits();
console.log(numOfFruits); // 3
```

위 함수는 `fruits`라는 변수에 담긴 배열의 길이만 돌려주고 있습니다. 조금 사용 용도가 제한적인 상황입니다. 모든 배열에 대해서 길이 값을 반환해줄 수 있는 함수를 만들어보는 것은 어떨까요? 함수는 인자를 받을 수 있기 때문에, 그런 성질을 이용하면 좋을것 같습니다.

```javascript
function getNumOfItems (array) {
  return array.length;
}

var fruits = [ 'apple', 'orange', 'grape' ];
var numOfFruits = getNumOfItems(fruits);
console.log(numOfFruits); // 3
```

위 예제 코드의 `getNumOfItems`는 매개 변수로 `array`라는 것을 선언해놓았습니다. 그리고 해당 함수를 실행하며 인자로 `fruits` 배열을 넣어주고 있습니다. 그렇기 때문에 함수 내부에서 `array`라는 매개 변수는 `fruits`가 대입되고, `fruits`의 길이를 반환하게 됩니다.

조금 더 재사용이 유연해진 함수가 작성되었습니다.

#### 배열의 요소 접근

배열의 경우, 문자열과 마찬가지로 각 요소들을 인덱스를 이용하여 접근할 수 있습니다.

```javascript
var food = [ 'pasta', 'steak', 'rice' ];
var myFavoriteFood = food[1];
console.log(myFavoriteFood); // 'steak'
```

인덱스를 이용하여 배열의 해당 인덱스 위치에 자리한 요소를 수정할 수도 있습니다.

```javascript
var fibonacci = [ 1, 2, 3, 5, 8, 13 ];

console.log(fibonacci[4]); // 8

fibonacci[4] = false;

console.log(fibonacci[4]); // false
```

#### 배열에 요소 추가하기

우선 인덱스를 이용하여 원하는 위치에 요소를 추가할 수 있습니다.

```javascript
var arr = [];
arr[0] = true;
console.log(arr[0]); // true

arr[2] = true;
console.log(arr[2]); // true

console.log(arr); // [ true, undefined, true ]
```

또는 아래와 같이 메서드를 이용할 수도 있습니다.

```javascript
var arr = [];

// push 메서드는 배열의 뒤에 요소를 추가합니다.
arr.push(1); // arr은 [1]이 됩니다.
arr.push(2); // arr은 [1, 2]가 됩니다.

// pop 메서드는 배열의 뒤에서 하나의 요소를 제거합니다.
arr.pop(); // arr은 다시 [1]이 됩니다.
arr.pop(); // arr은 다시 빈 배열이 됩니다.
```

#### 다양한 배열 메서드

[Array Methods](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global\_Objects/Array#%EB%A9%94%EC%84%9C%EB%93%9C)

위 링크에서 여러 가지 메서드들을 한번 학습해보시기 바랍니다.

### 추가 학습 자료

* [Arrays - W3Schools](https://www.w3schools.com/js/js\_arrays.asp)
* [Arrays - Javascript Info](https://javascript.info/array)
* [Arrays - MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global\_Objects/Array)
* [Arrays and Objects - Eloquent Javascript](https://eloquentjavascript.net/04\_data.html)
