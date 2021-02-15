---
id: 587d78a3367417b2b2512ad1
title: Aprenda sobre Cores Complementares
challengeType: 0
videoUrl: 'https://scrimba.com/c/c2MD3Tr'
forumTopicId: 301056
dashedName: learn-about-complementary-colors
---

# --description--

A teoria das cores e seu impacto no design é um tópico profundo e apenas o básico é abordado nos desafios a seguir. Em um site, a cor pode chamar a atenção para o conteúdo, evocar emoções ou criar harmonia visual. Usar diferentes combinações de cores pode realmente mudar a aparência de um site, e muito pensamento pode ser necessário para escolher uma paleta de cores que funcione com o seu conteúdo.

A roda de cores (ou mais conhecido como circulo cromático) é uma ferramenta útil para visualizar como as cores se relacionam umas com as outras - é um círculo onde as tonalidades semelhantes são vizinhas e tonalidades diferentes estão mais distantes. Quando duas cores estão opostas na roda, são chamadas de cores complementares. Elas têm a característica de que, se combinadas, "cancelam" um a outra e criam uma cor cinza. No entanto, quando colocadas lado a lado, essas cores parecem mais vibrantes e produzem um forte contraste visual.

Alguns exemplos de cores complementares, com seus códigos hexadecimais:

<blockquote>vermelho (#FF0000) e ciano (#00FFFF)<br>verde (#00FF00) e magenta (#FF00FF)<br>azul (#0000FF) e amarelo (#FFFF00)</blockquote>

Isso é diferente do modelo de cores RYB desatualizado que muitos de nós aprendemos na escola, que tem cores primárias e complementares diferentes. A teoria da cor moderna usa o modelo RGB aditivo (como na tela de um computador) e o modelo CMY(K) subtrativo (como na impressão). Leia [aqui](https://en.wikipedia.org/wiki/Color_model) para obter mais informações sobre este assunto complexo.

Existem muitas ferramentas de seleção de cores disponíveis online que oferecem a opção de encontrar o complemento de uma cor.

**Nota:** Para todos os desafios de cores: usar cores pode ser uma maneira poderosa de adicionar interesse visual a uma página. No entanto, a cor sozinha não deve ser usada como a única forma de transmitir informações importantes, porque os usuários com deficiência visual podem não entender esse conteúdo. Esse problema será abordado com mais detalhes nos desafios de acessibilidade aplicada.

# --instructions--

Altere a propriedade `background-color` das classes `blue` e `yellow` para suas respectivas cores. Observe como as cores parecem diferentes umas das outras em comparação com o fundo branco.

# --hints--

O elemento `div` com a classe `blue` deve ter um `background-color` azul.

```js
assert($('.blue').css('background-color') == 'rgb(0, 0, 255)');
```

O elemento `div` com a classe `yellow` deve ter um `background-color` amarela.

```js
assert($('.yellow').css('background-color') == 'rgb(255, 255, 0)');
```

# --seed--

## --seed-contents--

```html
<style>
  body {
    background-color: #FFFFFF;
  }
  .blue {
    background-color: #000000;
  }
  .yellow {
    background-color: #000000;
  }
  div {
    display: inline-block;
    height: 100px;
    width: 100px;
  }
</style>
<div class="blue"></div>
<div class="yellow"></div>
```

# --solutions--

```html
<style>
  body {
    background-color: #FFFFFF;
  }
  .blue {
    background-color: blue;
  }
  .yellow {
    background-color: yellow;
  }
  div {
    display: inline-block;
    height: 100px;
    width: 100px;
  }
</style>
<div class="blue"></div>
<div class="yellow"></div>
```
