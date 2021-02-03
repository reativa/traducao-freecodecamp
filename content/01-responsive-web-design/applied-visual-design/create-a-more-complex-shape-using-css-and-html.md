---
id: 587d78a6367417b2b2512ade
title: Create a More Complex Shape Using CSS and HTML
challengeType: 0
videoUrl: 'https://scrimba.com/c/cPpz4fr'
forumTopicId: 301050
dashedName: create-a-more-complex-shape-using-css-and-html
---

# --description--

Uma das formas mais populares do mundo é a forma de coração e, neste desafio, você criará um usando CSS puro. Mas primeiro, você precisa entender os pseudo-elementos `:: before` e `:: after`. Esses pseudo-elementos são usados para adicionar algo antes ou depois de um elemento selecionado. No exemplo a seguir, um pseudo-elemento `:: before` é usado para adicionar um retângulo a um elemento com a classe `heart`:

```css
.heart::before {
  content: "";
  background-color: yellow;
  border-radius: 25%;
  position: absolute;
  height: 50px;
  width: 70px;
  top: -50px;
  left: 5px;
}
```

Para os pseudo-elementos `:: before` e `:: after` funcionarem corretamente, eles devem ter uma propriedade `content` definida. Esta propriedade geralmente é usada para adicionar coisas como uma foto ou texto ao elemento selecionado. Quando os pseudo-elementos `:: before` e `:: after` são usados para fazer formas, a propriedade `content` ainda é necessária, mas é definida como uma string vazia. No exemplo acima, o elemento com a classe `heart` tem um pseudo-elemento `:: before` que produz um retângulo amarelo com `height` e `width` de 50px e 70px, respectivamente. Este retângulo tem cantos arredondados devido ao seu `border-radius` de 25% e está posicionado absolutamente à 5 px da `esquerda` e 50 px acima do `topo` do elemento.
# --instructions--

Transforme o elemento da tela em um coração. No seletor `heart :: after`, mude `background-color` para pink e `border-radius` para 50%.

Em seguida, direcione o elemento com a classe `heart` (apenas `heart`) e preencha a propriedade `transform`. Use a função `rotate ()` com -45 graus.

Finalmente, no seletor `heart :: before`, defina sua propriedade `content` para uma string vazia.

# --hints--

A propriedade `background-color` do seletor `heart :: after` deve ser rosa.

```js
const heartAfter = code.match(/\.heart::after\s*{[\s\S]+?[^\}]}/g)[0];
assert(
  /({|;)\s*background-color\s*:\s*pink\s*(;|})/g.test(heartAfter)
);
```

O `border-radius` do seletor `heart :: after` deve ser 50%.

```js
assert(code.match(/border-radius\s*?:\s*?50%/gi).length == 2);
```

A propriedade `transform` para a classe `heart` deve usar uma função `rotate ()` definida para -45 graus.

```js
assert(code.match(/transform\s*?:\s*?rotate\(\s*?-45deg\s*?\)/gi));
```

O `content` do seletor `heart :: before` deve ser uma string vazia.
```js
assert(code.match(/\.heart::before\s*?{\s*?content\s*?:\s*?("|')\1\s*?;/gi));
```

# --seed--

## --seed-contents--

```html
<style>
  .heart {
    position: absolute;
    margin: auto;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-color: pink;
    height: 50px;
    width: 50px;
    transform: ;
  }
  .heart::after {
    background-color: blue;
    content: "";
    border-radius: 25%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: 0px;
    left: 25px;
  }
  .heart::before {
    content: ;
    background-color: pink;
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: -25px;
    left: 0px;
  }
</style>
<div class="heart"></div>
```

# --solutions--

```html
<style>
  .heart {
    position: absolute;
    margin: auto;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-color: pink;
    height: 50px;
    width: 50px;
    transform: rotate(-45deg);
  }
  .heart::after {
    background-color: pink;
    content: "";
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: 0px;
    left: 25px;
  }
  .heart::before {
    content: "";
    background-color: pink;
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: -25px;
    left: 0px;
  }
</style>
<div class="heart"></div>
```
