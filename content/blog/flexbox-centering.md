---
date: "2020-01-04"
description: ''
title: CSS como usar o Flexbox centering
tags: layout
---

Horizontally and vertically centers a child element within a parent element using `flexbox`.

```html
<div class="flexbox-centering"><div class="child">Centered content.</div></div>
```

```css
.flexbox-centering {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100px;
}
```

#### Explanation

1. `display: flex` enables flexbox.
2. `justify-content: center` centers the child horizontally.
3. `align-items: center` centers the child vertically.

#### Browser support

<span class="snippet__support-note">⚠️ Needs prefixes for full support.</span>

- https://caniuse.com/#feat=flexbox

[Acesse a Referência original](http://github.com/30-seconds/)
