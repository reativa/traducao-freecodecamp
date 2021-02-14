---
id: 587d78a7367417b2b2512ae1
title: Criar movimento usando animações CSS
challengeType: 0
videoUrl: 'https://scrimba.com/c/c7amZfW'
forumTopicId: 301051
dashedName: create-movement-using-css-animation
---

# --description--

Quando os elementos têm uma `position` especificada, como `fixed` ou `relative`, as propriedades de deslocamento CSS `right`, `left`, `top` e `bottom` podem ser usadas em regras de animação para criar movimento.

Conforme mostrado no exemplo abaixo, você pode deslocar o item para baixo e depois para cima definindo a propriedade `top` do keyframe `50%` para 50px, mas configurando-o para 0px para o primeiro (`0%`) e o último keyframe (`100%`).

```css
@keyframes rainbow {
  0% {
    background-color: blue;
    top: 0px;
  }
  50% {
    background-color: green;
    top: 50px;
  }
  100% {
    background-color: yellow;
    top: 0px;
  }
}
```

# --instructions--

Adicione um movimento horizontal à animação `div`. Usando a propriedade de deslocamento `left`, adicione à `@keyframes`, para que o arco-íris comece em 0 pixels em `0%`, se mova para 25 pixels em `50%` e termine em -25 pixels em `100%`. Não substitua a propriedade `top` no editor - A animação deve ter movimento vertical e horizontal.

# --hints--

A `@keyframes` `0%` deve usar o deslocamento `left` de 0px.

```js
assert(code.match(/[^50]0%\s*?{[\s\S]*?left:\s*?0px(;[\s\S]*?|\s*?)}/gi));
```

A `@keyframes` `50%` deve usar o deslocamento `left` de 25px.

```js
assert(code.match(/50%\s*?{[\s\S]*?left:\s*?25px(;[\s\S]*?|\s*?)}/gi));
```

A `@keyframes` `100%` deve usar o deslocamento `esquerda` de -25px.

```js
assert(code.match(/100%\s*?{[\s\S]*?left:\s*?-25px(;[\s\S]*?|\s*?)}/gi));
```

# --seed--

## --seed-contents--

```html
<style>
  div {
    height: 40px;
    width: 70%;
    background: black;
    margin: 50px auto;
    border-radius: 5px;
    position: relative;
  }

  #rect {
    animation-name: rainbow;
    animation-duration: 4s;
  }

  @keyframes rainbow {
    0% {
      background-color: blue;
      top: 0px;

    }
    50% {
      background-color: green;
      top: 50px;

    }
    100% {
      background-color: yellow;
      top: 0px;

    }
  }
</style>

<div id="rect"></div>
```

# --solutions--

```html
<style>
  div {
    height: 40px;
    width: 70%;
    background: black;
    margin: 50px auto;
    border-radius: 5px;
    position: relative;
  }

  #rect {
    animation-name: rainbow;
    animation-duration: 4s;
  }

  @keyframes rainbow {
    0% {
      background-color: blue;
      top: 0px;
      left: 0px;
    }
    50% {
      background-color: green;
      top: 50px;
      left: 25px;
    }
    100% {
      background-color: yellow;
      top: 0px;
      left: -25px;
    }
  }
</style>
<div id="rect"></div>
```
