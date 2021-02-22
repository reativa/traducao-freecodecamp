---
id: 5a9036d038fddaf9a66b5d32
title: Adicionar colunas com grid-template-columns
challengeType: 0
videoUrl: 'https://scrimba.com/p/pByETK/c7NzDHv'
forumTopicId: 301117
dashedName: add-columns-with-grid-template-columns
---

# --description--

Simplismente criar um elemento de grid não o leva a tão longe. Você precisa definir a estrutura do grid também. Para adicionar algumas colunas ao grid, use a propriedade `grid-template-columns` em um container grid como demostrado abaixo:

```css
.container {
  display: grid;
  grid-template-columns: 50px 50px;
}
```

Isto irá dar ao grid duas colunas cada uma com 50px de largura. O número de parâmetros dado a propriedade `grid-template-columns` indica o número de colunas no grid, e o valor de cada parâmetro indica a largura de cada coluna. 

# --instructions--

Dê ao container grid três colunas com `100px` de largura cada.

# --hints--

A classe `container` deve ter uma propriedade `grid-template-columns` com três unidades de `100px`.

```js
assert(
  code.match(
    /.container\s*?{[\s\S]*grid-template-columns\s*?:\s*?100px\s*?100px\s*?100px\s*?;[\s\S]*}/gi
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
    width: 100%;
    background: LightGray;
    display: grid;
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
<style>.container {grid-template-columns: 100px 100px 100px;}</style>
```
