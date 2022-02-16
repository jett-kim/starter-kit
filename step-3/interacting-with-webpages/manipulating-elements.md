# Manipulating Elements

{% embed url="https://vimeo.com/352501832" %}

DOM을 이용하여 선택한 요소들을 필요에 따라 수정하거나 삭제할 수도 있습니다.

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

위와 같은 HTML 문서가 있고, `h1` 요소의 텍스트를 변경하고 싶은 상황이라고 생각해보세요.

앞선 단계에서 학습했던 방식 중 하나를 이용하여 `h1` 요소를 선택한 후, 해당 요소의 텍스트를 수정해보겠습니다.

```javascript
const $heading = document.querySelector("h1");

$heading.textContent = "I am a NEW Heading";
```

위의 예제처럼 `textContent`란 속성을 이용하여 `h1` 요소의 텍스트 내용을 수정할 수 있습니다.

만약 여러분께서 HTML 요소를 대상으로 어떠한 작업을 해야 하는 상황인데, 어떻게 해야 할지 모르신다면 가장 좋은 방법은 인터넷 검색입니다. `"자바스크립트 HTML 요소 텍스트 수정"` 등의 키워드로 검색하시면 필요한 정보들을 찾으실 수 있습니다. 또한 [Node](https://developer.mozilla.org/ko/docs/Web/API/Node) 문서나 [Element](https://developer.mozilla.org/ko/docs/Web/API/Element) 문서의 왼쪽 "관련 주제"에 나열된 속성이나 메소드를 살펴보시고 적용해볼 수도 있습니다.

[`Node.textContent`](https://developer.mozilla.org/ko/docs/Web/API/Node/textContent)에 대한 페이지에서 아래 쪽 예제 코드를 보시면 방금 위에서 보여드린 방식으로 텍스트를 수정할 수 있음을 알 수 있습니다.

> 구글링한 정보나 MDN에서 찾은 정보를 바로 적용하기 어렵다면 jsbin.com 등의 웹 에디터에서 간단하게 테스트해보세요.

#### 자주 사용할 만한 속성들

아래 나열된 속성이나 메소드는 자주 사용되는 것들이니 반드시 숙지해보시기 바랍니다.

* [Element.children - 자식 요소 가져오기](https://developer.mozilla.org/ko/docs/Web/API/ParentNode/children)
* [Element.classList - 요소의 클래스 정보](https://developer.mozilla.org/ko/docs/Web/API/Element/classList)
* [Element.innerHTML - 요소의 HTML](https://developer.mozilla.org/ko/docs/Web/API/Element/innerHTML)
* [Element.style - 요소의 CSS 스타일](https://developer.mozilla.org/en-US/docs/Web/API/ElementCSSInlineStyle/style)
* [Element.remove - 요소 삭제하기](https://developer.mozilla.org/ko/docs/Web/API/ChildNode/remove)
* [Element.appendChild - 자식 요소 추가하기](https://developer.mozilla.org/ko/docs/Web/API/Node/appendChild)

