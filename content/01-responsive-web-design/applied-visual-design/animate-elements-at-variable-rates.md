---
id: 587d78a8367417b2b2512ae5
title: Animate Elements at Variable Rates
challengeType: 0
videoUrl: 'https://scrimba.com/c/cZ89WA4'
forumTopicId: 301040
dashedName: animate-elements-at-variable-rates
---

# --description--

Existem várias maneiras de alterar as ritmos de animação similarmente a elementos animados. Até agora, isso foi conseguido aplicando uma propriedade `animation-iteration-count` e definindo regras `@ keyframes`.

Para ilustrar, a animação à direita consiste em duas "estrelas" que diminuem em tamanho e opacidade na marca de 20% utilizando a regra `@ keyframes`, que cria a animação cintilante. Você pode alterar a regra do `@ keyframes` para um dos elementos, para que as estrelas cintilem em ritmos diferentes.

# --instructions--

Altere o ritmo de animação para o elemento com o nome de classe `star-1` alterando sua regra de `@ keyframes` para 50%.

# --hints--

A regra `@ keyframes` para a classe `star-1` deve ser de 50%.
```js
assert(code.match(/twinkle-1\s*?{\s*?50%/g));
```

# --seed--

## --seed-contents--

```html
<style>
  .stars {
    background-color: white;
    height: 30px;
    width: 30px;
    border-radius: 50%;
    animation-iteration-count: infinite;
  }

  .star-1 {
    margin-top: 15%;
    margin-left: 60%;
    animation-name: twinkle-1;
    animation-duration: 1s;
  }

  .star-2 {
    margin-top: 25%;
    margin-left: 25%;
    animation-name: twinkle-2;
    animation-duration: 1s;
  }

  @keyframes twinkle-1 {
    20% {
      transform: scale(0.5);
      opacity: 0.5;
    }
  }

  @keyframes twinkle-2 {
    20% {
      transform: scale(0.5);
      opacity: 0.5;
    }
  }

  #back {
    position: fixed;
    padding: 0;
    margin: 0;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(black, #000099, #66c2ff, #ffcccc, #ffeee6);
  }
</style>

<div id="back"></div>
<div class="star-1 stars"></div>
<div class="star-2 stars"></div>
```

# --solutions--

```html
<style>
  .stars {
    background-color: white;
    height: 30px;
    width: 30px;
    border-radius: 50%;
    animation-iteration-count: infinite;
  }

  .star-1 {
    margin-top: 15%;
    margin-left: 60%;
    animation-name: twinkle-1;
    animation-duration: 1s;
  }

  .star-2 {
    margin-top: 25%;
    margin-left: 25%;
    animation-name: twinkle-2;
    animation-duration: 1s;
  }

  @keyframes twinkle-1 {
    50% {
      transform: scale(0.5);
      opacity: 0.5;
    }
  }

  @keyframes twinkle-2 {
    20% {
      transform: scale(0.5);
      opacity: 0.5;
    }
  }

  #back {
    position: fixed;
    padding: 0;
    margin: 0;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(black, #000099, #66c2ff, #ffcccc, #ffeee6);
  }
</style>
<div id="back"></div>
<div class="star-1 stars"></div>
<div class="star-2 stars"></div>
```
