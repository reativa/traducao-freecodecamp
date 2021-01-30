---
id: 587d78b1367417b2b2512b09
title: Make an Image Responsive
challengeType: 0
videoUrl: 'https://scrimba.com/p/pzrPu4/cz763UD'
forumTopicId: 301140
dashedName: make-an-image-responsive
---

# --description--

Tornar imagens responsivas com CSS é na verdade muito simples. Você simplesmente precisa adicionar estas propriedades a imagem:

```css
img {
  max-width: 100%;
  height: auto;
}
```

A `max-width` de `100%` dará certeza absoluta que a imagem nunca será maior que o container que a abriga, e a `height` de `auto`fará a imagem manter a proporção original. 

# --instructions--


Adicione as regras de estilização a classe `responsive-img` para tornar a imagem responsiva. Nunca deve ser maior que o container (neste caso, a janela anteiror) e deve manter a proporção original. Após adicionar este código, redimensione a visualização para ver como a imagem se comporta.

# --hints--

Sua classe `responsive-img` deve ter a `max-width` setada em `100%`.

```js
assert(getComputedStyle($('.responsive-img')[0]).maxWidth === '100%');
```

Sua classe `responsive-img` deve ter a`height` setada em `auto`.

```js
assert(code.match(/height:\s*?auto;/g));
```

# --seed--

## --seed-contents--

```html
<style>
.responsive-img {


}

img {
  width: 600px;
}
</style>

<img class="responsive-img" src="https://s3.amazonaws.com/freecodecamp/FCCStickerPack.jpg" alt="freeCodeCamp stickers set">
<img src="https://s3.amazonaws.com/freecodecamp/FCCStickerPack.jpg" alt="freeCodeCamp stickers set">
```

# --solutions--

```html
<style>
.responsive-img {
  max-width: 100%;
  height: auto;
}

img {
  width: 600px;
}
</style>

<img class="responsive-img" src="https://s3.amazonaws.com/freecodecamp/FCCStickerPack.jpg" alt="freeCodeCamp stickers set">
<img src="https://s3.amazonaws.com/freecodecamp/FCCStickerPack.jpg" alt="freeCodeCamp stickers set">
```
