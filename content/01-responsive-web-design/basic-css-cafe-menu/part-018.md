---
id: 5f3477cbcb6ba47918c1da92
title: Parte 18
challengeType: 0
dashedName: part-18
---

# --description--

Como o estilo da página é semelhante no celular e em um computador desktop ou notebook, você precisa adicionar um elemento `meta` com um atributo especial `content`.

Adicione o seguinte no elemento `head`:



```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

# --hints--

Test 1

```js

```

# --seed--

## --seed-contents--

```html
<!DOCTYPE html>
<html>
--fcc-editable-region--
  <head>
    <meta charset="utf-8" />
    <title>Camper Cafe Menu</title>
    <link href="styles.css" rel="stylesheet" type="text/css" />
  </head>
--fcc-editable-region--
  <body>
    <header>
      <h1>CAMPER CAFE</h1>
      <p>Est. 2020</p>
    </header>
    <main>
      <section>
        <h2>Coffees</h2>
      </section>
    </main>
  </body>
<html>
```

```css
h1, h2, p {
  text-align: center;
}
```

