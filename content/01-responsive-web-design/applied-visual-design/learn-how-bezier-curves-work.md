---
id: 587d78a9367417b2b2512ae8
title: Aprenda como as Bezier curves funcionam
challengeType: 0
videoUrl: 'https://scrimba.com/c/c9bDrs8'
forumTopicId: 301058
dashedName: learn-how-bezier-curves-work
---

# --description--

O último desafio introduziu a propriedade `animation-timing-function` e algumas palavras-chave que mudam a velocidade de uma animação ao longo de sua duração. CSS oferece uma opção diferente de palavras-chave que fornece um controle ainda mais preciso sobre como a animação que é reproduzida, por meio do uso de curvas de Bezier (Bezier Curves).

Em animações CSS, as curvas de Bezier são usadas com a função `cubic-bezier`. A forma da curva representa como a animação é reproduzida. A curva vive em um sistema de coordenadas 1 por 1. O eixo X deste sistema de coordenadas é a duração da animação (pense nisso como uma escala de tempo), e o eixo Y é a mudança na animação.

A função `cubic-bezier` consiste em quatro pontos principais que ficam nesta grade 1 por 1: `p0`, `p1`, `p2` e `p3`. `p0` e `p3` são configurados para você - eles são os pontos inicial e final que estão sempre localizados respectivamente na origem (0, 0) e (1, 1). Você define os valores x e y para os outros dois pontos e onde colocá-los na grade e determina a forma da curva a ser seguida pela animação. Isso é feito em CSS declarando os valores x e y dos pontos de "âncora" `p1` e `p2` na forma: `(x1, y1, x2, y2)`. Juntando tudo, aqui está um exemplo de uma curva de Bezier no código CSS:

`animation-timing-function: cubic-bezier(0.25, 0.25, 0.75, 0.75);`

No exemplo acima, os valores x e y são equivalentes para cada ponto (x1 = 0,25 = y1 e x2 = 0,75 = y2), se você se lembrar da aula de geometria, resulta em uma linha que se estende da origem ao ponto (1, 1). Esta animação é uma mudança linear de um elemento durante a duração de uma animação que é o mesmo que usar a palavra-chave `linear`. Em outras palavras, ele muda a uma velocidade constante.

# --instructions--

Para o elemento com o id de `ball1`, altere o valor da propriedade `animation-timing-function` de `linear` para o valor da função `cubic-bezier` equivalente. Use os valores dos pontos fornecidos no exemplo acima.

# --hints--

O valor da propriedade `animation-timing-function` para o elemento com o id `ball1` deve ser a função de cubic-bezier linear equivalente.

```js
assert(
  $('#ball1').css('animation-timing-function') ==
    'cubic-bezier(0.25, 0.25, 0.75, 0.75)'
);
```

O valor da propriedade `animation-timing-function` para o elemento com o id `ball2` não deve mudar.

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

  .balls{
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
    left: 27%;
    animation-timing-function: linear;
  }
  #ball2 {
    left: 56%;
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

# --solutions--

```html
<style>

  .balls{
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
    left: 27%;
    animation-timing-function: cubic-bezier(0.25, 0.25, 0.75, 0.75);
  }
  #ball2 {
    left: 56%;
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
