---
id: 587d781e367417b2b2512ac9
title: Mude a posição relativa de um elemento
challengeType: 0
videoUrl: 'https://scrimba.com/c/czVmMtZ'
forumTopicId: 301044
dashedName: change-an-elements-relative-position
---

# --description--

O CSS trata cada elemento do HTML com sua própria 'box' (caixa), o que é normalmente conhecido como <dfn>CSS Box Model</dfn>. Os elementos 'Block-level' começam automaticamente em uma nova linha (por exemplo: títulos (h1,h2,...), paragrafos (p), e as 'divs') enquanto os elementos inline se encaixam conforme os elementos a sua volta (como imagens ou 'spans'). O layout padrão dos elementos é chamado de o <dfn>'normal flow'</dfn> de um documento, mas o CSS oferece a propriedade 'position' para sobrescrever isso.

Quando a 'position' de um elemento é `relative`, isso te permite especificar como o CSS deve mover o elemento *relativamento* a sua posição atual no 'normal flow' da página. Isso se une as propriedades: `left`(esquerda) ou `right`(direita), e `top`(cima) ou `bottom`(baixo). Essas propriedades ditam quantos pixels, porcentagem, ou 'ems' mover *para longe* de onde esta normalmente posicionado. O exemplo a seguir move o paragrafor 10 pixels para longe da parte de baixo (bottom):

```css
p {
  position: relative;
  bottom: 10px;
}
```

Mudar a posição relativa de um elemento não remove ele do 'normal flow' - os outros elementos a sua volta ainda se comportam como se o item estivesse na sua posição original. **Nota:** O método 'position' traz uma grande flexibilidade e poder sobre o visual do layout. É bom lembrar que não importa a posição do elemento, o 'HTML' deve estar organizado e fazer sentido quando lido de cima para baixo. É dessa forma que pessoas com dificuldades visuais (que necessitam da assistência de aparelhos como leitores de tela) irão acessar essa página.

# --instructions--

Mude o `position` do `h2` para `relative`, e use o CSS para mover 15 pixels para longe do `top` onde ele está no normal flow. Note que não há nenhum impacto na posição dos elementos h1 e p.

# --hints--

O elemento `h2` tem que estar com o `position` como `relative`.

```js
assert($('h2').css('position') == 'relative');
```

Seu código deve usar o CSS para mover relativamente a posição do `h2` 15px para longe do `top` de onde ele normalmente estaria.

```js
assert($('h2').css('top') == '15px');
```

# --seed--

## --seed-contents--

```html
<style>
  h2 {


  }
</style>
<body>
  <h1>On Being Well-Positioned</h1>
  <h2>Move me!</h2>
  <p>I still think the h2 is where it normally sits.</p>
</body>
```

# --solutions--

```html
<style>
  h2 {
    position: relative;
    top: 15px;
  }
</style>
<body>
  <h1>On Being Well-Positioned</h1>
  <h2>Move me!</h2>
  <p>I still think the h2 is where it normally sits.</p>
</body>
```
