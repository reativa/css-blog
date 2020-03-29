---
date: "2020-01-04"
description: ''
title: CSS - como usar o Bouncing Loader
tags: animação, intermedário
---

Cria uma animação _bouncing loarder_.

```html
<div class="bouncing-loader">
  <div></div>
  <div></div>
  <div></div>
</div>
```

```css
@keyframes bouncing-loader {
  to {
    opacity: 0.1;
    transform: translate3d(0, -1rem, 0);
  }
}
.bouncing-loader {
  display: flex;
  justify-content: center;
}
.bouncing-loader > div {
  width: 1rem;
  height: 1rem;
  margin: 3rem 0.2rem;
  background: #8385aa;
  border-radius: 50%;
  animation: bouncing-loader 0.6s infinite alternate;
}
.bouncing-loader > div:nth-child(2) {
  animation-delay: 0.2s;
}
.bouncing-loader > div:nth-child(3) {
  animation-delay: 0.4s;
}
```

#### Explicação

Nota: `1rem` normalmente equivale a `16px`.

1. `@keyframes` define uma animação que tem dois estados, onde o elemento muda a opacidade(`opacity`) e é transladado no plano 2D através de `transform: translate3d()`. Usando apenas um eixo de transladação em `transform: translate3d()` melhora a performance da animação.
2. `.bouncing-loader` é o _container_ pai da animação(_bouncing circles_) e usa `display: flex` e `justify-content: center` para posicioná-los no centro.
3. `.bouncing-loader > div` marca a árvore de três elementos `div`s filhos do elemento pai para ser estilizado. As `div`s recebem largura e altura de `1rem`, usando `border-radius: 50%` para transformar quadrados em círculos.
4. `margin: 3rem 0.2rem` determina que cada círculo tem uma margem inferior/superior de `3rem` e uma margem direita/esquerda de `0.2rem`, assim elas não tocam diretamente uma nas outras, dando a elas um espaço para "respirar".
5. `animation` é uma forma abreviada de várias propriedades de animação: `animation-name`, `animation-duration`, `animation-iteration-count`, `animation-direction` são usadas.
6. `nth-child(n)` marca qual é o enésimo elemento filho do elemento pai.
7. `animation-delay` é usado na segunda e na terceira `div` respectivamente, assim cada elemento não inicia a animação ao mesmo tempo.


#### Suporte a Navegadores

- https://caniuse.com/#feat=css-animation


#### Notas de Tradução

1. A função `translate3d()` [aceita três argumentos](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/translate3d):
   1. `tx` - referente ao eixo `x`
   2. `ty` - referente ao eixo `y`
   3. `tz` - referente ao eixo `z`

Nesse exemplo, zeramos os eixos `x` e `z`, para definimos o valor de `y` a `-1rem` para que os círculos pulem apenas na horizontal, respeitando o limite de `1rem`.

2. `rem` é uma abreviação para `root element` e é uma unidade de medida relativa, sendo recomendada, pela [w3.org](https://www.w3.org/TR/css-values-3/#font-relative-lengths), para estilizar o comprimento de elementos tipográficos(fontes).

[Acesse a Referência original](http://github.com/30-seconds/)
