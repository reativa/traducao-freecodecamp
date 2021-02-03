---
id: 587d781e367417b2b2512ac9
title: Mudar a posição relativa de um elemento
challengeType: 0
videoUrl: 'https://scrimba.com/c/czVmMtZ'
forumTopicId: 301044
dashedName: change-an-elements-relative-position
---

# --description--

CSS trata cada elemento HTML como sua própria caixa, que geralmente é conhecida como <dfn>CSS Box Model</dfn>. Os itens block-level começam automaticamente em uma nova linha (pense em títulos, parágrafos e divs), enquanto os itens inline ficam dentro do conteúdo circundante (como imagens ou extensões). O layout padrão dos elementos dessa forma é chamado de <dfn> fluxo normal </dfn> de um documento, mas o CSS oferece a propriedade chamada `position` para substituí-la.

Quando a `position` de um elemento é definida como `relative`, permite que você especifique como o CSS deve movê-lo *em relação* à sua posição atual no fluxo normal da página. Ele é pareado com as propriedades de deslocamento CSS `left` ou `right` e `top` ou `bottom`. Eles dizem quantos pixels, porcentagens ou ems o item deve ser movido *para longe* de onde ele está normalmente posicionado. O exemplo a seguir move o parágrafo 10 pixels para longe da parte inferior:

```css
p {
  position: relative;
  bottom: 10px;
}
```

Alterar a posição de um elemento para `relative` não o remove do fluxo normal - outros elementos ao redor dele ainda se comportam como se aquele item estivesse em sua posição padrão. **Observação:** O posicionamento oferece bastante flexibilidade e poder sobre o layout visual de uma página. É bom lembrar que não importa a posição dos elementos, a marcação HTML subjacente deve ser organizada e fazer sentido quando lida de cima para baixo. É assim que usuários com deficiência visual (que contam com dispositivos auxiliares como leitores de tela) acessam seu conteúdo.

# --instructions--

Mude a `position` da `h2` para `relative`, e use um deslocamento CSS para movê-lo 15 pixels longe do `top` de onde ele se encontra no fluxo normal. Observe que não há impacto nas posições dos elementos h1 e p circundantes.

# --hints--

O elemento `h2` deve ter uma propriedade `position` definida como `relative`.

```js
assert($('h2').css('position') == 'relative');
```

Seu código deve usar um deslocamento CSS para posicionar relativamente o `h2` 15px longe do `top` de onde ele normalmente fica.

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
