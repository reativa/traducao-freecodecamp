---
id: 587d78a3367417b2b2512acf
title: Alterar a posição de elementos sobrepostos
challengeType: 0
videoUrl: 'https://scrimba.com/c/cM94aHk'
forumTopicId: 301046
dashedName: change-the-position-of-overlapping-elements-with-the-z-index-property
---

# --description--

Quando elementos são posicionados para sobrepor (e.g. usando `position: absolute | relative | fixed | sticky`), o elemento que vem depois na marcação HTML irá, por padrão, aparecer no topo de outros elementos. Entretando, a propriedade `z-index` pode especificar a ordem de como os elementos são empilhados um em cima do outro. Ele deve ser um inteiro (e.g. um número inteiro e não um decimal), e valores altos para a propriedade `z-index` de um elemento o movem mais alto na pilha do que aqueles com valores mais baixos.

# --instructions--

Adicionar uma propriedade `z-index` para o elemento com o nome de classe `first` (o retângulo vermelho) e defina-o com um valor de 2 para cobrir o outro elemento (retângulo azul).

# --hints--

O elemento com a classe `first` deve ter um `z-index` de valor 2.

```js
assert($('.first').css('z-index') == '2');
```

# --seed--

## --seed-contents--

```html
<style>
  div {
    width: 60%;
    height: 200px;
    margin-top: 20px;
  }

  .first {
    background-color: red;
    position: absolute;

  }
  .second {
    background-color: blue;
    position: absolute;
    left: 40px;
    top: 50px;
    z-index: 1;
  }
</style>

<div class="first"></div>
<div class="second"></div>
```

# --solutions--

```html
<style>
  div {
    width: 60%;
    height: 200px;
    margin-top: 20px;
  }

  .first {
    background-color: red;
    position: absolute;
    z-index: 2;
  }
  .second {
    background-color: blue;
    position: absolute;
    left: 40px;
    top: 50px;
    z-index: 1;
  }
</style>
<div class="first"></div>
<div class="second"></div>
```
