---
date: "2020-01-04"
description: ''
title: CSS - Borda com Triângulo no Topo (balãozinho)
tags: visual,beginner
---

Cria um container de texto com um triângulo no topo (balãozinho).

```html
<div class="container">
  Borda com Triângulo no Topo
</div>
```

```css
.container {
  position: relative;
  background: #ffffff;
  padding: 15px;
  border: 1px solid #dddddd;
  margin-top: 20px;
}

.container:before, .container:after {
  content: '';
  position: absolute;
  bottom: 100%;
  left: 19px;
  border: 11px solid transparent;
  border-bottom-color: #dddddd;
}

.container:after {
  left: 20px;
  border: 10px solid transparent;
  border-bottom-color: #ffffff;
}
```

#### Explicação

- Use os pseudo-elementos `:before` e `:after` para criar dois triângulos.
- A cor do triângulo de `:before` deve ter a mesma cor da borda do container.
- A cor do triângulo de `:after` deve ter a mesma cor de fundo do container.
- A largura da borda do triângulo de `:before` deve ser `1px` mais larga do que a do triângulo de `:after`, servindo assim de borda do triângulo.
- O triângulo de `:after` deve ser de `1px` para a direita do triângulo de `:before` para permitir que sua borda esquerda seja mostrada.

#### Browser Support

100.0%

[Acesse a Referência original](http://github.com/30-seconds/)
