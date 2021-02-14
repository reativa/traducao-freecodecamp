---
id: 587d78a5367417b2b2512ad8
title: Criar textura adicionando um padrão como imagem de fundo
challengeType: 0
videoUrl: 'https://scrimba.com/c/cQdwJC8'
forumTopicId: 301052
dashedName: create-texture-by-adding-a-subtle-pattern-as-a-background-image
---

# --description--

Uma forma de adicionar textura e um plano de fundo interessante e fazê-lo se destacar mais é adicionar um padrão. O segredo é o equilíbrio, pois você não quer que o fundo se destaque muito e se distancie do primeiro plano. A propriedade `background` suporta a função `url()` para vincular a uma imagem da textura ou padrão escolhido. O endereço do link é colocado entre aspas dentro de parênteses.

# --instructions--

Usando o url `https://cdn-media-1.freecodecamp.org/imgr/MJAkxbh.png`, coloque o `background` em toda a página com o seletor `body`.

# --hints--

Seu elemento `body` deve ter um `background` definido com a `url()` do link fornecido.

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
