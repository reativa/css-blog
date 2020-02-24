---
date: "2020-01-04"
description: ''
title: CSS como usar o Lobotomized Owl Selector  
tags: layout, beginner  
---

Sets an automatically inherited margin for all elements that follow other elements in the document.

```html
<div>
  <div>Parent 01</div>
  <div>Parent 02
    <div>Child 01</div>
    <div>Child 02</div>
  </div>
  <div>Parent 03</div>
</div>
```

```css
* + * {
  margin-top: 1.5em;
}
```

#### Explanation

- [View this link for a detailed explanation.](https://alistapart.com/article/axiomatic-css-and-lobotomized-owls/)
- In this example, all elements in the flow of the document that follow other elements will receive `margin-top: 1.5em`.
- This example assumes that the paragraphs' `font-size` is 1em and its `line-height` is 1.5.

#### Browser support

[Acesse a Referência original](http://github.com/30-seconds/)
