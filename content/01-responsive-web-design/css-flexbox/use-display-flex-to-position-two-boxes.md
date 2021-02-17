---
id: 587d78ab367417b2b2512af0
title: 'Use display: Posicione Duas Caixas com flex'
challengeType: 0
videoUrl: 'https://scrimba.com/p/pVaDAv/cgz3QS7'
forumTopicId: 301105
dashedName: use-display-flex-to-position-two-boxes
---

# --description--

Esta seção usa estilos de desafio alternados para mostrar como usar CSS para posicionar elementos de maneira flexível. Primeiro, um desafio explicará a teoria, depois um desafio prático usando um componente de tweet simples aplicará o conceito do flexbox.

Colocar a propriedade CSS `display: flex;` em um elemento permite que você use outras propriedades flex para construir uma página responsiva.

# --instructions--

Adicione a propriedade do CSS `display` ao `#box-container` e defina seu valor para `flex`.

# --hints--

`#box-container` deve possuir a propriedade `display` definida como `flex`.

```js
assert($('#box-container').css('display') == 'flex');
```

# --seed--

## --seed-contents--

```html
<style>
  #box-container {
    height: 500px;

  }

  #box-1 {
    background-color: dodgerblue;
    width: 50%;
    height: 50%;
  }

  #box-2 {
    background-color: orangered;
    width: 50%;
    height: 50%;
  }
</style>
<div id="box-container">
  <div id="box-1"></div>
  <div id="box-2"></div>
</div>
```

# --solutions--

```html
<style>
  #box-container {
    height: 500px;
    display: flex;
  }

  #box-1 {
    background-color: dodgerblue;
    width: 50%;
    height: 50%;
  }

  #box-2 {
    background-color: orangered;
    width: 50%;
    height: 50%;
  }
</style>
<div id="box-container">
  <div id="box-1"></div>
  <div id="box-2"></div>
</div>
```
