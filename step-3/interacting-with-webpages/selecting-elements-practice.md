# 🖋  Selecting Elements Practice

### Quiz #1

```javascript
/*

  < Selecting Elements basic 1 >

  💬 를 적절한 값으로 고쳐주세요!

*/

const $p1 = document.getElementById("first-item");
const $p2 = document.getElementsByClassName("third-item");

const text1 = $p1.textContent;
const text2 = $p2[0].textContent;

const result = text1 + text2;

if (result === 💬) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/rNYapVK?editors=1010)



### Quiz #2

```javascript
/*

  < Selecting Elements basic 2 >

  💬 를 적절한 값으로 고쳐주세요!

*/

const $li = document.getElementsByTagName("li");
const $p = document.getElementsByTagName("p");

const text1 = $li[2].textContent;
const text2 = $p[1].textContent;

const result = text1 + text2;

if (result === 💬) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/zYPxpqm)



### Quiz #3

```javascript
/*

  < Selecting Elements basic 3 >

  💬 를 적절한 값으로 고쳐주세요!

*/

const $item = document.querySelectorAll(".item");
const $li = document.querySelectorAll("li");

const length1 = $item.length;
const length2 = $li.length;

const result = length1 + length2;

if (result === 💬) {
  alert("🎉");
}
```

[Codepen에서 직접 해보기](https://codepen.io/vanillacoding/pen/mdqypre?editors=1010)
