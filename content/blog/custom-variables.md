---
date: "2020-01-04"
description: ''
title: CSS como usar o Custom variables
tags: other
---

CSS variables that contain specific values to be reused throughout a document.

```html
<p class="custom-variables">CSS is awesome!</p>
```

```css
:root {
  /* Place variables within here to use the variables globally. */
}

.custom-variables {
  --some-color: #da7800;
  --some-keyword: italic;
  --some-size: 1.25em;
  --some-complex-value: 1px 1px 2px whitesmoke, 0 0 1em slategray, 0 0 0.2em slategray;
  color: var(--some-color);
  font-size: var(--some-size);
  font-style: var(--some-keyword);
  text-shadow: var(--some-complex-value);
}
```

#### Explanation

- The variables are defined globally within the `:root` CSS pseudo-class which matches the root element of a tree representing the document. Variables can also be scoped to a selector if defined within the block.
- Declare a variable with `--variable-name:`.
- Reuse variables throughout the document using the `var(--variable-name)` function.

#### Browser support

- https://caniuse.com/#feat=css-variables

[Acesse a Referência original](http://github.com/30-seconds/)
