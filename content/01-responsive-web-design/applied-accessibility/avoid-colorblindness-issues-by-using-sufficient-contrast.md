---
id: 587d778f367417b2b2512aac
title: Avoid Colorblindness Issues by Using Sufficient Contrast
challengeType: 0
videoUrl: 'https://scrimba.com/c/cmzMEUw'
forumTopicId: 301012
dashedName: avoid-colorblindness-issues-by-using-sufficient-contrast
---

# --description--

A cor é uma grande parte do design visual, mas seu uso apresenta dois problemas de acessibilidade. Primeiro, a cor sozinha não deve ser usada como a única maneira de transmitir informações importantes, porque os usuários de leitores de tela não as verão. Em segundo lugar, as cores do primeiro plano e do plano de fundo precisam de contraste suficiente para que usuários daltônicos possam distingui-las.

Os desafios anteriores cobriram alternativas de texto para resolver o primeiro problema. O último desafio introduziu ferramentas de verificação de contraste para ajudar com o segundo. A taxa de contraste recomendada pela WCAG de 4,5: 1 se aplica tanto ao uso de cores quanto às combinações de tons de cinza.

Usuários daltônicos têm dificuldade em distinguir algumas cores de outras - geralmente em matiz, mas às vezes também em luminosidade. Você deve se lembrar que a taxa de contraste é calculada usando os valores de luminância (ou luminosidade) relativa das cores do primeiro plano e do plano de fundo.

Na prática, a taxa de contraste de 4,5: 1 pode ser alcançada sombreando (adicionando preto) à cor mais escura e matizando (adicionando branco) à cor mais clara. Tons mais escuros na roda de cores são considerados tons de azul, violetas, magentas e vermelhos, enquanto as cores mais claras são laranjas, amarelos, verdes e azuis-verdes.

# --instructions--

Camper Cat está experimentando usar cores para o texto e o plano de fundo de seu blog, mas sua combinação atual de um `background-color` esverdeado com uma `color` de texto marrom tem uma relação de contraste de 2,5: 1. Você pode ajustar facilmente a claridade das cores, já que ele as declarou usando a propriedade CSS `hsl ()` (que significa hue, saturation, lightness) alterando o terceiro argumento. Aumente o valor de claridade do `background-color` de 35% para 55% e diminua o valor de claridade da`color` de 20% para 15%. Isso melhora o contraste para 5,9: 1.

# --hints--

Seu código só deve alterar o valor de claridade da propriedade `color` do texto para um valor de 15%.
```js
assert(code.match(/color:\s*?hsl\(0,\s*?55%,\s*?15%\)/gi));
```

Seu código só deve alterar o valor de claridade da propriedade  `background-color` para um valor de 55%.

```js
assert(code.match(/background-color:\s*?hsl\(120,\s*?25%,\s*?55%\)/gi));
```

# --seed--

## --seed-contents--

```html
<head>
  <style>
  body {
    color: hsl(0, 55%, 20%);
    background-color: hsl(120, 25%, 35%);
  }
  </style>
</head>
<body>
  <header>
    <h1>Deep Thoughts with Master Camper Cat</h1>
  </header>
  <article>
    <h2>A Word on the Recent Catnip Doping Scandal</h2>
    <p>The influence that catnip has on feline behavior is well-documented, and its use as an herbal supplement in competitive ninja circles remains controversial. Once again, the debate to ban the substance is brought to the public's attention after the high-profile win of Kittytron, a long-time proponent and user of the green stuff, at the Claw of Fury tournament.</p>
    <p>As I've stated in the past, I firmly believe a true ninja's skills must come from within, with no external influences. My own catnip use shall continue as purely recreational.</p>
  </article>
</body>
```

# --solutions--

```html
<head>
  <style>
  body {
    color: hsl(0, 55%, 15%);
    background-color: hsl(120, 25%, 55%);
  }
  </style>
</head>
<body>
  <header>
    <h1>Deep Thoughts with Master Camper Cat</h1>
  </header>
  <article>
    <h2>A Word on the Recent Catnip Doping Scandal</h2>
    <p>The influence that catnip has on feline behavior is well-documented, and its use as an herbal supplement in competitive ninja circles remains controversial. Once again, the debate to ban the substance is brought to the public's attention after the high-profile win of Kittytron, a long-time proponent and user of the green stuff, at the Claw of Fury tournament.</p>
    <p>As I've stated in the past, I firmly believe a true ninja's skills must come from within, with no external influences. My own catnip use shall continue as purely recreational.</p>
  </article>
</body>
```
