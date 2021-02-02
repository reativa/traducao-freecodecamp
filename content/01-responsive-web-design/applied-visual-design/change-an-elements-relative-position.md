---
id: 587d781e367417b2b2512ac9
title: Change an Element's Relative Position
challengeType: 0
videoUrl: 'https://scrimba.com/c/czVmMtZ'
forumTopicId: 301044
dashedName: change-an-elements-relative-position
---

# --description--

CSS trata cada elemento HTML como sua própria caixa, a qual é normalmente referenciada como <dfn>CSS Box Model</dfn>. Itens de nível de bloco automaticamente começam em uma nova linha (pense em cabeçalhos, parágrafos e divs) enquanto itens em linha se inserem em conteúdos que o circundam (como imagens ou spans). O layout padrão dos elementos neste formato é chamado de <dfn>normal flow</dfn> de um documento, mas o CSS oferece a propriedade posição para substituí-lo.

Quando a posição de um elemento é ajustada para `relative`, isto permite a você especificar como o CSS deve movê-lo * em relação * à sua posição atual no fluxo normal da página. 
Esta propriedade combina com as propriedades de deslocamento do CSS, `left` ou `right`, e `top` ou `bottom`. Estas propriedades dizem quantos pixels, porcentagens, ou ems o item se move para *longe* de onde ela é normalmente posicionada. O exemplo a seguir move o parágrafo 10 pixels para longe da parte inferior:

```css
p {
  position: relative;
  bottom: 10px;
}
```
Mudar a posição do elemento para relativo não o remove para o fluxo normal - outros elementos ao redor ainda se comportam como se aquele item estivesse na posição padrão.
 **Note:** O posicionamento permite a você uma maior flexbilidade e poder sobre o layout de uma página. É bom lembrar que não importa a posição dos elementos, a marcação HTML deve ser organizada e fazer sentido quando lida de cima para baixo. Isto é como os usuários com necessidades visuais (que dependem de dispositivos assistivos como leitores de tela) acessam o seu conteúdo.
 
# --instructions--

Mude a `position` do `h2` para `relative`, e use o deslocamento CSS para movê-lo 15 pixels para longe do `top` de onde ele se encontra no fluxo normal. Note que não isso não terá impacto nas posições dos elementos h1 e p que estão ao redor.

# --hints--

O elemento `h2` deve ter uma propriedade `position` ajustada para `relative`.

```js
assert($('h2').css('position') == 'relative');
```
Seu código deve usar um deslocamento CSS para posicionar relativamente o `h2` 15px distante do` top` de onde ele normalmente fica.

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
