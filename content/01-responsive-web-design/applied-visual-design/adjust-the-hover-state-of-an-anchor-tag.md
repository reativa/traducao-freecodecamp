---
id: 587d781d367417b2b2512ac8
title: Adjust the Hover State of an Anchor Tag
challengeType: 0
videoUrl: 'https://scrimba.com/c/cakRGcm'
forumTopicId: 301035
dashedName: adjust-the-hover-state-of-an-anchor-tag
---

# --description--

Este desafio abordará o uso de pseudo-classes. Uma pseudo-classe é uma palavra-chave que pode ser adicionada a seletores, a fim de selecionar um estado específico do elemento.

Por exemplo, o estilo de uma tag âncora pode ser alterada para seu estado de foco usando o seletor de pseudo-classe `: hover`. Aqui está o CSS para alterar a `cor` da tag âncora para vermelho durante seu estado de foco:

```css
a:hover {
  color: red;
}
```

# --instructions--

O editor de código tem uma regra CSS para estilizar todas as tags `a` na cor preta. Adicione uma regra para que quando o usuário passar o mouse sobre a tag `a`, a`color` seja azul.

# --hints--

A tag âncora `color` deve permanecer preta, apenas adicione as regras CSS para o estado `:hover`.

```js
assert($('a').css('color') == 'rgb(0, 0, 0)');
```

A tag âncora deve ter uma `cor` azul com o passar do mouse.

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
