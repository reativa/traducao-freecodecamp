---
id: 5d7925329445167ecc2ac9c9
title: Parte 4
challengeType: 0
dashedName: part-4
---

# --description--

Em JavaScript, as funções são de primeira classe. Isso significa que elas podem ser usados como quaisquer outros valores - por exemplo, elas podem ser atribuídos a variáveis.

Atribua `add` para uma nova variável `addVar`.

# --hints--

Veja a descrição acima para obter instruções.

```js
assert(code.replace(/\s/g, '').includes('constaddVar=add'));
```

# --seed--

## --before-user-code--

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Spreadsheet</title>
  <style>
    #container {
      display: grid;
      grid-template-columns: 50px repeat(10, 200px);
      grid-template-rows: repeat(11, 30px);
    }
    .label {
      background-color: lightgray;
      text-align: center;
      vertical-align: middle;
      line-height: 30px;
    }
  </style>
</head>
<body>
<div id="container">
  <div></div>
</div>
```

## --after-user-code--

```html
</body>
</html>
```

## --seed-contents--

```html
<script>

function add(x, y) {
  return x + y;
}

const infixToFunction = {};


</script>
```

# --solutions--

```html
<script>
function add(x, y) {
  return x + y;
}

const addVar = add;

const infixToFunction = {};
</script>
```
