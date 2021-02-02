---
id: 5f3477ae34c1239cafe128be
title: Parte 14
challengeType: 0
dashedName: part-14
---

# --description--

Agora você tem três tipos de seletores com exatamente o mesmo estilo. Você pode adicionar o mesmo grupo de estilos para vários elementos separando os seletores com vírgulas, do seguinte modo:

```css
selector1, selector2 {
  property: value;
}
```

Use a single type selector to center the `h1`, `h2` and `p` elements at the same time.

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
    <title>Camper Cafe Menu</title>
--fcc-editable-region--
    <style>
      h1 {
        text-align: center;
      }
      h2 {
        text-align: center;
      }
      p {
        text-align: center;
      }
    </style>
--fcc-editable-region--
  </head>
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

