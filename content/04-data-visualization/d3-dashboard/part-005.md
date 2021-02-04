---
id: 5d8a4cfbe6b6180ed9a1c9e2
title: Parte 5
challengeType: 0
dashedName: part-5
---

# --description--

Em seguida, adicione um contêiner para o painel. Coloque um elemento `div` vazio no corpo com uma classe `dashboard`. Você irá adicionar todos os elementos do painel dentro da div.

# --hints--

test-text

```js
assert($('div.dashboard').length === 1);
```

# --seed--

## --seed-contents--

```html
<!DOCTYPE html>
<html>
  <head>
    <title>D3 Dashboard</title>
    <link rel="stylesheet" href="./dashboard.css">
  </head>

  <body>

  
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

    
  </head>

  <body>
    <div class="dashboard"></div>
  </body>
</html>
```
