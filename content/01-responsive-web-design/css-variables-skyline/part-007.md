---
id: 5d822fd413a79914d39e98cf
title: Parte 7
challengeType: 0
dashedName: part-7
---

# --description--

Você pode ver o body, é a linha horizontal em sua página; a caixa ao redor é o elemento html. Faça seu body preencher toda a janela de visualização, dando-lhe uma `height` de` 100vh`. Remova a margem padrão do body, definindo o `margin` para `0`. Finalmente, defina a propriedade de `overflow` para `hidden` para ocultar as barras de rolagem que aparecem quando algo ultrapassa a janela de visualização.

# --hints--

texto de teste

```js
const body = code.match(/body\s*{[\s\S]+?[^}]}/g)[0];
assert(
  /height\s*:\s*100vh\s*(;|})/g.test(body) &&
    /margin\s*:\s*(0|0px)\s*(;|})/g.test(body) &&
    /overflow\s*:\s*hidden\s*(;|})/g.test(body)
);
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

  <body></body>
</html>
```
