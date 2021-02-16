---
id: bad87fee1348bd9aedf08802
title: Descomentar HTML
challengeType: 0
videoUrl: 'https://scrimba.com/p/pVMPUv/cBmG9T7'
forumTopicId: 18329
dashedName: uncomment-html
---

# --description--

Comentar é uma maneira de deixar comentários para outros desenvolvedores em seu código, sem afetar a saída resultante exibida para o usuário final.

Comentar também é uma maneira conveniente de tornar o código inativo sem ter que excluí-lo completamente.

Os comentários em HTML começam com `<!--` e terminam com `-->`

# --instructions--

Descomente seus elementos `h1`, `h2` e `p`.

# --hints--

Seu elemento `h1` deve estar visível na página ao descomentá-lo.

```js
assert($('h1').length > 0);
```

Seu elemento `h2` deve estar visível na página ao descomentá-lo.

```js
assert($('h2').length > 0);
```

Seu elemento `p` deve estar visível na página ao descomentá-lo.

```js
assert($('p').length > 0);
```
Nenhuma tag de fechamento de comentário deve estar visível na página (ou seja , `-->`).

```js
assert(!$('*:contains("-->")')[1]);
```

# --seed--

## --seed-contents--

```html
<!--
<h1>Hello World</h1>

<h2>CatPhotoApp</h2>

<p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
-->
```

# --solutions--

```html
<h1>Hello World</h1>

<h2>CatPhotoApp</h2>

<p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
```
