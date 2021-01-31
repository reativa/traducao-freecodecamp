---
id: bad87fee1348bd9aedf08823
title: Add a Negative Margin to an Element
challengeType: 0
videoUrl: 'https://scrimba.com/c/cnpyGs3'
forumTopicId: 16166
dashedName: add-a-negative-margin-to-an-element
---

# --description--

Um elemento `margin` controla a quantidade de espaço entre a `border` de um elemento e os demais elementos.

Se você definir a `margin` de um elemento com um valor negativo, o elemento ficará maior.

# --instructions--

Tente definir a `margin` para um valor negativo, como a da caixa vermelha.


Altere a `margin` da caixa azul para `-15px`, de forma que preencha toda a largura horizontal da caixa amarela ao redor dela. 

# --hints--

Sua classe `blue-box` deve fornecer elementos  `-15px` de `margin`. 

```js
assert($('.blue-box').css('margin-top') === '-15px');
```

# --seed--

## --seed-contents--

```html
<style>
  .injected-text {
    margin-bottom: -25px;
    text-align: center;
  }

  .box {
    border-style: solid;
    border-color: black;
    border-width: 5px;
    text-align: center;
  }

  .yellow-box {
    background-color: yellow;
    padding: 10px;
  }

  .red-box {
    background-color: crimson;
    color: #fff;
    padding: 20px;
    margin: -15px;
  }

  .blue-box {
    background-color: blue;
    color: #fff;
    padding: 20px;
    margin: 20px;
  }
</style>

<div class="box yellow-box">
  <h5 class="box red-box">padding</h5>
  <h5 class="box blue-box">padding</h5>
</div>
```

# --solutions--

```html
<style>
  .injected-text {
    margin-bottom: -25px;
    text-align: center;
  }

  .box {
    border-style: solid;
    border-color: black;
    border-width: 5px;
    text-align: center;
  }

  .yellow-box {
    background-color: yellow;
    padding: 10px;
  }

  .red-box {
    background-color: crimson;
    color: #fff;
    padding: 20px;
    margin: -15px;
  }

  .blue-box {
    background-color: blue;
    color: #fff;
    padding: 20px;
    margin: 20px;
    margin-top: -15px;
  }
</style>

<div class="box yellow-box">
  <h5 class="box red-box">padding</h5>
  <h5 class="box blue-box">padding</h5>
</div>
```
