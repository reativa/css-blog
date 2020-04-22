---
date: "2020-01-04"
description: ''
title: CSS - Como usar a função Calc()
tags: other
---

A função `calc()` permite ao CSS definir valores com o uso de expressões matemáticas. O valor adotado pela propriedade é o resultado de uma expressão matemática.

```html
<div class="box-example"></div>
```

```css
.box-example {
  height: 280px;
  background: #222 url('https://image.ibb.co/fUL9nS/wolf.png') no-repeat;
  background-position: calc(100% - 20px) calc(100% - 20px);
}
```

#### Explicação

1. Ela permite somar, subtrair, multiplicar e dividir.
2. Pode ser utilizada com unidades de medidas diferentes (pixel e porcentagenm juntas, por exemplo).
3. É permitido aninhar funções `calc()`.
4. Pode ser usada com qualquer propriedade em que `<length>`, `<frequency>`, `<angle>`, `<time>`, `<number>`, `<color>`, ou `<integer>` é permitida, como width, height, font-size, top, left, etc.

#### Suporte a Navegadores

- https://caniuse.com/#feat=calc

[Acesse a Referência original](http://github.com/30-seconds/)
