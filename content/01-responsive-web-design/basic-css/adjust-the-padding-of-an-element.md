---
id: bad88fee1348bd9aedf08825
title: Ajuste o preenchimento de um elemento 
challengeType: 0
videoUrl: 'https://scrimba.com/c/cED8ZC2'
forumTopicId: 301083
dashedName: adjust-the-padding-of-an-element
---

# --description--

Agora vamos deixar nosso Cat Photo App de lado por um tempo e aprender mais sobre como estilizar HTML.

Você já deve ter notado isso, mas todos os elementos HTML são essencialmente pequenos retângulos.

Três propriedades importantes controlam o espaço que envolve cada elemento HTML: `padding`,` border` e `margin`.

O `padding` de um elemento controla a quantidade de espaço entre o conteúdo do elemento e sua `border`.

Aqui, podemos ver que a caixa azul e a caixa vermelha estão aninhadas na caixa amarela. Observe que a caixa vermelha tem mais `padding` do que a caixa azul.

Quando você aumenta o `padding` da caixa azul, aumenta a distância (` padding`) entre o texto e a borda ao redor dele. 


# --instructions--

Altere o `padding` da sua caixa azul para corresponder ao da sua caixa vermelha.
# --hints--

Sua classe `blue-box` deve fornecer elementos` 20px` de `padding`. 

```js
assert($('.blue-box').css('padding-top') === '20px');
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
  }

  .blue-box {
    background-color: blue;
    color: #fff;
    padding: 10px;
  }
</style>
<h5 class="injected-text">margin</h5>

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
  }

  .blue-box {
    background-color: blue;
    color: #fff;
    padding: 20px;
  }
</style>
<h5 class="injected-text">margin</h5>

<div class="box yellow-box">
  <h5 class="box red-box">padding</h5>
  <h5 class="box blue-box">padding</h5>
</div>
```
