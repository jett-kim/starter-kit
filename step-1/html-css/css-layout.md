# 📗  CSS Layout

### 1. Block vs Inline Block

HTML 요소들은 크게 두 가지로 분류할 수 있습니다. 첫번째는 Block 요소, 그리고 두번째는 Inline 요소입니다. 이 두 가지의 차이점은 굉장히 중요합니다. 그렇다면 그 차이점은 무엇일까요?

#### 1-1. Block Elements

Block 요소들은 화면상에서 항상 새로운 줄에서 시작하고, 위 아래에 서로 쌓이는 형식으로 나타납니다. 그리고 사용 가능한 최대치의 폭을 차지하게 됩니다.

아래의 예제를 한번 보시기 바랍니다. HTML 상으로는 한 줄에 2개의 `p` 태그를 작성하였습니다. 하지만 화면에서 보시면, 두 개의 `p` 태그가 모두 전체 화면의 폭만큼 넓게 자리잡은 상태로 각각의 새로운 줄에 나타나는 것을 볼 수 있습니다. `p` 태그는 브라우저 상에서 기본으로 Block 요소이기 때문입니다.

[예제 링크](https://codepen.io/ken123777/pen/VOGqxV?editors=1100#0)

```markup
<html>
<head>
  <title>HTML & CSS</title>
</head>
<body>
  <p class="one">one</p><p class="two">two</p>
</body>
</html>
```

```css
.one {
  background-color: red;
}

.two {
  background-color: blue;
}
```

Block 요소들은 또 다른 Block 요소를 자식으로 가질 수도 있고, Inline 요소를 자식으로 가질 수도 있습니다. 그에 대한 제약은 없습니다. 조금 다른 예제를 한번 볼까요?

[예제 링크](https://codepen.io/ken123777/pen/qGMgjG?editors=1100#0)

`div` 또한 Block 요소입니다. 폭이 화면의 폭만큼 넓지 않은 이유는 `width: 50%;`라는 설정을 했기 때문입니다. 그리고 `div` 요소 내부에는 `p` 태그가 두 개 들어있습니다. 해당 `p` 태그는 Block 요소이기 때문에 자신들이 차지할 수 있는 가장 최대치의 폭을 차지하게 됩니다. 양 옆에 약간의 노란색 공간이 보이는 것은 `div` 요소에게 주어진 `padding: 10px;` 때문입니다.

```markup
<html>
<head>
  <title>HTML & CSS</title>
</head>
<body>
  <div class="container">
    <p class="one">one</p>
    <p class="two">two</p>
  </div>
</body>
</html>
```

```css
.container {
  background-color: yellow;
  width: 50%;
  padding: 10px;
}

.one {
  background-color: red;
}

.two {
  background-color: blue;
}
```

#### 1-2. Inline Elements

Inline 요소들은 새 줄에서 나타나지 않습니다. 일반적인 문서에서의 텍스트 흐름과 동일하게 동작합니다. 하나에 이어 또 다른 하나가 줄줄이 이어 붙어서 나타나는 형식입니다. 그리고 요소 내부 컨텐츠의 양만큼만 폭을 차지하게 됩니다. Inline 요소들은 또 다른 Inline 요소들을 자식으로 포함할 수 있지만, Block 요소를 자식으로 품을 수는 없습니다. 예제를 통해 확인해볼까요?

[예제 링크](https://codepen.io/ken123777/pen/jovdXx?editors=1100#0)

`span` 태그는 대표적인 Inline 요소 중 하나입니다. 화면 상으로 초록색 배경이 적용된 부분들이 보이시나요? 각각의 Inline 요소들입니다. 새로운 줄로 넘어가지 않고 텍스트의 흐름 상에 자연스럽게 적용됩니다.

```markup
<html>
<head>
  <title>HTML & CSS</title>
</head>
<body>
  <div class="container">
    <p><span class="italic-text">Hello</span> <span class="bold-text">Vanilla</span> Coding</p>
  </div>
</body>
</html>
```

```css
.container {
  background-color: yellow;
}

.italic-text {
  font-style: italic;
  background-color: green;
}

.bold-text {
  font-weight: bold;
  background-color: green;
}
```

### 2. Positioning

우리는 CSS를 이용하여 웹페이지 컨텐츠의 위치(Position)를 우리가 원하는 대로 조정할 수 있습니다. 컨텐츠의 위치를 조정하기 위해서는 다양한 방법들이 있는데, 어떤 방법들이 있는지 한번 살펴보도록 하겠습니다.

#### 2-1. Using Flex

가장 첫 번째 방법은 CSS의 `flex` 속성을 이용하는 것입니다. `flex` 속성은 기존 요소들의 흐름에서 벗어나, 다양한 방식으로 자식 요소들을 배치할 수 있는 유연함을 제공합니다.

아래 예제를 보시면, 간단한 웹페이지를 만들어 놓았습니다. 모든 요소들은 일반적인 Block 요소의 흐름대로 수직으로 나열되어 있습니다.

Flex를 사용하지 않은 [예제 링크](https://codepen.io/ken123777/pen/gJBRYm?editors=1100#0)

```markup
<header>
  <code>&#60;HEADER&#62;</code>
</header>

<div class="main">
  <section>
    <code>&#60;SECTION&#62;</code>
  </section>

  <aside>
    <code>&#60;ASIDE&#62;</code>
  </aside>
</div>

<footer>
  <code>&#60;FOOTER&#62;</code>
</footer>
```

```css
code {
  background: #000000;
  color: #FFFFFF;
  display: block;
  padding: 25px;
  text-align: center;
}

header,
section,
aside,
footer {
  margin: 10px;
}

footer {
  margin-bottom: 0;
}
```

위의 웹페이지 예제에서 보셨던 `<section>`과 `<aside>` 요소는 Block 요소이기 때문에, 기본적으로 위/아래 형식으로 배치됩니다. 이제 두 요소를 양 옆으로 나란히 배치해보도록 하겠습니다. `<section>`요소와 `<aside>` 요소의 부모인 `".main"` 요소에 `flex` 를 적용해보겠습니다.

[예제 링크](https://codepen.io/ken123777/pen/dEgRYM?editors=1100#0)

```markup
<header>
  <code>&#60;header&#62;</code>
</header>

<div class="main">
  <section>
    <code>&#60;SECTION&#62;</code>
  </section>

  <aside>
    <code>&#60;ASIDE&#62;</code>
  </aside>
</div>

<footer>
  <code>&#60;footer&#62;</code>
</footer>
```

```css
.main {
  display: flex;
}

code {
  background: #000000;
  color: #FFFFFF;
  display: block;
  padding: 25px;
  text-align: center;
}

header,
section,
aside,
footer {
  margin: 10px;
}

footer {
  margin-bottom: 0;
}
```

{% hint style="info" %}
Flex 속성은 매우 다양한 기능들을 제공합니다. 하나씩 배우면 되니, 아직 너무 고민하지 마세요.
{% endhint %}

#### 2-2. Using Inline Block

두 번째 방법은 `display` 속성에 해당하는 값 중 하나인 `inline-block`을 이용하는 방법입니다. `inline-block`을 이용하면, 여러 개의 Block 요소들을 마치 Inline 요소처럼 한 줄에 이어서 배치할 수 있습니다. 아래 예제를 보시면 이전 예제와 약간의 스타일 차이는 있지만, Block 요소를 한 줄에 나란히 배치한 것을 볼 수 있습니다. 이전과는 다르게 `<section>` 요소와 `<aside>` 요소에 `display: inline-block;`을 주었습니다.

[예제 링크](https://codepen.io/ken123777/pen/vwVZvW?editors=1100#0)

```markup
<header>
  <code>&#60;header&#62;</code>
</header>

<section>
  <code>&#60;section&#62;</code>
</section>

<aside>
  <code>&#60;aside&#62;</code>
</aside>

<footer>
  <code>&#60;footer&#62;</code>
</footer>
```

```css
code {
  background: #000000;
  color: #FFFFFF;
  display: block;
  padding: 25px;
  text-align: center;
}

header,
section,
aside,
footer {
  margin: 10px;
}

footer {
  clear: both;
  margin-bottom: 0;
}

section, aside {
  display: inline-block;
}
```

#### 2-3. Using Position Property

Flex와 Inline Block을 이용하여 다양한 배치를 시도할 수 있지만, 조금 더 정밀하게 배치할 수 있는 방법이 필요한 상황도 있습니다. 그런 상황에서 자주 사용되는 속성이 바로 `position` 입니다. 모든 요소들은 웹페이지에서 기본으로 `position: static;`을 갖습니다. 하지만 우리가 원한다면 다른 값으로 변경할 수 있고, 가장 흔하게 많이 사용되는 것이 바로 `position: relative;` 그리고 `position: absolute;`입니다.

**a. Relative Position**

`position: relative;`가 적용된 요소들의 경우, 별도의 추가적인 CSS 속성을 적용하지 않는 이상 별다른 특이점이 없습니다. 하지만, `top`, `right`, `bottom`, `left` 등의 값을 지정하게 되면 위치가 조정됩니다.

[예제 링크](https://codepen.io/ken123777/pen/gJBxaB?editors=1100#0)

**b. Absolute Position**

`position: absolute;`가 적용된 요소들의 경우는 조금 다릅니다. `position: absolute;`가 적용되게 되면 기존의 위치는 유지되지 않고, 가장 가까운 부모 요소 중 `position: relative;`가 적용된 요소를 찾아 그 요소를 기준으로 위치가 잡히게 됩니다. 만약 부모 요소 중 `position: relative;`를 가진 요소가 없는 경우, 전체 페이지를 기준으로 위치가 잡히게 됩니다.

[예제 링크](https://codepen.io/ken123777/pen/dEgzvm?editors=1100#0)

#### 도움이 될 만한 자료들

* [CSS Layout 학습](http://ko.learnlayout.com/toc.html)
* [게임으로 배우는 CSS Flexbox](https://flexboxfroggy.com/#ko)
