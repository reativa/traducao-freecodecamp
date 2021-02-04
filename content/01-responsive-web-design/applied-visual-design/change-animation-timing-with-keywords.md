---
id: 587d78a8367417b2b2512ae7
title: Alterar o tempo da animação com palavras-chave
challengeType: 0
videoUrl: 'https://scrimba.com/c/cJKvwCM'
forumTopicId: 301045
dashedName: change-animation-timing-with-keywords
---

# --description--

Em animações no CSS, a propriedade `animation-timing-function` controla a rapidez com que um elemento animado muda ao longo da duração da animação. Se a animação é um carro se movendo do ponto A para o ponto B em um determinado tempo (sua `animation-duration`), a `animation-timing-function` diz como o carro acelera e desacelera ao longo do percurso.

Existem várias palavras-chave predefinidas disponíveis para opções populares. Por exemplo, o valor padrão é `ease`, que começa devagar, acelera no meio e depois desacelera novamente no final. Outras opções incluem `ease-out`, que é rápido no início e depois desacelera, `ease-in`, que é lento no início e acelera no final, ou `linear`, que aplica uma velocidade de animação constante.

# --instructions--

Para os elementos com id de `ball1` e `ball2`, adicione uma propriedade `animation-timing-function` para cada um e defina `# ball1` para `linear` e `# ball2` para `eas-out`. Observe a diferença como os elementos se movem durante a animação, mas terminam juntos, pois eles compartilham a mesma `animation-duration` de 2 segundos.

# --hints--

O valor da propriedade `animation-timing-function` para o elemento com o id `ball1` deve ser linear.

```js
const ball1Animation = __helpers.removeWhiteSpace(
  $('#ball1').css('animation-timing-function')
);
assert(ball1Animation == 'linear' || ball1Animation == 'cubic-bezier(0,0,1,1)');
```

O valor da propriedade `animation-timing-function` para o elemento com o id `ball2` deve ser ease-out.

```js
const ball2Animation = __helpers.removeWhiteSpace(
  $('#ball2').css('animation-timing-function')
);
assert(
  ball2Animation == 'ease-out' || ball2Animation == 'cubic-bezier(0,0,0.58,1)'
);
```

# --seed--

## --seed-contents--

```html
<style>

  .balls {
    border-radius: 50%;
    background: linear-gradient(
      35deg,
      #ccffff,
      #ffcccc
    );
    position: fixed;
    width: 50px;
    height: 50px;
    margin-top: 50px;
    animation-name: bounce;
    animation-duration: 2s;
    animation-iteration-count: infinite;
  }
  #ball1 {
    left:27%;

  }
  #ball2 {
    left:56%;

  }

  @keyframes bounce {
    0% {
      top: 0px;
    }
    100% {
      top: 249px;
    }
  }

</style>

<div class="balls" id="ball1"></div>
<div class="balls" id="ball2"></div>
```

# --solutions--

```html
<style>
  .balls {
    border-radius: 50%;
    background: linear-gradient(
      35deg,
      #ccffff,
      #ffcccc
    );
    position: fixed;
    width: 50px;
    height: 50px;
    margin-top: 50px;
    animation-name: bounce;
    animation-duration: 2s;
    animation-iteration-count: infinite;
  }
  #ball1 {
    left:27%;
    animation-timing-function: linear;
  }
  #ball2 {
    left:56%;
    animation-timing-function: ease-out;
  }

  @keyframes bounce {
    0% {
      top: 0px;
    }
    100% {
      top: 249px;
    }
  }
</style>
<div class="balls" id="ball1"></div>
<div class="balls" id="ball2"></div>
```
