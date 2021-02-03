---
id: 5d79253297c0ebb149ea9fed
title: Parte 1
challengeType: 0
dashedName: part-1
---

# --description--

Na programação funcional, preferimos os valores imutáveis em vez de valores mutáveis.

Valores mutáveis (declarado com `var` ou `let`) podem levar a comportamentos e bugs inesperados. Os valores declarados como `const` não podem ser reatribuídos, o que facilita a sua utilização, pois não é necessário manter um controle dos seus valores.

Comece criando um objeto vazio `infixToFunction` usando `const`.

# --hints--

Veja a descrição acima para obter as instruções.

```js
assert(code.replace(/\s/g, '').includes('constinfixToFunction={}'));
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


</script>
```

# --solutions--

```html
<script>
const infixToFunction = {};
</script>
```
