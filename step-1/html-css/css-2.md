# CSS 선택자

이번에는 CSS Selector(선택자)에 대해서 살펴보도록 하겠습니다.

### Selectors (선택자)

우리는 CSS에서 다양한 방법으로 HTML 요소를 선택하여 스타일을 적용시킬 수 있습니다.

#### 1. Type

```css
h1 {
  color: blue;
}
```

HTML의 태그 종류(type)을 지정하여 요소들을 꾸밀 수 있습니다. 지정한 태그 종류에 해당하는 _모든_ 요소들은 설정한 스타일이 적용됩니다.

```markup
<h1>Lorem ipsum</h1>
```

#### 2. Class

```css
.thick {
  font-weight: bold;
}
```

HTML 요소들의 클래스를 이용하여 요소들을 선택할 수도 있습니다. 클래스를 선택할 때는 클래스명 앞에 `.`을 적어주어야 합니다.

```markup
<span class="thick">I'm thick</span>
```

여러분은 동일한 클래스명을 많은 HTML 요소에게 줄 수 있습니다. 동일한 스타일을 여러 개의 요소에게 공통적으로 적용할 때 유용하게 사용되는 방법입니다.

그리고 또한 여러분은 하나의 HTML 요소에게 하나 이상의 클래스명을 줄 수 있습니다.

```css
.thick {
    font-weight: bold;
}

.alert {
    color: red;
}
```

아래의 `p` 태그는 `color: red;`와 `font-weight: bold;`가 모두 적용됩니다.

```markup
<p class="thick alert">Warning...</p>
```

#### 3. ID

```css
#box {
  background: blue;
}
```

HTML 요소의 ID 값을 이용하여 선택할 수 있습니다. ID를 이용하여 선택할 때는 ID 명 앞에 `#` 기호를 붙여주어야 합니다.

```markup
<div id="box">I'm a box</div>
```

하나의 웹 페이지에서 하나의 ID 명은 반드시 하나의 요소에만 적용되어야 합니다. 여러 개의 HTML 요소들이 동일한 ID 값을 가질 수 없습니다.

#### 4. Compound

```css
h1, h2, #box {
  font-family: Arial, Helvetica, sans-serif;
}
```

여러 개의 Selector를 동시에 나열하는 방식입니다. 쉼표로 구분하여 나열된 Selector 중 하나라도 일치한다면 해당 스타일이 적용되게 됩니다.

```markup
<h1>Heading</h1>
<h2>Subheading</h2>
<div id="box">I'm a box</div>
```

#### 5. Descendent

```css
#nav li {
  background: blue;
}
```

이 선택 방식은 특정 요소의 하위 요소를 선택할 때 사용됩니다. 두 개의 선택자 사이에 공백을 한 칸 주게 되면, 공백을 기준으로 왼쪽에 명시된 선택자의 하위에 존재하며 왼쪽에 명시된 선택자를 가진 HTML 요소를 선택하게 됩니다. 위 예제에서는 `nav`라는 ID 값을 가진 요소의 하위에 존재하는 모든 `li` 태그 요소들을 선택하여 스타일을 명시하고 있습니다.

```markup
<ul id="nav">
  <li>child</li>
</ul>
```

#### 6. Child

```css
#list > li {
  border: 1px solid black;
}
```

부등호 기호를 위와 같이 사용하여 직속 자식 요소들을 선택할 수도 있습니다. 위 예제의 경우, `list`라는 ID 값을 가진 요소의 직속 자식 요소들 중 `li` 태그 요소들만을 선택하여 스타일을 적용하게 됩니다. 직속 자식이 아닌 손자/손녀 요소 혹은 그 하위 요소들은 제외됩니다.

```markup
<ul id="list">
  <li>child</li>
  <li>child
    <ul>
      <li>grand child</li>
    </ul>
  </li>
</ul>
```

#### 7. Universal

```css
* {
  color: orange;
}
```

위 선택자는 페이지의 모든 요소들을 선택하는 방법입니다.

```markup
<h5>Sub heading</h5>
```

#### 8. Attribute

```css
img[alt="Cat"] {
  border: 1px solid black;
}
```

위 선택자는 `img` 태그들 중 `alt` 속성의 값이 `"Cat"`인 HTML 요소들을 선택하여 스타일을 적용합니다. `alt` 이외의 다른 속성들을 이용하여 선택할 수도 있습니다.

```markup
<img src="myimage.jpg" alt="Cat">
```

### 추가적으로 학습해야 할 자료들

* [MDN - CSS 소개](https://developer.mozilla.org/ko/docs/Learn/CSS/Introduction\_to\_CSS)
* [MDN - CSS 속성 참고 자료](https://developer.mozilla.org/ko/docs/Web/CSS/Reference)
* [반드시 기억해야 하는 CSS 선택자 30개](https://code.tutsplus.com/ko/tutorials/the-30-css-selectors-you-must-memorize--net-16048)
* [게임으로 배우는 CSS](http://flukeout.github.io)
