---
id: 5a90376038fddaf9a66b5d3c
title: Alinhar todos itens horizontalmente utilizand justify-items
challengeType: 0
videoUrl: 'https://scrimba.com/p/pByETK/cJbpECn'
forumTopicId: 301120
dashedName: align-all-items-horizontally-using-justify-items
---

# --description--

Às vezes você quer que todos os itens em seu Grid CSS tenham o mesmo alinhamento. Você pode utilizar as propriedades aprendidas anteriormente e alinha cada item individualmente, ou pode alinhar eles de uma vez por todas utilizando `justify-items` em seu grid container. Esta propriedade pode aceitar todos os mesmo valores que você aprendeu nos dois desafios anteriores, a diferença é que aqui fazer isto dará o alinhamento desejado a  **todos** os itens de seu grid.

# --instructions--

Utilize esta propriedade para centralizar todos os seus itens horizontalmente.

# --hints--

A classe `container` deve ter a propriedade `justify-items`que deve ter o valor `center`.

```js
assert(
  code.match(
    /.container\s*?{[\s\S]*justify-items\s*?:\s*?center\s*?;[\s\S]*}/gi
  )
);
```

# --seed--

## --seed-contents--

```html
<style>
  .item1{background:LightSkyBlue;}
  .item2{background:LightSalmon;}
  .item3{background:PaleTurquoise;}
  .item4{background:LightPink;}
  .item5{background:PaleGreen;}

  .container {
    font-size: 40px;
    min-height: 300px;
    width: 100%;
    background: LightGray;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr;
    grid-gap: 10px;
    /* Only change code below this line */

    
    /* Only change code above this line */
  }
</style>

<div class="container">
  <div class="item1">1</div>
  <div class="item2">2</div>
  <div class="item3">3</div>
  <div class="item4">4</div>
  <div class="item5">5</div>
</div>
```

# --solutions--

```html
<style>.container {justify-items: center;}</style>
```
