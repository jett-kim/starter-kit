# 🖋  CSS 선택자 Practice

### Selector (1)

태그 선택자를 사용해 스타일을 적용시켜 봅니다.

```css
tag {
  background-color: navy;
}
```

[Codepen으로 직접 해보기](https://codepen.io/vanillacoding/pen/LYOpxOO)

### Selector (2)

클래스 선택자를 사용해 스타일을 적용시켜 봅니다.

```css
.class {
  background-color: orange;
}
```

[Codepen으로 직접 해보기](https://codepen.io/vanillacoding/pen/mdqeRpG?editors=1100)

### Selector (3)

아이디 선택자를 사용해 스타일을 적용시켜 봅니다.

```css
#id {
  background-color: orange;
}
```

[Codepen으로 직접 해보기](https://codepen.io/vanillacoding/pen/jOabyZO?editors=1100)

### Selector (4)

HTML 구조에 따라 엘리먼트를 선택해서 스타일을 적용할 수 있습니다.

```css
/* div 태그 내부에 있는 "모든 p 태그" 에게 해당 스타일을 적용 */
div p {
  background-color: navy;
}

/* div 태그의 "직계 후손 p 태그에게만" 해당 스타일을 적용 */
div > p {
  background-color: pink;
}
```

[Codepen으로 직접 해보기](https://codepen.io/vanillacoding/pen/LYOpxQO?editors=1100)



### margin

margin은 엘리먼트의 바깥쪽 여백과 관련된 속성입니다.

```css
div {
  margin: 10px;
}
```

[Codepen으로 직접 해보기](https://codepen.io/vanillacoding/pen/WNXQRMV?editors=1100)

### padding

padding은 엘리먼트의 안쪽 여백과 관련된 속성입니다.

```css
div {
  padding: 10px;
}
```

[Codepen으로 직접 해보기](https://codepen.io/vanillacoding/pen/abVvpYw)



### font family

CSS를 사용해 HTML 태그 내부의 텍스트에 원하는 폰트를 적용시킬 수 있습니다.

```css
p {
  font-family: "Font Name"
}
```

[Codepen으로 직접 해보기](https://codepen.io/vanillacoding/pen/OJOyWvq?editors=1100)
