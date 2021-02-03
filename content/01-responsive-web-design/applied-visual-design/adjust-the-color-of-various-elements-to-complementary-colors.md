---
id: 587d78a4367417b2b2512ad3
title: Adjust the Color of Various Elements to Complementary Colors
challengeType: 0
videoUrl: 'https://scrimba.com/c/cWmPpud'
forumTopicId: 301033
dashedName: adjust-the-color-of-various-elements-to-complementary-colors
---

# --description--

O desafio de cores complementares mostrou que cores opostas na paleta de cores podem fazer as outras cores parecerem mais vibrantes quando colocadas lado a lado. Contudo, o contraste visual forte pode ser ruim se for usado em demasia em um site, e pode, às vezes, tornar um texto difícil de ler se for colocado sobre um plano de fundo de cor complementar. Na prática, uma das cores é normalmente dominante e a cor complementar é usada para trazer mais atenção visual a determinado conteúdo na página.
 
# --instructions--

Esta página usará uma sombra em azul-petróleo (`#09A7A1`) como cor dominante, e esta cor complementar em laranja (`#FF790E`) para destacar visualmente os botões de inscrição. Mude o `background-color` do `header` e do `footer` de preto para a cor azul-petróleo. Depois mude a `color` do texto em `h2` para azul-petróleo também. Por fim, mude o `background-color` do `button` para a cor laranja.

# --hints--

O elemento `header` deve ter `background-color` com o valor #09A7A1.

```js
assert($('header').css('background-color') == 'rgb(9, 167, 161)');
```

O elemento `footer` deve ter `background-color` com o valor #09A7A1.

```js
assert($('footer').css('background-color') == 'rgb(9, 167, 161)');
```
O elemento `h2` deve ter `color` com o valor #09A7A1.

```js
assert($('h2').css('color') == 'rgb(9, 167, 161)');
```
O elemento `button` deve ter `background-color` com o valor #FF790E.

```js
assert($('button').css('background-color') == 'rgb(255, 121, 14)');
```

# --seed--

## --seed-contents--

```html
<style>
  body {
    background-color: white;
  }
  header {
    background-color: black;
    color: white;
    padding: 0.25em;
  }
  h2 {
    color: black;
  }
  button {
    background-color: white;
  }
  footer {
    background-color: black;
    color: white;
    padding: 0.5em;
  }
</style>
<header>
  <h1>Cooking with FCC!</h1>
</header>
<main>
  <article>
    <h2>Machine Learning in the Kitchen</h2>
    <p>Join this two day workshop that walks through how to implement cutting-edge snack-getting algorithms with a command line interface. Coding usually involves writing exact instructions, but sometimes you need your computer to execute flexible commands, like <code>fetch Pringles</code>.</p>
    <button>Sign Up</button>
  </article>
  <article>
    <h2>Bisection Vegetable Chopping</h2>
    <p>This week-long retreat will level-up your coding ninja skills to actual ninja skills. No longer is the humble bisection search limited to sorted arrays or coding interview questions, applying its concepts in the kitchen will have you chopping carrots in O(log n) time before you know it.</p>
    <button>Sign Up</button>
  </article>
</main>
<br>
<footer>&copy; 2018 FCC Kitchen</footer>
```

# --solutions--

```html
<style>
  body {
    background-color: white;
  }
  header {
    background-color: #09A7A1;
    color: white;
    padding: 0.25em;
  }
  h2 {
    color: #09A7A1;
  }
  button {
    background-color: #FF790E;
  }
  footer {
    background-color: #09A7A1;
    color: white;
    padding: 0.5em;
  }
</style>
<header>
  <h1>Cooking with FCC!</h1>
</header>
<main>
  <article>
    <h2>Machine Learning in the Kitchen</h2>
    <p>Join this two day workshop that walks through how to implement cutting-edge snack-getting algorithms with a command line interface. Coding usually involves writing exact instructions, but sometimes you need your computer to execute flexible commands, like <code>fetch Pringles</code>.</p>
    <button>Sign Up</button>
  </article>
  <article>
    <h2>Bisection Vegetable Chopping</h2>
    <p>This week-long retreat will level-up your coding ninja skills to actual ninja skills. No longer is the humble bisection search limited to sorted arrays or coding interview questions, applying its concepts in the kitchen will have you chopping carrots in O(log n) time before you know it.</p>
    <button>Sign Up</button>
  </article>
</main>
<br>
<footer>&copy; 2018 FCC Kitchen</footer>
```
