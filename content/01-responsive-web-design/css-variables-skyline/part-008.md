---
id: 5d822fd413a79914d39e98d0
title: Parte 8
challengeType: 0
dashedName: part-8
---

# --description--

É difícil ver agora, mas há um border na borda da visualização, que é o body .Crie um elemento `div` no body com uma classe de `background-buildings`. Este será um contêiner para um grupo de edifícios.

# --hints--

texto de teste

```js
assert($("#display-body")[0].contains($("div.background-buildings")[0]));
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
        box-sizing: border-box;
      }

      body {
        height: 100vh;
        margin: 0;
        overflow: hidden;
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

      body {
        height: 100vh;
        margin: 0;
        overflow: hidden;
      }
    </style>
  </head>

  <body>
    <div class="background-buildings"></div>
  </body>
</html>
```
