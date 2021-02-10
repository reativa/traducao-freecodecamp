---
id: 587d78a9367417b2b2512ae9
title: Use uma curva de Bézier para mover um Gráfico
challengeType: 0
videoUrl: 'https://scrimba.com/c/c6bnRCK'
forumTopicId: 301071
dashedName: use-a-bezier-curve-to-move-a-graphic
---

# --description--

Um desafio anterior discutiu o valor `ease-out` que descreve uma animação que inicia rápido e então diminui sua velocidade no fim da animação. À direita, é mostrada a diferença entre valor `ease-out` (no elemento azul) e o valor `linear` (no elemento vermelho). Uma progressão de animação similar ao do valor `ease-out` pode ser feito usando uma função cúbica personalizada de uma curva de Bézier (`cubic-bezier`). 

No geral, mudar os pontos `p1` e `p2` leva a criação de diferentes curvas de Bézier, que controla a progressão da animação sobre o tempo. Aqui está um exempor de uma curva e Bézier usando valores para imitar o efeito do estilo ease-out:

`animation-timing-function: cubic-bezier(0, 0, 0.58, 1);`

Lembre-se que todas as funções `cubic-bezier` começam com um ponto `p0` na coordenada (0, 0) e termina em um ponto `p3` na coordenada (1, 1). Nesse exemplo, a curve se move mais rápido no eixo Y (começa no 0, vai até o `p1` de y com valor 0, depois vai para o `p2` de y com valor 1) do que se move através do eixo X (0 para iniciar, depois de 0 em `p1` para 0.58 no `p2`). Como resultade, a modificação da progressão de animação do elemento é mais rápida do que o tempo de animação desse segmento. Mas, próximo ao final da curva, a relação entre a mudança dos valores de x e y fica da seguinte forma - o valor de y se move de 1 para 1 (sem alteração), já o valor de x se move de 0.58 para 1, fazendo com que a progressão da animação fique mais devagar comparado com a duração da animação. 

# --instructions--

Para ver o efeito da curva de Bézier em ação, mude a propriedade `animation-timing-function` do elemento com o id `red` para uma função `cubic-bezier` com os valores x1, y1, x2, y2 definidos respectivamente 0, 0, 0.58, 1. Isso irá deixar as animações de ambos os elementos similares.

# --hints--

O valor da propriedade `animation-timing-function` do elemento com o id `red` deve ser uma função `cubic-bezier` com os valores x1, y1, x2, y2 definidos respectivamente como 0, 0, 0.58, 1 .

```js
assert(
  $('#red').css('animation-timing-function') == 'cubic-bezier(0, 0, 0.58, 1)'
);
```

O elemento com o id `red` não deve ter mais a propriedade `animation-timing-function` com o valor `linear`.

```js
assert($('#red').css('animation-timing-function') !== 'linear');
```

O valor da propriedade `animation-timing-function` para o id `blue` não deve ser alterado.

```js
const blueBallAnimation = __helpers.removeWhiteSpace(
  $('#blue').css('animation-timing-function')
);
assert(
  blueBallAnimation == 'ease-out' ||
    blueBallAnimation == 'cubic-bezier(0,0,0.58,1)'
);
```

# --seed--

## --seed-contents--

```html
<style>
  .balls{
    border-radius: 50%;
    position: fixed;
    width: 50px;
    height: 50px;
    margin-top: 50px;
    animation-name: bounce;
    animation-duration: 2s;
    animation-iteration-count: infinite;
  }
  #red {
    background: red;
    left: 27%;
    animation-timing-function: linear;
  }
  #blue {
    background: blue;
    left: 56%;
    animation-timing-function: ease-out;
  }
  @keyframes bounce {
    0% {
      top: 0px;
    }
    100% {
      top: 249px;
    }
  }
</style>
<div class="balls" id= "red"></div>
<div class="balls" id= "blue"></div>
```

# --solutions--

```html
<style>
  .balls{
    border-radius: 50%;
    position: fixed;
    width: 50px;
    height: 50px;
    margin-top: 50px;
    animation-name: bounce;
    animation-duration: 2s;
    animation-iteration-count: infinite;
  }
  #red {
    background: red;
    left: 27%;
    animation-timing-function: cubic-bezier(0, 0, 0.58, 1);
  }
  #blue {
    background: blue;
    left: 56%;
    animation-timing-function: ease-out;
  }
  @keyframes bounce {
    0% {
      top: 0px;
    }
    100% {
      top: 249px;
    }
  }
</style>
<div class="balls" id= "red"></div>
<div class="balls" id= "blue"></div>
```
