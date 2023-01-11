# 📗  DOM Introduction

{% embed url="https://vimeo.com/787837408/b877893269" %}

### Document Object Model

[MDN](https://developer.mozilla.org/en-US/docs/Web/API/Document\_Object\_Model/Introduction)에서 말하는 **Document Object Model**의 정의는 다음과 같습니다.

> The Document Object Model (DOM) is a programming interface for HTML.
>
> (번역) DOM이란 HTML 문서를 위한 프로그래밍 인터페이스입니다.

프로그래밍 인터페이스라는 용어가 생소하신가요? 구글링을 한번 해볼까요?

[위키피디아](https://en.wikipedia.org/wiki/Application\_programming\_interface)에 의하면, 프로그래밍 인터페이스(혹은 Applicataion Programming Interface a.k.a API)의 정의는 다음과 같습니다.

> An application programming interface (API) is a computing interface which defines interactions between multiple software intermediaries.
>
> (의역) 쉽게 말해, 여러 소프트웨어 간의 교류를 가능하게 해주는 표면 같은 존재입니다.

예를 들어, 금요일 밤 여러분이 집에서 TV를 시청한다고 생각해보세요.

SBS 정글의 법칙을 시청하다가 병만족의 행태가 남사스러워 MBC의 나혼자산다를 보려고 합니다. 그리고 채널을 바꾸기 위해 리모콘을 찾습니다. 리모콘에는 다양한 종류의 버튼들이 있고, 우리는 이 버튼들을 이용하여 TV와 교류할 수 있습니다. 물론 우리가 원하는 채널로 변경할 수도 있습니다.

위와 같은 상황에서 우리에게 주어진 리모콘의 표면에 있는 버튼들이 프로그래밍 인터페이스와 같은 역할을 한다고 생각하시면 됩니다. 여러분은 주어진 인터페이스를 이용하여 원하는대로 TV를 조종할 수 있습니다.

마찬가지로 DOM이라는 인터페이스를 이용한다면, 여러분은 HTML 문서를 조종할 수 있습니다.

```javascript
const $text = document.querySelector(".some-text");
$text.textContent = "Hello, World";
```

위 코드에서 우리는 `.some-text`라는 클래스를 가진 요소를 선택하여 해당 요소의 텍스트를 수정하였습니다. 즉, 자바스크립트를 이용하여 HTML 문서를 조종할 수 있는 것이고, DOM이라는 프로그래밍 인터페이스가 있기에 가능한 것입니다.

#### HTML 문서를 조종한다?

사실 정확히 말하자면, 우리는 자바스크립트를 이용하여 HTML 문서를 조종하는 것은 아닙니다.

HTML 문서란, 브라우저가 화면을 그리기 위한 **초기 설계도의 역할**을 할 뿐입니다. 브라우저는 HTML이라는 설계도를 이용하여 초기 화면을 그리게 되고, 우리는 브라우저가 만든 이 화면을 DOM으로 접근하고 조종하게 되는 것입니다.

**즉, 우리가 자바스크립트로 화면을 수정한다고해서 여러분이 작업한 HTML 문서 자체가 수정되는 것은 아니라는 의미입니다.**

그렇다면 DOM 인터페이스를 이용하여 어떤 작업들을 할 수 있는지 조금 더 자세히 살펴볼까요?
