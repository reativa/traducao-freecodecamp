---
id: 587d78a4367417b2b2512ad2
title: Saiba mais sobre cores terciárias
challengeType: 0
forumTopicId: 301057
dashedName: learn-about-tertiary-colors
---

# --description--

Monitores de computador e telas de dispositivos criam cores diferentes combinando quantidades de luz vermelha, verde e azul. Isso é conhecido como modelo de cores aditivas RGB na teoria moderna das cores. Vermelho - Red (R), Verde - Green (G) e Azul - Blue (B) são chamados de cores primárias. A mistura de duas cores primárias cria as cores secundárias ciano (G + B), magenta (R + B) e amarelo (R + G). Você viu essas cores no desafio Cores Complementares. Essas cores secundárias são o complemento da cor primária não usada em sua criação e são opostas a essa cor primária no circulo cromático (roda das cores). Por exemplo, o magenta é feito com vermelho e azul e é complemento do verde.

As cores terciárias são o resultado da combinação de uma cor primária com uma de suas vizinhas de cor secundária. Por exemplo, dentro do modelo de cores RGB, vermelho (primário) e amarelo (secundário) tornam-se laranja (terciária). Isso adiciona mais seis cores a uma roda de cores simples para um total de doze.

Existem vários métodos de seleção de cores diferentes que resultam em uma combinação harmoniosa de design. Um exemplo que pode usar cores terciárias é chamado de esquema de harmonia complementar dividida. Este esquema começa com uma cor de base e a emparelha com as duas cores adjacentes ao seu complemento. As três cores fornecem forte contraste visual em um design, mas são mais sutis do que usar duas cores complementares.

Aqui estão três cores criadas usando o esquema de harmonia complementar dividida:

<table class='table table-striped'><thead><tr><th>Color</th><th>Hex Code</th></tr></thead><thead></thead><tbody><tr><td>laranja</td><td>#FF7F00</td></tr><tr><td>ciano</td><td>#00FFFF</td></tr><tr><td>framboesa</td><td>#FF007F</td></tr></tbody></table>

# --instructions--

Altere a propriedade `background-color` das classes `orange`, `cyan` e `raspberry` para suas respectivas cores. Certifique-se de usar os códigos hexadecimais e não os nomes das cores.

# --hints--

O elemento `div` com classe `orange` deve ter um `background-color` laranja.

```js
assert($('.orange').css('background-color') == 'rgb(255, 127, 0)');
```

O elemento `div` com a classe `cyan` deve ter um `background-color` de ciano.

```js
assert($('.cyan').css('background-color') == 'rgb(0, 255, 255)');
```

O elemento `div` com a classe `raspberry` deve ter um `background-color` de framboesa.

```js
assert($('.raspberry').css('background-color') == 'rgb(255, 0, 127)');
```

Todos os valores de `background-color` para as classes de cores devem ser códigos hexadecimais e não nomes de cores.

```js
assert(!/background-color:\s(orange|cyan|raspberry)/.test(code));
```

# --seed--

## --seed-contents--

```html
<style>
  body {
    background-color: #FFFFFF;
  }

  .orange {
    background-color: #000000;
  }

  .cyan {
    background-color: #000000;
  }

  .raspberry {
    background-color: #000000;
  }

  div {
    height: 100px;
    width: 100px;
    margin-bottom: 5px;
  }
</style>

<div class="orange"></div>
<div class="cyan"></div>
<div class="raspberry"></div>
```

# --solutions--

```html
<style>
  body {
    background-color: #FFFFFF;
  }

  .orange {
    background-color: #FF7F00;
  }

  .cyan {
    background-color: #00FFFF;
  }

  .raspberry {
    background-color: #FF007F;
  }

  div {
    height: 100px;
    width: 100px;
    margin-bottom: 5px;
  }
</style>
<div class="orange"></div>
<div class="cyan"></div>
<div class="raspberry"></div>
```
