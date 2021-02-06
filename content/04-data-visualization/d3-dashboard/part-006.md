---
id: 5d8a4cfbe6b6180ed9a1c9e3
title: Parte 6
challengeType: 0
dashedName: part-6
---

# --description--

Agora você está olhando para a folha de estilo à qual vinculou anteriormente. No topo deste arquivo, direcione o `body` do documento HTML e dê a ele uma` background-color` de `#ccc`.

# --hints--

test-text

```js
const body = code.match(/body\s*{[\s\S]+?[^}]}/g)[0];
assert(/background-color\s*:\s*#ccc\s*(;|})/gi.test(body));
```

# --seed--

## --before-user-code--

```html
<!DOCTYPE html>
<html>
  <head>
    <title>D3 Dashboard</title>
  </head>

  <body>
    <div class="dashboard"></div>
  </body>
</html>
```

## --seed-contents--

```html
<style>


</style>
```

# --solutions--

```html
<style>
body {
  background-color: #ccc;
}
</style>
```
