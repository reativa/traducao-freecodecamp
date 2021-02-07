---
id: 5d822fd413a79914d39e98cd
title: Parte 5
challengeType: 0
dashedName: part-5
---

# --description--

Em CSS, você pode direcionar tudo com um asterisco. Adicione uma borda a tudo usando o seletor `*` em sua área de estilo e dando a ele uma `border` de `1px solid black`. Esse é um truque que gosto de usar para ajudar a visualizar onde os elementos estão e seus tamanhos. Você removerá isso mais tarde.

# --hints--

texto de teste

```js
assert(
  code.match(
    /<style\s*>\s*\*\s*{\s*border\s*:\s*1px\s+solid\s+black\s*;?\s*}\s*<\/style\s*>/g
  )
);
```

# --seed--

## --seed-contents--

```html
<!DOCTYPE html>
<html>
  <head>
    <title>freeCodeCamp Skyline Project</title>
    <style></style>
  </head>

  <body></body>
</html>
```

# --solutions--

```html
<!DOCTYPE html>
<html>
  <head>
    <title>freeCodeCamp Skyline Project</title>
    <style>
      * {
        border: 1px solid black;
      }
    </style>
  </head>

  <body></body>
</html>
```
