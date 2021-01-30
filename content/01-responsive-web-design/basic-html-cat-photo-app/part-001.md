---
id: 5dc174fcf86c76b9248c6eb2
title: Part 1
challengeType: 0
dashedName: part-1
---

# --description--

Os elementos HTML têm tags de abertura como `<h1>` e tag de fechamento como `</h1>`.

encontre o elemento `h1` e altere o texto entre as tags de abertura e fechamento para dizer `CatPhotoApp`.

# --hints--

O texto `CatPhotoApp` deve esta presente no código. Você pode querer verificar a ortografia.

```js
assert(code.match(/catphotoapp/i));
```

Seu elemento `h1` deve ter uma tag de abertura. tags de abertura tem essa sintaxe: `<elementName>`.

```js
assert(document.querySelector('h1'));
```

Seu elemento `h1` deve ter uma tag de fechamento. Tag de fechamento `/` logo após o `<` .

```js
assert(code.match(/<\/h1\>/));
```

Você tem mais de um elemento `h1`. Remova o elemento `h1` extra.

```js
assert(document.querySelectorAll('h1').length === 1);
```

Seu elemento `h1` deve ter o texto `CatPhotoApp`. Você omitiu o texto, cometeu um erro de digitação ou ele não está entre as tags de abertura e fechamento do elemento `h1`.

```js
assert(document.querySelector('h1').innerText.toLowerCase() === 'catphotoapp');
```

# --seed--

## --seed-contents--

```html
<html>
  <body>
--fcc-editable-region--
    <h1>Hello World</h1>
--fcc-editable-region--
  </body>
</html>
```

