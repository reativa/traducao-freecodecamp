---
id: 587d78a4367417b2b2512ad4
title: Adjust the Hue of a Color
challengeType: 0
videoUrl: 'https://scrimba.com/c/cPp38TZ'
forumTopicId: 301036
dashedName: adjust-the-hue-of-a-color
---

# --description--

As cores têm várias características, incluindo Hue(matiz), Saturation(saturação) e Lightness(luminosidade). CSS3 introduziu a propriedade `hsl ()` como uma forma alternativa de escolher uma cor, declarando diretamente essas características.

**Hue** é o que as pessoas geralmente chamam de 'cor'. Se você imaginar um espectro de cores começando com o vermelho à esquerda, passando pelo verde no meio e pelo azul à direita, o matiz é onde uma cor se ajusta ao longo desta linha. Em `hsl ()`, *hue* usa um conceito de roda de cores em vez do espectro, onde o ângulo da cor no círculo é dado como um valor entre 0 e 360.

**Saturation** é a quantidade de cinza em uma cor. Uma cor totalmente saturada não contém cinza e uma cor minimamente saturada é quase totalmente cinza. Sendo uma porcentagem com 100% igual a totalmente saturado.

**Lightness**  é a quantidade de branco ou preto em uma cor. Uma porcentagem é fornecida variando de 0% (preto) a 100% (branco), onde 50% é a cor normal.

Aqui estão alguns exemplos de uso de `hsl ()` com cores de claridade normais totalmente saturadas:

<table class='table table-striped'><thead><tr><th>Color</th><th>HSL</th></tr></thead><tbody><tr><td>red</td><td>hsl(0, 100%, 50%)</td></tr><tr><td>yellow</td><td>hsl(60, 100%, 50%)</td></tr><tr><td>green</td><td>hsl(120, 100%, 50%)</td></tr><tr><td>cyan</td><td>hsl(180, 100%, 50%)</td></tr><tr><td>blue</td><td>hsl(240, 100%, 50%)</td></tr><tr><td>magenta</td><td>hsl(300, 100%, 50%)</td></tr></tbody></table>

# --instructions--

Altere a `background-color` de cada elemento `div` com base nos nomes das classes (`green`,`cyan` ou `blue`) usando `hsl ()`. Todos os três devem ter saturação total e leveza normal.

# --hints--

Seu código deve usar a propriedade `hsl ()` para declarar a cor verde.

```js
assert(code.match(/\.green\s*?{\s*?background-color:\s*?hsl/gi));
```

Seu código deve usar a propriedade `hsl ()` para declarar a cor ciano.

```js
assert(code.match(/\.cyan\s*?{\s*?background-color:\s*?hsl/gi));
```

Seu código deve usar a propriedade `hsl ()` para declarar a cor azul.

```js
assert(code.match(/\.blue\s*?{\s*?background-color:\s*?hsl/gi));
```

O elemento `div` com classe `green` deve ter uma `background-color` verde.

```js
assert($('.green').css('background-color') == 'rgb(0, 255, 0)');
```

O elemento `div` com a classe `cyan` deve ter uma `background-color` de ciano.

```js
assert($('.cyan').css('background-color') == 'rgb(0, 255, 255)');
```

O elemento `div` com a classe `blue` deve ter uma `background-color` azul.

```js
assert($('.blue').css('background-color') == 'rgb(0, 0, 255)');
```

# --seed--

## --seed-contents--

```html
<style>
  body {
    background-color: #FFFFFF;
  }

  .green {
    background-color: #000000;
  }

  .cyan {
    background-color: #000000;
  }

  .blue {
    background-color: #000000;
  }

  div {
    display: inline-block;
    height: 100px;
    width: 100px;
  }
</style>

<div class="green"></div>
<div class="cyan"></div>
<div class="blue"></div>
```

# --solutions--

```html
<style>
  body {
    background-color: #FFFFFF;
  }

  .green {
    background-color: hsl(120, 100%, 50%);
  }

  .cyan {
    background-color:   hsl(180, 100%, 50%);
  }

  .blue {
    background-color: hsl(240, 100%, 50%);
  }

  div {
    display: inline-block;
    height: 100px;
    width: 100px;
  }
</style>
<div class="green"></div>
<div class="cyan"></div>
<div class="blue"></div>
```
