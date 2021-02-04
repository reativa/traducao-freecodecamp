---
id: 5d8a4cfbe6b6180ed9a1c9e1
title: Part 4
challengeType: 0
dashedName: part-4
---

# --description--
Abaixo do título, crie um link para sua folha de estilo externa adicionando um elemento `link` com um atributo` rel` de `stylesheet` e um atributo` href` de `. / Dashboard.css`. Lembre-se de que os elementos do link não precisam de uma tag de fechamento. Você adicionará alguns estilos a este arquivo em breve.

# --hints--

test-text

```js
const link = code.match(/<link\s+[\s\S]+?[^>]>/gi)[0];
assert(
  /rel\s*=\s*('|")\s*stylesheet\s*\1/gi.test(link) &&
    /href\s*=\s*('|")\s*(.\/)?dashboard\.css\s*\1/gi.test(link)
);
```

# --seed--

## --seed-contents--

```html
<!DOCTYPE html>
<html>
  <head>
    <title>D3 Dashboard</title>

    
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
  </body>
</html>
```
