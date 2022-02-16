# Creating Elements

수정과 삭제가 가능하듯, 우리가 원하는대로 생성할 수도 있습니다. 예제 코드와 함께 보여드리겠습니다.

```javascript
// h1 요소 만들어서 `heading`이라는 변수에 할당
const heading = document.createElement("h1");

// 방금 생성한 `heading` 요소의 텍스트 설정
heading.textContent = "제목입니당";
// 방금 생성한 `heading` 요소의 스타일 설정
heading.style.fontSize = "50px";

// 방금 생성한 `heading` 요소를 body 태그의 자식으로 추가
document.body.appendChild(heading);
```

위 예제처럼 우리가 원하는 요소를 만들고, 글씨를 수정하고 스타일도 수정할 수 있습니다. 그리고 우리가 원하는 자리에 추가할 수도 있습니다.

> 우리가 자바스크립트로 생성한 요소는 우리가 직접 화면 어딘가에 명시적으로 추가하기 전까지는 시각적으로 화면에 나타나지 않습니다. 예를 들면, 위 예제 코드에서 `document.body.appendChild(heading);`라는 코드가 없었다면, heading은 화면에 나타나지 않습니다.

#### 🚨 퀴즈

아래 두 가지 예제 코드의 차이점을 분별해보세요.

{% code title="Example 1" %}
```javascript
const something = document.createElement("p");

for (let i = 0; i < 5; i++) {
  something.textContent = i;
  document.body.appendChild(something);
}
```
{% endcode %}

{% code title="Example 2" %}
```javascript
for (let i = 0; i < 5; i++) {
  const something = document.createElement("p");
  something.textContent = i;
  document.body.appendChild(something);
}
```
{% endcode %}
