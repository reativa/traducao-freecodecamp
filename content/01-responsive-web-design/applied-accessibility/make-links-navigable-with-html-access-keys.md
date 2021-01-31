---
id: 587d7790367417b2b2512aaf
title: Make Links Navigable with HTML Access Keys
challengeType: 0
videoUrl: 'https://scrimba.com/c/cQvmaTp'
forumTopicId: 301021
dashedName: make-links-navigable-with-html-access-keys
---

# --description--

O HTML oferece o atributo `accesskey` para especificar uma tecla de atalho para ativar ou trazer o foco para um elemento. Isso pode tornar a navegação mais eficiente para usuários apenas com teclado.

O HTML5 permite que este atributo seja usado em qualquer elemento, mas é particularmente útil quando é usado com elementos interativos. Isso inclui links, botões e controles de formulário.

Aqui está um exemplo:

`<button accesskey="b">Important Button</button>`

# --instructions--

Camper Cat quer que os links em torno dos títulos dos dois artigos do blog tenham atalhos de teclado para que os usuários de seu site possam navegar rapidamente pela história completa. Adicione um atributo `accesskey` em ambos os links e defina o primeiro como "g"(para Garfield) e o segundo como "c"(para Chuck Norris).

# --hints--

Seu código deve adicionar um atributo `accesskey` à tag `a` com o `id` igual a "primeiro ".

```js
assert ($ ('# first'). attr ('accesskey'));
```

Seu código deve adicionar um atributo `accesskey` à tag `a` com o `id` igual a "segundo ".

```js
assert ($ ('# segundo'). attr ('accesskey'));
```

Seu código deve definir o atributo `accesskey` na tag `a` com o `id` igual a "first " para "g ". Note que esse caso é importante.

```js
assert ($ ('# first'). attr ('accesskey') == 'g');
```

Seu código deve definir o atributo `accesskey` na tag `a` com o `id` igual a "segundo" para "c ". Note que esse caso é importante.


```js
assert($('#second').attr('accesskey') == 'c');
```

# --seed--

## --seed-contents--

```html
<body>
  <header>
    <h1>Deep Thoughts with Master Camper Cat</h1>
  </header>
  <article>


    <h2><a id="first" href="#">The Garfield Files: Lasagna as Training Fuel?</a></h2>


    <p>The internet is littered with varying opinions on nutritional paradigms, from catnip paleo to hairball cleanses. But let's turn our attention to an often overlooked fitness fuel, and examine the protein-carb-NOM trifecta that is lasagna...</p>
  </article>
  <article>


    <h2><a id="second" href="#">Is Chuck Norris a Cat Person?</a></h2>


    <p>Chuck Norris is widely regarded as the premier martial artist on the planet, and it's a complete coincidence anyone who disagrees with this fact mysteriously disappears soon after. But the real question is, is he a cat person?...</p>
  </article>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

# --solutions--

```html
<body>
  <header>
    <h1>Deep Thoughts with Master Camper Cat</h1>
  </header>
  <article>


    <h2><a id="first" accesskey="g" href="#">The Garfield Files: Lasagna as Training Fuel?</a></h2>


    <p>The internet is littered with varying opinions on nutritional paradigms, from catnip paleo to hairball cleanses. But let's turn our attention to an often overlooked fitness fuel, and examine the protein-carb-NOM trifecta that is lasagna...</p>
  </article>
  <article>


    <h2><a id="second" accesskey="c" href="#">Is Chuck Norris a Cat Person?</a></h2>


    <p>Chuck Norris is widely regarded as the premier martial artist on the planet, and it's a complete coincidence anyone who disagrees with this fact mysteriously disappears soon after. But the real question is, is he a cat person?...</p>
  </article>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```
