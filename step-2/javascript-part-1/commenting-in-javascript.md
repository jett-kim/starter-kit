# Commenting in JavaScript

우리는 아래와 같이 자바스크립트 코드와 함께 추가적인 코멘트(주석)를 작성할 수 있습니다. 코멘트는 코드의 로직이나 결과에 영향을 미치지 않으며, 오로지 프로그래머들을 위한 설명 등의 목적으로 작성합니다.

#### 한 줄로 코멘트 추가하기

한 줄로 코멘트를 작성할 때는 `//`를 이용할 수 있습니다.

```javascript
// Fruit: orange
const orange = { taste: "sweet" };

// Fruit: apple
const apple = { taste: "no good" };

const melon = { taste: "no good" }; // Fruit: melon
```

#### 한 줄 이상의 코멘트 작성하기

`/*`와 `*/`를 이용하여 코멘트를 여러 줄 작성할 수도 있습니다.

```javascript
/*

이렇게
여러 줄의
코멘트를
작성할 수도
있습니다.

 */

const apple = { taste: "no good" };
const orange = { taste: "sweet" };
```
