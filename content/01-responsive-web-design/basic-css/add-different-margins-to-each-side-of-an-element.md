---
id: bad87fee1248bd9aedf08824
title: Adicionando margens diferentes para cada lado de um elemento.
challengeType: 0
videoUrl: 'https://scrimba.com/c/cg4RWh4'
forumTopicId: 16633
dashedName: add-different-margins-to-each-side-of-an-element
---

# --description--

Às vezes, você desejará personalizar um elemento para que tenha uma `margin` diferente em cada um de seus lados.

O CSS permite que você controle a `margin` de todos os quatro lados individuais de um elemento com as propriedades` margin-top`, `margin-right`,` margin-bottom` e `margin-left`. 

# --instructions--

Dê à caixa azul uma `margem` de` 40px` em seu lado superior e esquerdo, mas apenas `20px` em sua parte inferior e direita. 
# --hints--

Sua classe `blue-box` deve fornecer ` 40px` de `margin` em relação ao topo dos elementos. 

```js
assert($('.blue-box').css('margin-top') === '40px');
```

Sua classe `blue-box` deve fornecer os elementos` 20px` de `margin` direita. 

```js
assert($('.blue-box').css('margin-right') === '20px');
```

Sua classe `blue-box` deve fornecer a parte inferior dos elementos` 20px` de `margin`. 

```js
assert($('.blue-box').css('margin-bottom') === '20px');
```

Sua classe `blue-box` deve dar ` 40px` de `margin` à esquerda dos elementos . 
```js
assert($('.blue-box').css('margin-left') === '40px');
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
    margin-top: 40px;
    margin-right: 20px;
    margin-bottom: 20px;
    margin-left: 40px;
  }

  .blue-box {
    background-color: blue;
    color: #fff;
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
    margin-top: 40px;
    margin-right: 20px;
    margin-bottom: 20px;
    margin-left: 40px;
  }

  .blue-box {
    background-color: blue;
    color: #fff;
    margin-top: 40px;
    margin-right: 20px;
    margin-bottom: 20px;
    margin-left: 40px;
  }
</style>
<h5 class="injected-text">margin</h5>

<div class="box yellow-box">
  <h5 class="box red-box">padding</h5>
  <h5 class="box blue-box">padding</h5>
</div>
```
