---
id: 587d78a6367417b2b2512add
title: Crie um gráfico usando CSS
challengeType: 0
videoUrl: 'https://scrimba.com/c/cEDWPs6'
forumTopicId: 301048
dashedName: create-a-graphic-using-css
---

# --description--

Manipulando diferentes seletores e propriedades, você pode fazer formas interessantes. Uma das formas mais fáceis é uma lua crescente. Para esse desafio você precisará usar a propriedade `box-shadow` que cria a sombra de um elemento, juntamente com a propriedade `border-radius` que controla a circularidade das extremidades dos cantos de um elemento.

Você irá criar um objeto redondo, transparente com uma sombra sólida que esta levemente movida para o lado - você verá que a sombra vai ser a forma da lua.

Para criar um objeto redondo, a propriedade `border-radius` deve ter o valor de 50%.

Você deve lembrar que a propriedade `box-shadow` tem os seguintes valores respectivamente: `offset-x`, `offset-y`, `blur-radius`, `spread-radius` e o valor da cor. A propriedades `blur-radius` e `spread-radius` são opcionais.

# --instructions--

Manipule a forma quadrada no editor para criar a forma da lua. Primeiro, mude o `background-color` para 'transparent', então coloque o valor de 50% no `border-radius` para fazer uma forma circular. Por fim, mude os valores da propriedade `box-shadow` para `offset-x`: 25px, `offset-y`: 10px, `blur-radius`: 0, `spread-radius`: 0, e 'color': blue.

# --hints--

O valor do `background-color` deve ser `transparent`.

```js
assert(code.match(/background-color:\s*?transparent;/gi));
```

O valor do `border-radius` deve ser `50%`.

```js
assert(code.match(/border-radius:\s*?50%;/gi));
```

O valor do `box-shadow` deve ser 25px para `offset-x`, 10px para `offset-y`, 0 para `blur-radius`, 0 para `spread-radius`, e finalmente 'blue' para 'color'.

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
