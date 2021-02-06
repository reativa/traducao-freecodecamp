---
id: 5d8a4cfbe6b6180ed9a1c9e7
title: Parte 10
challengeType: 0
dashedName: part-10
---

# --description--

Dê ao contâiner algum espaço adicionando um `padding` de `100px 10px` ao elemento `body`.

# --hints--

test-text

```js
const body = code.match(/body\s*{[\s\S]+?[^}]}/g)[0];
assert(/padding\s*:\s*100px\s*10px\s*(;|})/g.test(body));
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
body {
  background-color: #ccc;

  
}

.dashboard {
  width: 980px;
  height: 500px;
  background-color: white;
  box-shadow: 5px 5px 5px 5px #888;
  margin: auto;
}
</style>
```

# --solutions--

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
}
</style>
```
