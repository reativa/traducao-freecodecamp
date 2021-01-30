---
id: 587d778a367417b2b2512aa6
title: Improve Form Field Accessibility with the label Element
challengeType: 0
videoUrl: 'https://scrimba.com/c/cGJMMAN'
forumTopicId: 301016
dashedName: improve-form-field-accessibility-with-the-label-element
---

# --description--

Melhorar a acessibilidade com a marcação semântica HTML se aplica ao uso de nomes de tag apropriadas, bem como atributos. Os próximos desafios cobrem alguns cenários importantes usando atributos em formulários.

A tag `label` envolve o texto para um item de controle de formulário específico, geralmente o nome ou rótulo de uma escolha. Isso vincula o significado ao item e torna o formulário mais legível. O atributo `for` em uma tag` label` associa explicitamente essa `label` com o controle de formulário e é usado por leitores de tela.

Você aprendeu sobre botões de opção e seus rótulos em uma lição na seção HTML básico. Nessa lição, envolvemos o elemento de entrada do botão de opção dentro de um elemento `label` junto com o texto do rótulo para tornar o texto clicável. Outra maneira de conseguir isso é usando o atributo `for` conforme explicado nesta lição.

O valor do atributo `for` deve ser igual ao valor do atributo `id` do controle de formulário. Aqui está um exemplo:

```html
<form>
  <label for="name">Name:</label>
  <input type="text" id="name" name="name">
</form>
```

# --instructions--

Camper Cat espera atrair muito interesse pelo seu blog cheio de postagens profundas,sendo assim ele quer incluir um formulário de inscrição por e-mail. Adicione um atributo `for` no` label` do e-mail que corresponda ao `id` em seu campo` input`.

# --hints--

Seu código deve ter um atributo `for` na tag` label` que não está vazio.

```js
assert ($ ('label'). attr ('for'));
```

O valor do atributo `for` deve corresponder ao valor` id` no `input` do e-mail.

```js
assert ($ ('label'). attr ('for') == 'email');
```

# --seed--

## --seed-contents--

```html
<body>
  <header>
    <h1>Deep Thoughts with Master Camper Cat</h1>
  </header>
  <section>
    <form>
      <p>Sign up to receive Camper Cat's blog posts by email here!</p>


      <label>Email:</label>
      <input type="text" id="email" name="email">


      <input type="submit" name="submit" value="Submit">
    </form>
  </section>
  <article>
    <h2>The Garfield Files: Lasagna as Training Fuel?</h2>
    <p>The internet is littered with varying opinions on nutritional paradigms, from catnip paleo to hairball cleanses. But let's turn our attention to an often overlooked fitness fuel, and examine the protein-carb-NOM trifecta that is lasagna...</p>
  </article>
  <img src="samuraiSwords.jpeg" alt="">
  <article>
    <h2>Defeating your Foe: the Red Dot is Ours!</h2>
    <p>Felines the world over have been waging war on the most persistent of foes. This red nemesis combines both cunning stealth and lightning speed. But chin up, fellow fighters, our time for victory may soon be near...</p>
  </article>
  <img src="samuraiSwords.jpeg" alt="">
  <article>
    <h2>Is Chuck Norris a Cat Person?</h2>
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
  <section>
    <form>
      <p>Sign up to receive Camper Cat's blog posts by email here!</p>


      <label for="email">Email:</label>
      <input type="text" id="email" name="email">


      <input type="submit" name="submit" value="Submit">
    </form>
  </section>
  <article>
    <h2>The Garfield Files: Lasagna as Training Fuel?</h2>
    <p>The internet is littered with varying opinions on nutritional paradigms, from catnip paleo to hairball cleanses. But let's turn our attention to an often overlooked fitness fuel, and examine the protein-carb-NOM trifecta that is lasagna...</p>
  </article>
  <img src="samuraiSwords.jpeg" alt="">
  <article>
    <h2>Defeating your Foe: the Red Dot is Ours!</h2>
    <p>Felines the world over have been waging war on the most persistent of foes. This red nemesis combines both cunning stealth and lightning speed. But chin up, fellow fighters, our time for victory may soon be near...</p>
  </article>
  <img src="samuraiSwords.jpeg" alt="">
  <article>
    <h2>Is Chuck Norris a Cat Person?</h2>
    <p>Chuck Norris is widely regarded as the premier martial artist on the planet, and it's a complete coincidence anyone who disagrees with this fact mysteriously disappears soon after. But the real question is, is he a cat person?...</p>
  </article>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```
