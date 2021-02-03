---
id: 587d78a5367417b2b2512ad8
title: Create Texture by Adding a Subtle Pattern as a Background Image
challengeType: 0
videoUrl: 'https://scrimba.com/c/cQdwJC8'
forumTopicId: 301052
dashedName: create-texture-by-adding-a-subtle-pattern-as-a-background-image
---

# --description--

Uma forma de adicionar textura e destaque para um *background*, e fazê-lo se destacar mais, é adicionando um padrão sutil. O segredo é o equilíbrio, pois você não quer que o fundo se destaque muito e se distancie do primeiro plano. A propriedade `background` suporta a função  `url()` para vincular uma imagem de textura ou de algum outro padrão escolhido. O endereço do link é colocado entre aspas entre parênteses. 

# --instructions--

Usando a url : `https://cdn-media-1.freecodecamp.org /imgr/ MJAkxbh.png`, defina o `background` da página interia com o seletor `body`.

# --hints--

Seu elemento `body` deve ter uma propriedade `background` definido com a `url()` do link fornecido.

```js
assert(
  code.match(
    /background:\s*?url\(\s*("|'|)https:\/\/cdn-media-1\.freecodecamp\.org\/imgr\/MJAkxbh\.png\1\s*\)/gi
  )
);
```

# --seed--

## --seed-contents--

```html
<style>
  body {

  }
</style>
```

# --solutions--

```html
<style>
  body {
    background: url("https://cdn-media-1.freecodecamp.org/imgr/MJAkxbh.png");
  }
</style>
```
