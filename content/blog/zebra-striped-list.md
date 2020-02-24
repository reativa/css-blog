---
date: "2020-01-04"
description: ''
title: CSS como usar o Zebra striped list
tags: visual
---

Creates a striped list with alternating background colors, which is useful for differentiating siblings that have content spread across a wide row.

```html
<ul>
  <li>Item 01</li>
  <li>Item 02</li>
  <li>Item 03</li>
  <li>Item 04</li>
  <li>Item 05</li>
</ul>
```

```css
li:nth-child(odd) {
  background-color: #ddd;
}
```

#### Explanation

- Use the `:nth-child(odd)` or `:nth-child(even)` pseudo-class to apply a different background color to elements that match based on their position in a group of siblings.
- Note that you can use it to apply different styles to other HTML elements like div, tr, p, ol, etc.

#### Browser support

https://caniuse.com/#feat=css-sel3

[Acesse a Referência original](http://github.com/30-seconds/)
