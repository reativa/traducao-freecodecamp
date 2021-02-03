---
id: 587d78a7367417b2b2512ae1
title: Create Movement Using CSS Animation
challengeType: 0
videoUrl: 'https://scrimba.com/c/c7amZfW'
forumTopicId: 301051
dashedName: create-movement-using-css-animation
---

# --description--

Quando os elementos têm uma `position` especificada, como `fixed` ou `relative`, as propriedades de deslocamento CSS `right`, `left`, `top` e `bottom` podem ser usadas em regras de animação para criar movimento.

Como mostrado no exemplo abaixo, é possível empurrar o produto para baixo, em seguida, para cima, definindo a propriedade `top` do keyframe de `50% ` para 50 pixels, mas definindo a 0px para o primeiro (`0%`) e o úlitmo(`100%`) keyframe .

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

Adicione um movimento horizontal à animação da `div`. Usando a propriedade de deslocamento `left`, adicione à regra `@ keyframes` para que o arco-íris comece em 0 pixels no ponto de `0%`, se mova para 25 pixels no ponto de `50%` e termine em -25 pixels em `100%`. Não substitua a propriedade `top` no editor - a animação deve ter movimento vertical e horizontal.

# --hints--

A regra `@ keyframes` para `0% ` deve usar o deslocamento `left` de 0px.
```js
assert(code.match(/[^50]0%\s*?{[\s\S]*?left:\s*?0px(;[\s\S]*?|\s*?)}/gi));
```

A regra `@ keyframes` para `50% ` deve usar o deslocamento `left` de 25px.

```js
assert(code.match(/50%\s*?{[\s\S]*?left:\s*?25px(;[\s\S]*?|\s*?)}/gi));
```

A regra `@ keyframes` para `100% ` deve usar o deslocamento `left` de -25px.

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
