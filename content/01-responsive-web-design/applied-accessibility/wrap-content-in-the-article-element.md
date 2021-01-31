---
id: 587d774e367417b2b2512aa0
title: Wrap Content in the article Element
challengeType: 0
videoUrl: 'https://scrimba.com/c/cPp79S3'
forumTopicId: 301029
dashedName: wrap-content-in-the-article-element
---
# --description--

O `article` é outro dos novos elementos HTML5 que adiciona significado semântico à sua marcação. O `article` é um elemento de seccionamento e é usado para envolver conteúdo independente e autocontido. A tag funciona bem com entradas de blog, postagens de fórum ou artigos de notícias.

Determinar se o conteúdo pode ser independente geralmente é uma questão de julgamento, mas existem alguns testes simples que você pode usar. Pergunte a si mesmo: se você removeu todo o contexto circundante, esse conteúdo ainda faria sentido? Da mesma forma para textos, o conteúdo se manteria se estivesse em um feed RSS?

Lembre-se de que as pessoas que usam tecnologias assistivas contam com uma marcação organizada e semanticamente significativa para entender melhor seu trabalho.

**Nota sobre `section` e `div`**
O elemento `section` também é novo no HTML5 e tem um significado semântico ligeiramente diferente do `article`. Um `article` é para um conteúdo autônomo, e uma `section` é para agrupar conteúdo relacionado por temas. Eles podem ser usados ​​uns com os outros, conforme necessário. Por exemplo, se um livro é o `article`, então cada capítulo é uma `section`. Quando não há relacionamento entre grupos de conteúdo, use uma `div`.

```html
<div> - groups content
<section> - groups related content
<article> - groups independent, self-contained content
```

# --instructions--


O Camper Cat usou as tags `article` para envolver as postagens em sua página de blog, mas ele se esqueceu de usá-las na parte superior. Altere a tag `div` para usar uma tag `article`.


# --hints--

Seu código deve ter três tags `article`.

```js
assert($('article').length == 3);
```

Seu código não deve ter nenhuma tag `div`.

```js
assert($('div').length == 0);
```

# --seed--

## --seed-contents--

```html
<h1>Deep Thoughts with Master Camper Cat</h1>
<main>
  <div>
    <h2>The Garfield Files: Lasagna as Training Fuel?</h2>
    <p>The internet is littered with varying opinions on nutritional paradigms, from catnip paleo to hairball cleanses. But let's turn our attention to an often overlooked fitness fuel, and examine the protein-carb-NOM trifecta that is lasagna...</p>
  </div>

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
</main>
```

# --solutions--

```html
<h1>Deep Thoughts with Master Camper Cat</h1>
<main>
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
</main>
```
