---
id: 5a9036ee38fddaf9a66b5d37
title: Adicionar gaps mais rapidamente com grid-gap
challengeType: 0
videoUrl: 'https://scrimba.com/p/pByETK/ca2qVtv'
forumTopicId: 301118
dashedName: add-gaps-faster-with-grid-gap
---

# --description--


`grid-gap` é uma propriedade atalho para `grid-row-gap` e `grid-column-gap` dos dois desafios anteriores que é mais conveniente de usar. Se `grid-gap` tem um valor, criará gaps entre todas as linhas e colunas. Entretanto, se houver dois valores, o primeiro representará gap entre as linhas e o segundo entre as colunas.

# --instructions--

Use `grid-gap` para adicionar um gap de `10px` entre as linhas e `20px`para adicionar gap entre as colunas.

# --hints--

A classe`container` deve ter uma propriedade `grid-gap` que adiciona um gap de `10px` gap entre linhas e um gap de `20px` entre colunas.

```js
assert(
  code.match(
    /.container\s*?{[\s\S]*grid-gap\s*?:\s*?10px\s+?20px\s*?;[\s\S]*}/gi
  )
);
```

# --seed--

## --seed-contents--

```html
<style>
  .d1{background:LightSkyBlue;}
  .d2{background:LightSalmon;}
  .d3{background:PaleTurquoise;}
  .d4{background:LightPink;}
  .d5{background:PaleGreen;}

  .container {
    font-size: 40px;
    min-height: 300px;
    width: 100%;
    background: LightGray;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr;
    /* Only change code below this line */

    
    /* Only change code above this line */
  }
</style>
<div class="container">
  <div class="d1">1</div>
  <div class="d2">2</div>
  <div class="d3">3</div>
  <div class="d4">4</div>
  <div class="d5">5</div>
</div>
```

# --solutions--

```html
<style>.container {grid-gap: 10px 20px;}</style>
```
