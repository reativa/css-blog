---
date: "2020-01-04"
description: ''
title: CSS como usar o Grid centering
tags: layout
---

Horizontally and vertically centers a child element within a parent element using `grid`.

```html
<div class="grid-centering"><div class="child">Centered content.</div></div>
```

```css
.grid-centering {
  display: grid;
  justify-content: center;
  align-items: center;
  height: 100px;
}
```

#### Explanation

1. `display: grid` enables grid.
2. `justify-content: center` centers the child horizontally.
3. `align-items: center` centers the child vertically.

#### Browser support

- https://caniuse.com/#feat=css-grid

[Acesse a Referência original](http://github.com/30-seconds/)
