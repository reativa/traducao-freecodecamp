---
id: 5d8a4cfbe6b6180ed9a1c9df
title: Parte 2
challengeType: 0
dashedName: part-2
---

# --description--

Em seguida, adicione as tags de abertura e fechamento `html`, `head` e `body` abaixo do doctype. Certifique-se de aninhá-los corretamente.

# --hints--

test-text

```js
assert(
  /<!DOCTYPE\s+html\s*>\s*<html\s*>\s*<head\s*>\s*<\/head\s*>\s*<body\s*>\s*<\/body\s*>\s*<\/html\s*>/gi.test(
    code
  )
);
```

# --seed--

## --seed-contents--

```html
<!DOCTYPE html>
```

# --solutions--

```html
<!DOCTYPE html>
<html>
  <head>
  </head>

  <body>
  </body>
</html>
```
