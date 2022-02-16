# Selecting Elements

{% embed url="https://vimeo.com/352474390" %}
CSS 선택자
{% endembed %}

{% embed url="https://vimeo.com/352477326" %}
getElementby\~\~
{% endembed %}

{% embed url="https://vimeo.com/352496353" %}
부모, 자식 요소 선택하기
{% endembed %}

### 요소 선택하기

우선 HTML 문서를 기반으로 만들어진 화면 속 요소를 선택하는 방법부터 살펴볼까요?

화면 속 요소를 선택하는 방법에는 크게 아래와 같이 4가지가 있습니다.

1. 아이디 이름을 이용하여 선택하는 방법
2. 클래스 이름을 이용하여 선택하는 방법
3. 태그 이름을 이용하여 선택하는 방법
4. CSS 선택자를 이용하여 선택하는 방법

```markup
<div class="container">
  <h1>I am a Heading</h1>
  <p>I am a Paragraph</p>
  <ul>
    <li class="item">
      <p>I am a Paragraph</p>
    </li>
    <li class="item">
      <p>I am a Paragraph</p>
    </li>
    <li class="item">
      <p>I am a Paragraph</p>
    </li>
  </ul>
  <button id="special-button">I am a Button</button>
</div>
```

#### 1. 아이디 이름을 이용하여 선택하는 방법

위와 같은 HTML 문서가 있다고 가정했을때, `special-button`이라는 아이디를 가진 요소를 다음과 같이 선택하여 사용할 수 있습니다.

```javascript
// special-button 아이디를 가진 요소를 선택하여 `$el` 변수에 대입
const $el = document.getElementById("special-button");

// special-button 아이디를 가진 요소의 텍스트 변경
$el.textContent = "I am a Special Button";
```

아이디란 기본적으로 하나의 HTML 문서에서 고유한 값이어야 하기 때문에, 위와 같이 `document.getElementById`를 이용하여 요소를 선택할 경우 우리에게 주어지는 값은 단 하나의 요소입니다.

위에서 우리가 선택한 그 하나의 요소는 Node 혹은 HTML Element라고 부르는 존재입니다. Node가 조금 더 포괄적인 상위 개념이고, HTML Element는 한 단계 하위 개념입니다. 그 차이를 지금 정확히 알아야 할 필요는 없지만, 시간이 되신다면 조사해보세요. (Google 추천 검색어: "Node vs Element")

위 예제 코드에서 선택한 요소는 Node이기도 하고 동시에 HTML Element이기 때문에, 아래 링크 페이지에서 왼쪽 "관련 주제"에 나열된 속성과 메소드를 모두 사용할 수 있습니다.

* [Node](https://developer.mozilla.org/ko/docs/Web/API/Node)
* [Element](https://developer.mozilla.org/ko/docs/Web/API/Element)

#### 2. 클래스 이름을 이용하여 선택하는 방법

위와 같은 HTML 문서가 있다고 가정했을때, 특정 클래스 이름을 가진 요소들은 다음과 같이 선택하여 사용할 수 있습니다.

```javascript
// item 클래스를 가진 "모든 요소들"을 선택하여 `$listItems` 변수에 대입
const $listItems = document.getElementsByClassName("item");

// container 클래스를 가진 "모든 요소들"을 선택하여 `$container` 변수에 대입
const $container = document.getElementsByClassName("container");

// getElementsByClassName의 결과값은 배열과 유사한 형태이므로 인덱스로 접근하여 사용한다.
$listItems[0].textContent = "List 1";
$listItems[1].textContent = "List 2";
$listItems[2].textContent = "List 3";

// HTML 상에서 해당 클래스를 가진 요소가 단 하나 뿐이더라도,
// getElementsByClassName의 결과값은 배열과 유사한 형태이므로 인덱스로 접근하여 사용한다.
$container[0].style.backgroundColor = "green";
```

위 예제에서 `getElementsByClassName` 함수를 이용하여 변수에 할당한 존재는 모두 배열과 유사한 형태(유사 배열)입니다. 그리고 이 유사 배열에 담긴 배열의 요소들이 하나의 HTML Element입니다. 그렇기 때문에 거의 대부분의 상황에서 우리는 배열의 인덱스 위치를 이용하여 사용해야 합니다.

#### 3. 태그 이름을 이용하여 선택하는 방법

위와 같은 HTML 문서가 있다고 가정했을때, 특정 태그를 사용한 요소들은 다음과 같이 선택하여 사용할 수 있습니다.

```javascript
// li 태그를 이용한 "모든 요소들"을 선택하여 `$listItems` 변수에 대입
const $listItems = document.getElementsByTagName("li");

// p 태그를 이용한 "모든 요소들"을 선택하여 `$paragraphs` 변수에 대입
const $paragraphs = document.getElementsByTagName("p");

// getElementsByTagName의 결과값은 배열과 유사한 형태이므로 인덱스로 접근하여 사용한다.
$listItems[0].textContent = "List 1";
$listItems[1].textContent = "List 2";
$listItems[2].textContent = "List 3";

// 위치와 상관없이 모든 p 태그를 선택하게 되므로 $paragraphs에는 총 4개의 요소가 선택되고,
// 그 중 첫번째 요소의 배경 색깔을 수정합니다.
$paragraphs[0].style.backgroundColor = "green";
```

위 예제에서 `getElementsByTagName` 함수를 사용하여 선택한 결과값은 `getElementsByClassName`을 사용한 결과값과 동일한 형태(HTML Element가 담긴 유사 배열)입니다.

#### 4. CSS 선택자를 이용하여 선택하는 방법

위와 같은 HTML 문서가 있다고 가정했을때, [CSS 선택자](https://code.tutsplus.com/ko/tutorials/the-30-css-selectors-you-must-memorize--net-16048)를 활용하여 아래와 같이 선택하여 사용할 수 있습니다. 최근에 가장 많이 사용되는 방법입니다.

```javascript
// CSS 선택자 문법을 이용하여 container라는 클래스 이름을 가진 요소를 선택합니다.
// querySelector라는 함수는 모든 경우에 "하나의 요소"를 반환합니다.
const $container = document.querySelector(".container");

const $button = document.querySelector("#special-button");

// 주어진 CSS 선택자와 일치하는 요소가 여러 개일 경우,
// querySelector 함수는 가장 첫번째 요소를 반환합니다.
const $listItem = document.querySelector(".item");

// querySelectorAll 함수는 주어진 CSS 선택자와 일치하는 "모든 요소들"을 유사 배열의 형태로 반환합니다.
// (요소를 제어하고 싶다면 인덱스 위치를 사용해야 합니다.)
const $paragraphs = document.querySelectorAll("p");
```
