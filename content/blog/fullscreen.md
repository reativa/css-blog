---
date: "2020-01-04"
description: ''
title: CSS como usar o Fullscreen
tags: visual
---

The :fullscreen CSS pseudo-class represents an element that's displayed when the browser is in fullscreen mode.

```html
<div class="container">
  <p><em>Click the button below to enter the element into fullscreen mode. </em></p>
  <div class="element" id="element"><p>I change color in fullscreen mode!</p></div>
  <br />
  <button onclick="var el = document.getElementById('element'); el.requestFullscreen();">
    Go Full Screen!
  </button>
</div>
```

```css
.container {
  margin: 40px auto;
  max-width: 700px;
}

.element {
  padding: 20px;
  height: 300px;
  width: 100%;
  background-color: skyblue;
  box-sizing: border-box;
}

.element p {
  text-align: center;
  color: white;
  font-size: 3em;
}

.element:-ms-fullscreen p {
  visibility: visible;
}

.element:fullscreen {
  background-color: #e4708a;
  width: 100vw;
  height: 100vh;
}
```

#### Explanation

1. `fullscreen` CSS pseudo-class selector is used to select and style an element that is being displayed in fullscreen mode.

#### Browser support

- https://developer.mozilla.org/en-US/docs/Web/CSS/:fullscreen
- https://caniuse.com/#feat=fullscreen

[Acesse a Referência original](http://github.com/30-seconds/)
