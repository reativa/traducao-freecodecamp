---
id: bad87fee1348bd9aedf08804
title: Comente HTML
challengeType: 0
videoUrl: 'https://scrimba.com/p/pVMPUv/cGyGbca'
forumTopicId: 16782
dashedName: comment-out-html
---

# --description--

Lembre-se que para iniciar um comentário, você precisa usar `<!--` e para terminar um comentário, você precisa usar `-->`

Aqui você precisará encerrar o comentário antes do seu elemento `h2` começar.

# --instructions--

Comente seu elemento `h1` e seu elemento `p`, mas não o seu elemento `h2`.

# --hints--

Seu elemento `h1` deve ser comentado para que não fique visível na página.

```js
assert($('h1').length === 0);
```


Seu elemento `h2` não deve ser comentado para que fique visível na página.

```js
assert($('h2').length > 0);
```

Seu elemento `p` deve ser comentado para que não fique visível na página.

```js
assert($('p').length === 0);
```

Cada um de seus comentários deve ser fechado com `-->`.

```js
assert(code.match(/[^fc]-->/g).length > 1);
```

Você não deve mudar a ordem do `h1` `h2` ou `p` no código.

```js
assert(
  code.match(/<([a-z0-9]){1,2}>/g)[0] === '<h1>' &&
    code.match(/<([a-z0-9]){1,2}>/g)[1] === '<h2>' &&
    code.match(/<([a-z0-9]){1,2}>/g)[2] === '<p>'
);
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
<!--<h1>Hello World</h1>-->
<h2>CatPhotoApp</h2> 
<!--<p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p> -->
```
