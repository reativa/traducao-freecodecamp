---
id: 5f356ed656a336993abd9f7c
title: Parte 26
challengeType: 0
dashedName: part-26
---

# --description--

Em seguida, você deseja centralizar a `div` horizontalmente. Você pode fazer isso ao definir suas propriedades `margin-left` e `margin-right` para `auto`. Pense na margem como um espaço invisível ao redor do elemento. Usando estas duas propriedades de margem, centralize o elemento `div` dentro do elemento `body`.

# --hints--

Test 1

```js

```

# --seed--

## --seed-contents--

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Camper Cafe Menu</title>
    <link href="styles.css" rel="stylesheet" type="text/css" />
  </head>
  <body>
    <div>
      <header>
        <h1>CAMPER CAFE</h1>
        <p>Est. 2020</p>
      </header>
      <main>
        <section>
          <h2>Coffees</h2>
        </section>
      </main>
    </div>
  </body>
<html>
```

```css
body {
  /*
  background-color: burlywood;
  */
}

h1, h2, p {
  text-align: center;
}

--fcc-editable-region--
div {
  width: 80%;
  background-color: burlywood;
}
--fcc-editable-region--
```

