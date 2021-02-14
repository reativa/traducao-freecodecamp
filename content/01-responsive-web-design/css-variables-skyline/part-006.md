---
id: 5d822fd413a79914d39e98ce
title: Parte 6
challengeType: 0
dashedName: part-6
---

# --description--

Também adicione um `box-sizing` em` border-box` para tudo. Isso fará com que a borda que você adicionou não adicione nenhum tamanho aos seus elementos.

# --hints--

texto de teste

```js
assert($("#display-body").css("box-sizing") === "border-box");
```

# --seed--

## --seed-contents--

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

# --solutions--

```html
<!DOCTYPE html>
<html>
  <head>
    <title>freeCodeCamp Skyline Project</title>
    <style>
      * {
        border: 1px solid black;
        box-sizing: border-box;
      }
    </style>
  </head>

  <body></body>
</html>
```
