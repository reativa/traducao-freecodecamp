---
id: 587d78a3367417b2b2512ad0
title: Centralize um elemento horizontalmente utilizando a propriedade margin
challengeType: 0
videoUrl: 'https://scrimba.com/c/cyLJqU4'
forumTopicId: 301043
dashedName: center-an-element-horizontally-using-the-margin-property
---

# --description--

Outra técnica de posicionamento é centralizar um elemento block horizontalmente. Uma forma de fazer isso é atributir o valor auto à sua propriedade `margin`

Esse método funciona também para imagens. Imagens são elementos inline por padrão, mas podem ser modificadas para elementos block se mudarmos a propriedade `display` para block.

# --instructions--

Centralize a `div` na página atribuindo à propriedade `margin` o valor auto.

# --hints--

A `div` deve ter a `margin` configurada como auto.

```js
assert(code.match(/margin:\s*?auto;/g));
```

# --seed--

## --seed-contents--

```html
<style>
  div {
    background-color: blue;
    height: 100px;
    width: 100px;

  }
</style>
<div></div>
```

# --solutions--

```html
<style>
  div {
    background-color: blue;
    height: 100px;
    width: 100px;
    margin: auto;
  }
</style>
<div></div>
```
