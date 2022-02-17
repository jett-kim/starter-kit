# 🖋  Events Practice

### Quiz #1

```javascript
/*

  < Events basic 1 >

  Button1을 눌럿을 때, Button2와 같이 "🎉"메세지와 함께
  
  알림창이 나나탈 수 있도록 button1Element에 이벤트를 등록시켜 주세요!

  🚨 HTML, CSS는 수정하지 않고 JS만 수정해주세요.

*/

const button1Element = document.querySelector(".button1");
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/jOaNrgK?editors=1010)



### Quiz #2

```javascript
/*

  < Function basic 2 >

  💬 를 적절한 값으로 고쳐주세요!

*/

function greetingMaker(greet, name) {
  return `💬`;
}

const hello = greetingMaker("Hello", "Jett");
const goodBye = greetingMaker("Goodbye", "Justin");

const result = (hello === "Hello, Jett") && (goodBye === "Goodbye, Justin");

if (result) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/JjOPREY?editors=1010)



### Quiz #3

```javascript
/*

  < 신호등 불 켜기 >

  다음과 같은 조건을 만족하여 신호등의 불이 켜질수 있도록 만들어 주세요!
  
  📌 Stop, Pause, Go 클릭 시 빨간색, 주황색, 초록색불이 들어와야 합니다.
  📌 전체 불 끄기 버튼을 클릭하면 모든 불이 꺼져야 합니다.
  
  🚨 HTML, CSS는 수정하지 않고 JS만 수정해주세요.

*/

const buttonElement = document.querySelector("button");
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/RwjboYd)
