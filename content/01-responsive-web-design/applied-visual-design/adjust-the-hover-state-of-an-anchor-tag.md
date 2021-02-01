---
id: 587d781d367417b2b2512ac8
title: Adjust the Hover State of an Anchor Tag
challengeType: 0
videoUrl: 'https://scrimba.com/c/cakRGcm'
forumTopicId: 301035
dashedName: adjust-the-hover-state-of-an-anchor-tag
---

# --description--

Este desafio envolverá o uso de pseudo-classes. Uma pseudo-classe é uma palavra chave que pode ser adicionada aos seletores, de forma a selecionar um estado específico de um elemento.

Por exemplo, o estilo de uma tag âncora pode ser modificada no movimento de passar o mouse usando o seletor de pseudo-classe `:hover`. Aqui está o código CSS que muda a `color` de uma tag âncora para vermelho durante o movimento de passar do mouse:

```css
a:hover {
  color: red;
}
```

# --instructions--

O editor de código tem uma regra CSS para estilizar todas as tags `a` para preto. Adicione uma regra para que quando o mouse passe sobre a tag `a`, a cor seja `blue`.

# --hints--

A `color` da tag âncora deverá permanecer preto, adicione somente a regra CSS para o estado `:hover`.

```js
assert($('a').css('color') == 'rgb(0, 0, 0)');
```

The anchor tag should have a `color` of blue on hover.

```js
assert(
  code.match(
    /a:hover\s*?{\s*?color:\s*?(blue|rgba\(\s*?0\s*?,\s*?0\s*?,\s*?255\s*?,\s*?1\s*?\)|#00F|rgb\(\s*?0\s*?,\s*?0\s*?,\s*?255\s*?\))\s*?;\s*?}/gi
  )
);
```

# --seed--

## --seed-contents--

```html
<style>
  a {
    color: #000;
  }



</style>
<a href="https://freecatphotoapp.com/" target="_blank">CatPhotoApp</a>
```

# --solutions--

```html
<style>
  a {
    color: #000;
  }
  a:hover {
    color: rgba(0,0,255,1);
  }
</style>
<a href="https://freecatphotoapp.com/" target="_blank">CatPhotoApp</a>
```
