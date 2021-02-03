---
id: 587d78b1367417b2b2512b0a
title: Use a Retina Image for Higher Resolution Displays
challengeType: 0
videoUrl: 'https://scrimba.com/p/pzrPu4/cVZ4Rfp'
forumTopicId: 301142
dashedName: use-a-retina-image-for-higher-resolution-displays
---

# --description--

Com o aumento dos dispositivos que se conectam a internet, seus tamanhos e especificação variam, e os displays que eles usam podem ser diferentes externa e internamente. A densidade de pixels é um aspecto que pode diferenciar um dispositivo de outros e esta densidade é conhecida como Pixel Por Polegada (PPI) ou Pontos por Polegada (DPI). O mais famoso desses displays é conhecido como "Tela Retina" (Retina Display) nos últimos MacBook Pro da Apple, e recentemente nos computadores iMac. Devido as diferenças na densidade de pixels entre displays "Retina" e os "Não-Retina", algumas imagens que não foram criadas pensando-se nos displays de alta resolução podem parecer "pixeladas" quando renderizadas em displays de alta resolução.

O jeito mais simples de fazer nossas imagens aparecerem de maneira apropriada em displays de alta resolução, tais como os display "Tela Retina" dos MacBook Pro é definir os valores de `width` e `height`somente na metade do indicado no arquivo original. Aqui está um exemplo de uma imagem que utiliza somente metade da largura e altura originais:

```html
<style>
  img { height: 250px; width: 250px; }
</style>
<img src="coolPic500x500" alt="A most excellent picture">
```

# --instructions--

Coloque a `width` e `height` da `img` com metade dos valores originais. Neste caso, tanto o `height`quanto o `width` são de `200px`.

# --hints--

Sua `img` deve ter `width` de 100 pixels.

```js
assert(document.querySelector('img').width === 100);
```

Sua `img` deve ter `height` de 100 pixels.

```js
assert(document.querySelector('img').height === 100);
```

# --seed--

## --seed-contents--

```html
<style>

</style>

<img src="https://s3.amazonaws.com/freecodecamp/FCCStickers-CamperBot200x200.jpg" alt="freeCodeCamp sticker that says 'Because CamperBot Cares'">
```

# --solutions--

```html
<style>
  img { 
    height: 100px; 
    width: 100px; 
  }
</style>

<img src="https://s3.amazonaws.com/freecodecamp/FCCStickers-CamperBot200x200.jpg" alt="freeCodeCamp sticker that says 'Because CamperBot Cares'">
```
