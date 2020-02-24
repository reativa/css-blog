---
date: "2020-01-04"
description: ''
title: CSS como usar o Constant width to height ratio
tags: layout
---

Given an element of variable width, it will ensure its height remains proportionate in a responsive fashion
(i.e., its width to height ratio remains constant).

```html
<div class="constant-width-to-height-ratio"></div>
```

```css
.constant-width-to-height-ratio {
  background: #333;
  width: 50%;
}
.constant-width-to-height-ratio::before {
  content: '';
  padding-top: 100%;
  float: left;
}
.constant-width-to-height-ratio::after {
  content: '';
  display: block;
  clear: both;
}
```

#### Explanation

- `padding-top` on the `::before` pseudo-element causes the height of the element to equal a percentage of its width. `100%` therefore means the element's height will always be `100%` of the width, creating a responsive square.
- This method also allows content to be placed inside the element normally.

#### Browser support

[Acesse a Referência original](http://github.com/30-seconds/)
