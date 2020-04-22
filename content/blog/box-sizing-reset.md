---
date: "2020-01-04"
description: ''
title: CSS - Como usar o Box-sizing Reset
tags: layout
---

Redefine o _box-model_ para que alturas(`height`) e larguras(`width`) não sejam afetadas por suas bordas(`borders`) ou preenchimento(`padding`)

```html
<div class="box">border-box</div>
<div class="box content-box">content-box</div>
```

```css
html {
  box-sizing: border-box;
}
*,
*::before,
*::after {
  box-sizing: inherit;
}
.box {
  display: inline-block;
  width: 150px;
  height: 150px;
  padding: 10px;
  background: tomato;
  color: white;
  border: 10px solid red;
}
.content-box {
  box-sizing: content-box;
}
```

#### Explicação

1. `box-sizing: border-box` faz com que a adição do preenchimento(`padding`) ou das bordas(`borders`) não afete a altura e a largura de um elemento.
2. `box-sizing: inherit` faz um elemento respeitar a regra de `box-sizing` do seu elemento pai.

#### Suporte à Navegadores

- https://caniuse.com/#feat=css3-boxsizing

[Acesse a Referência Original](http://github.com/30-seconds/)
