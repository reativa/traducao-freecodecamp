---
id: 587d7791367417b2b2512ab3
title: Crie um equilíbrio visual (Visual Balance) usando a propriedade 'text-align'
challengeType: 0
videoUrl: 'https://scrimba.com/c/c3b4EAp'
forumTopicId: 301053
dashedName: create-visual-balance-using-the-text-align-property
---

# --description--

Essa sessão do currículo foca no Design Visual Aplicado (Applied Visual Design). O primeiro grupo de desafios constrói o layout do cartão que foi dado para mostrar alguns princípios importantes.

Grande parte do conteúdo de uma página é composto por texto (text). O CSS tem diversas opções para alinhar isso com a propriedade `text-align`.

`text-align: justify;` faz com que todas as linhas, exceto a última, encontrem as bordas da direita e esquerda da sua caixa;

`text-align: center;` centraliza o texto na caixa;

`text-align: right;` alinha o texto a direita da caixa;

And `text-align: left;` (o padrão) alinha o texto a esquerda da caixa.

# --instructions--

Alinhe o texto com a tag `h4`, onde está escrito "Google", para o centro. Depois justifiquue o parágrafo que contém as informações de como o Google foi criado.

# --hints--

Seu código deve usar a propriedade "text-align: center" na tag `h4` para centraliza-la.

```js
assert($('h4').css('text-align') == 'center');
```

Seu código deve usar a propriedade "text-align: justify" na tag `p` para justificá-la.

```js
assert($('p').css('text-align') == 'justify');
```

# --seed--

## --seed-contents--

```html
<style>
  h4 {

  }
  p {

  }
  .links {
    margin-right: 20px;

  }
  .fullCard {
    border: 1px solid #ccc;
    border-radius: 5px;
    margin: 10px 5px;
    padding: 4px;
  }
  .cardContent {
    padding: 10px;
  }
</style>
<div class="fullCard">
  <div class="cardContent">
    <div class="cardText">
      <h4>Google</h4>
      <p>Google was founded by Larry Page and Sergey Brin while they were Ph.D. students at Stanford University.</p>
    </div>
    <div class="cardLinks">
      <a href="https://en.wikipedia.org/wiki/Larry_Page" target="_blank" class="links">Larry Page</a>
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
  }
  p {
    text-align: justify;
  }
  .links {
    margin-right: 20px;

  }
  .fullCard {
    border: 1px solid #ccc;
    border-radius: 5px;
    margin: 10px 5px;
    padding: 4px;
  }
  .cardContent {
    padding: 10px;
  }
</style>
<div class="fullCard">
  <div class="cardContent">
    <div class="cardText">
      <h4>Google</h4>
      <p>Google was founded by Larry Page and Sergey Brin while they were Ph.D. students at Stanford University.</p>
    </div>
    <div class="cardLinks">
      <a href="https://en.wikipedia.org/wiki/Larry_Page" target="_blank" class="links">Larry Page</a>
      <a href="https://en.wikipedia.org/wiki/Sergey_Brin" target="_blank" class="links">Sergey Brin</a>
    </div>
  </div>
</div>
```
