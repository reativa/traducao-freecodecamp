---
id: 587d78a3367417b2b2512ad0
title: Centralize um elemento horizontalmente utilizando a propriedade margin
challengeType: 0
videoUrl: 'https://scrimba.com/c/cyLJqU4'
forumTopicId: 301043
dashedName: center-an-element-horizontally-using-the-margin-property
---

# --description--


Outra técnica de posicionamento é centralizar um elemento de bloco horizontalmente. Uma maneira de fazer isso é definir sua `margin` para um valor de `auto`.


Este método também funciona com imagens. As imagens são elementos `inline` por padrão, mas podem ser alteradas para elementos `block` quando você define a propriedade `display` para `block`.
# --instructions--


Centralize a `div` na página adicionando uma propriedade `margin` com um valor de auto.
# --hints--

A `div` deve ter uma `margin` definida como `auto`.


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
