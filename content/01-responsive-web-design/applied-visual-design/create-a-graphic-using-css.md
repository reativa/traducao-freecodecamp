---
id: 587d78a6367417b2b2512add
title: Create a Graphic Using CSS
challengeType: 0
videoUrl: 'https://scrimba.com/c/cEDWPs6'
forumTopicId: 301048
dashedName: create-a-graphic-using-css
---

# --description--

Ao manipular diferentes seletores e propriedades, você pode criar formas interessantes. Uma das mais fáceis de experimentar é a forma de lua crescente. Para este desafio, você precisa trabalhar com a propriedade `box-shadow` que define a sombra de um elemento, junto com a propriedade `border-radius` que controla o arredondamento dos cantos do elemento.

Você criará um objeto redondo e transparente com uma sombra nítida ligeiramente deslocada para o lado - a sombra será na verdade a forma de lua que você vê.

Para criar um objeto redondo, a propriedade `border-radius` deve ser configurada para um valor de 50%.

Você deve se lembrar de um desafio anterior que a propriedade `box-shadow` assume valores para `offset-x`, `offset-y`,`blur-radius`, `spread-radius` e um valor de cor nessa ordem. Os valores `blur-radius` e `spread-radius` são opcionais.

# --instructions--

Manipule o elemento quadrado no editor para criar a forma da lua. Primeiro, altere o `background-color` para transparente e, em seguida, defina a propriedade `order-radius` como 50% para fazer a forma circular. Por fim, altere a propriedade `box-shadow` para definir `offset-x` para 25px, `offset-y` para 10px, `blur-radius` para 0, `spread-radius` para 0 e cor para azul .
# --hints--

O valor da propriedade `background-color` deve ser definido como `transparent`.
```js
assert(code.match(/background-color:\s*?transparent;/gi));
```

O valor da propriedade `border-radius` deve ser definido como `50% `.

```js
assert(code.match(/border-radius:\s*?50%;/gi));
```

O valor da propriedade `box-shadow` deve ser definido como 25px para `offset-x`, 10px para `offset-y`, 0 para `blur-radius`, 0 para `spread-radius` e finalmente azul para a cor.

```js
assert(
  code.match(/box-shadow:\s*?25px\s+?10px\s+?0(px)?\s+?0(px)?\s+?blue\s*?;/gi)
);
```

# --seed--

## --seed-contents--

```html
<style>
  .center {
    position: absolute;
    margin: auto;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    width: 100px;
    height: 100px;
    background-color: blue;
    border-radius: 0px;
    box-shadow: 25px 10px 10px 10px green;
  }

</style>
<div class="center"></div>
```

# --solutions--

```html
<style>
  .center {
    position: absolute;
    margin: auto;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    width: 100px;
    height: 100px;
    background-color: transparent;
    border-radius: 50%;
    box-shadow: 25px 10px 0 0 blue;
  }
</style>
<div class="center"></div>
```
