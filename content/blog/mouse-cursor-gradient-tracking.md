---
date: "2020-01-04"
description: ''
title: CSS como usar o Mouse cursor gradient tracking
tags: visual, interactivity,advanced
---

A hover effect where the gradient follows the mouse cursor.

```html
<button class="mouse-cursor-gradient-tracking"><span>Hover me</span></button>
```

```css
.mouse-cursor-gradient-tracking {
  position: relative;
  background: #7983ff;
  padding: 0.5rem 1rem;
  font-size: 1.2rem;
  border: none;
  color: white;
  cursor: pointer;
  outline: none;
  overflow: hidden;
}

.mouse-cursor-gradient-tracking span {
  position: relative;
}

.mouse-cursor-gradient-tracking::before {
  --size: 0;
  content: '';
  position: absolute;
  left: var(--x);
  top: var(--y);
  width: var(--size);
  height: var(--size);
  background: radial-gradient(circle closest-side, pink, transparent);
  transform: translate(-50%, -50%);
  transition: width 0.2s ease, height 0.2s ease;
}

.mouse-cursor-gradient-tracking:hover::before {
  --size: 200px;
}
```

```js
var btn = document.querySelector('.mouse-cursor-gradient-tracking')
btn.onmousemove = function(e) {
  var rect = e.target.getBoundingClientRect()
  var x = e.clientX - rect.left
  var y = e.clientY - rect.top
  btn.style.setProperty('--x', x + 'px')
  btn.style.setProperty('--y', y + 'px')
}
```

#### Explanation

1. `--x` and `--y` are used to track the position of the mouse on the button.
2. `--size` is used to keep modify of the gradient's dimensions.
3. `background: radial-gradient(circle closest-side, pink, transparent);` creates the gradient at the correct postion.

#### Browser support

<span class="snippet__support-note">⚠️ Requires JavaScript.</span>

- https://caniuse.com/#feat=css-variables

[Acesse a Referência original](http://github.com/30-seconds/)
