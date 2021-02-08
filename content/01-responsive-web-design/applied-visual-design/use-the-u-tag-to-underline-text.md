---
id: 587d781a367417b2b2512ab8
title: Use a tag u para sublinhar um texto
challengeType: 0
videoUrl: 'https://scrimba.com/c/cN6aQCL'
forumTopicId: 301082
dashedName: use-the-u-tag-to-underline-text
---

# --description--

Para sublinhar um texto, você pode usar a tag `u`. Isso é usado normalmente para destacar uma seção do texto que é importante, ou precisa ser lembrada. Com a tag `u`, o navegador aplica a propriedade CSS `text-decoration: underline;` ao elemento.

# --instructions--

Coloque a tag `u` somente dentro do texto "Ph.D. students".

**Nota:** Tente evitar a tag `u` quando ela pode ser confundida com um link. Tags âncora também têm uma formatação padrão de sublinhar.

# --hints--

Seu código deve ter uma tag `u` para a marcação.

```js
assert($('u').length === 1);
```

A tag `u` deve ficar entre o texto `Ph.D. students`.

```js
assert($('u').text() === 'Ph.D. students');
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
      <h4>Google</h4>
      <p>Google foi fundado por Larry Page e Sergey Brin enquanto faziam doutorado na <strong>Universidade de Stanford</strong>.</p>
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
      <h4>Google</h4>
      <p>Google foi fundado por Larry Page e Sergey Brin enquanto faziam doutorado na <strong>Universidade de Stanford</strong>.</p>
    </div>
    <div class="cardLinks">
      <a href="https://en.wikipedia.org/wiki/Larry_Page" target="_blank" class="links">Larry Page</a><br><br>
      <a href="https://en.wikipedia.org/wiki/Sergey_Brin" target="_blank" class="links">Sergey Brin</a>
    </div>
  </div>
</div>
```
