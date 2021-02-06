---
id: 5d8a4cfbe6b6180ed9a1c9ea
title: Parte 13
challengeType: 0
dashedName: part-13
---

# --description--

Adicione outro `script` abaixo do que você acabou de adicionar. Dê a ele um atributo `src` com `./data.js`.

Isso adiciona uma variável `data` ao seu projeto que contém o seu número de seguidores de mídia social, isso é um array de objetos. Cada objeto tem o ano e o seus seguidores para três plataformas diferentes. Você verá como funciona em breve.

# --hints--

test-text

```js
const script = code.match(/<script\s+[\s\S]+?[^>]>\s*<\/script\s*>/gi)[1];
assert(/src\s*=\s*('|")\s*(\.\/)?data.js\s*\1/gi.test(script));
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
<script>
  const data = [ 
    { year: 2012, followers: { twitter: 2594, tumblr:  401, instagram:   83 }},
    { year: 2013, followers: { twitter: 3049, tumblr:  440, instagram:  192 }},
    { year: 2014, followers: { twitter: 3511, tumblr:  415, instagram:  511 }},
    { year: 2015, followers: { twitter: 3619, tumblr:  492, instagram: 1014 }},
    { year: 2016, followers: { twitter: 4046, tumblr:  543, instagram: 2066 }},
    { year: 2017, followers: { twitter: 3991, tumblr:  701, instagram: 3032 }},
    { year: 2018, followers: { twitter: 3512, tumblr: 1522, instagram: 4512 }},
    { year: 2019, followers: { twitter: 3274, tumblr: 1989, instagram: 4715 }},
    { year: 2020, followers: { twitter: 2845, tumblr: 2040, instagram: 4801 }}
  ];
</script>
```

## --seed-contents--

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

# --solutions--

```html
<!DOCTYPE html>
<html>
  <head>
    <title>D3 Dashboard</title>
    <link rel="stylesheet" href="./dashboard.css">
    <script src="./d3-5.9.2.min.js"></script>
    <script src="./data.js"></script>
  </head>

  <body>
    <div class="dashboard"></div>

    
  </body>
</html>
```
