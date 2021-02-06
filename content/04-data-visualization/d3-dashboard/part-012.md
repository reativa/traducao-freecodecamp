---
id: 5d8a4cfbe6b6180ed9a1c9e9
title: Parte 12
challengeType: 0
dashedName: part-12
---

# --description--

De volta ao arquivo HTML, adicione uma tag `script` no fim do elemento head e dê a ele um atributo `src` com `./d3-5.9.2.min.js`. Não esqueça da tag de fechamento.
Isso adicionará a biblioteca D3 para o seu projeto, a partir de um cópia baixada.

# --hints--

test-text

```js
const script = code.match(/<script\s+[\s\S]+?[^>]>\s*<\/script\s*>/gi)[0];
assert(/src\s*=\s*('|")\s*(\.\/)?d3-5.9.2.min.js\s*\1/gi.test(script));
```

# --seed--

## --before-user-code--

```html
<style>
  body {
    background-color: #ccc;
    padding: 100px 10px;
  }

  .dashboard {
    width: 980px;
    height: 500px;
    background-color: white;
    box-shadow: 5px 5px 5px 5px #888;
    margin: auto;
    display: flex;
    align-items: center;
  }
</style>
```

## --seed-contents--

```html
<!DOCTYPE html>
<html>
  <head>
    <title>D3 Dashboard</title>
    <link rel="stylesheet" href="./dashboard.css">

    
  </head>

  <body>
    <div class="dashboard"></div>
  </body>
</html>
```

# --solutions--

```html
<!DOCTYPE html>
<html>
  <head>
    <title>D3 Dashboard</title>
    <link rel="stylesheet" href="./dashboard.css">
    <script src="./d3-5.9.2.min.js"></script>

    
 </head>

  <body>
    <div class="dashboard"></div>
  </body>
</html>
```
