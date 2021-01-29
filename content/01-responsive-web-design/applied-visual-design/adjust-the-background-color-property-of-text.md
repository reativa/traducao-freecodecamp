---
id: 587d781b367417b2b2512abc
title: Adjust the background-color Property of Text
challengeType: 0
videoUrl: 'https://scrimba.com/c/cEDqwA6'
forumTopicId: 301032
dashedName: adjust-the-background-color-property-of-text
---

# --description--

Ao invés de ajustar todo o plano de fundo ou a cor do texto para fazer o primeiro plano mais legível, você pode adicionar um `background-color` ao elemento que contém o texto que você deseja enfatizar. Esse desafio usa `rgba()` ao invés de código `hex` ou `rgb()` normal.

<blockquote>rgba representa:<br>  r = vermelho<br>  g = verde<br>  b = azul<br>  a = alfa/nível de opacidade</blockquote>

Os valores RGB podem variar entre 0 e 255. O valor alfa pode variar de 1, que é totalmente opaco ou de cor sólida, até 0, que é totalmente transparente. `rgba()` é ótimo para usar neste caso, pois permite que você ajuste a opacidade. Isso significa que você não precisa bloquear completamente o plano de fundo. 

Você vai usar `background-color: rgba(45, 45, 45, 0.1)` para esse desafio. Ele produz uma cor cinza escuro que é quase transparente devido ao baixo valor de opacidade de 0,1. 

# --instructions--

Para fazer o texto se destacar, ajuste o `background-color` do elemento `h4` para o valor `rgba()` fornecido.

Também para o elemento `h4`, remova a propriedade `height` e adicione um `padding` de 10px.

# --hints--

Seu código deve adicionar uma propriedade `background-color` ao elemento `h4` com o valor `rgba(45, 45, 45, 0.1)`.

```js
assert(
  /(background-color|background):rgba\(45,45,45,0?\.1\)(;?}|;)/gi.test(
    code.replace(/\s/g, '')
  )
);
```
Seu código deve adicionar uma propriedade `padding` ao elemento `h4` com o valor de 10 pixels.

```js
assert(
  $('h4').css('padding-top') == '10px' &&
    $('h4').css('padding-right') == '10px' &&
    $('h4').css('padding-bottom') == '10px' &&
    $('h4').css('padding-left') == '10px'
);
```
A propriedade `height` do elemento `h4` deve ser removida.

```js
assert(!($('h4').css('height') == '25px'));
```

# --seed--

## --seed-contents--

```html
<style>
  h4 {
    text-align: center;
    height: 25px;


  }
  p {
    text-align: justify;
  }
  .links {
    text-align: left;
    color: black;
  }
  .fullCard {
    width: 245px;
    border: 1px solid #ccc;
    border-radius: 5px;
    margin: 10px 5px;
    padding: 4px;
  }
  .cardContent {
    padding: 10px;
  }
  .cardText {
    margin-bottom: 30px;
  }
</style>
<div class="fullCard">
  <div class="cardContent">
    <div class="cardText">
      <h4>Alphabet</h4>
      <hr>
      <p><em>Google was founded by Larry Page and Sergey Brin while they were <u>Ph.D. students</u> at <strong>Stanford University</strong>.</em></p>
    </div>
    <div class="cardLinks">
      <a href="https://en.wikipedia.org/wiki/Larry_Page" target="_blank" class="links">Larry Page</a><br><br>
      <a href="https://en.wikipedia.org/wiki/Sergey_Brin" target="_blank" class="links">Sergey Brin</a>
    </div>
  </div>
</div>
```

# --solutions--

```html
<style>
  h4 {
    text-align: center;
    padding: 10px;
    background-color: rgba(45, 45, 45, 0.1);
  }
  p {
    text-align: justify;
  }
  .links {
    text-align: left;
    color: black;
  }
  .fullCard {
    width: 245px;
    border: 1px solid #ccc;
    border-radius: 5px;
    margin: 10px 5px;
    padding: 4px;
  }
  .cardContent {
    padding: 10px;
  }
  .cardText {
    margin-bottom: 30px;
  }
</style>
<div class="fullCard">
  <div class="cardContent">
    <div class="cardText">
      <h4>Alphabet</h4>
      <hr>
      <p><em>Google was founded by Larry Page and Sergey Brin while they were <u>Ph.D. students</u> at <strong>Stanford University</strong>.</em></p>
    </div>
    <div class="cardLinks">
      <a href="https://en.wikipedia.org/wiki/Larry_Page" target="_blank" class="links">Larry Page</a><br><br>
      <a href="https://en.wikipedia.org/wiki/Sergey_Brin" target="_blank" class="links">Sergey Brin</a>
    </div>
  </div>
</div>
```
