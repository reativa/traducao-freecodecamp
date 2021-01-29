---
id: 587d778f367417b2b2512aae
title: Give Links Meaning by Using Descriptive Link Text
challengeType: 0
videoUrl: 'https://scrimba.com/c/c437DcV'
forumTopicId: 301013
dashedName: give-links-meaning-by-using-descriptive-link-text
---

# --description--

Os usuários de leitores de tela têm opções diferentes para o tipo de conteúdo que seu dispositivo lê. Isso inclui pular para (ou mais) elementos de referência, pular para o conteúdo principal ou obter um resumo da página a partir dos títulos. Outra opção é ouvir apenas os links disponíveis em uma página.

Os leitores de tela fazem isso lendo o texto do link ou o que está entre as tags âncora (`a`). Ter uma lista de links "clique aqui" ou "leia mais" não é útil. Em vez disso, você deve usar um texto breve, mas descritivo, dentro das tags `a` para fornecer mais significado para esses usuários.

# --instructions--

O texto do link que a Camper Cat está usando não é muito descritivo sem o contexto da situação. Mova as tags âncora (`a`) para que envolvam o texto "informações sobre baterias " ao invés do "Clique aqui ".

# --hints--

Seu código deve mover as tags âncora `a` das palavras "Clique aqui" para envolver as palavras "informações sobre baterias ".
```js
assert(
  $('a')
    .text()
    .match(/^(information about batteries)$/g)
);
```

O elemento `a` deve ter um atributo` href` com um valor de uma string vazia `" "`.

```js
assert($('a').attr('href') === '');
```

O elemento `a` deve ter uma tag a fechando

```js
assert(
  code.match(/<\/a>/g) &&
    code.match(/<\/a>/g).length === code.match(/<a href=(''|"")>/g).length
);
```

# --seed--

## --seed-contents--

```html
<body>
  <header>
    <h1>Deep Thoughts with Master Camper Cat</h1>
  </header>
  <article>
    <h2>Defeating your Foe: the Red Dot is Ours!</h2>
    <p>Felines the world over have been waging war on the most persistent of foes. This red nemesis combines both cunning stealth and lightning speed. But chin up, fellow fighters, our time for victory may soon be near. <a href="">Click here</a> for information about batteries</p>
  </article>
</body>
```

# --solutions--

```html
<body>
  <header>
    <h1>Deep Thoughts with Master Camper Cat</h1>
  </header>
  <article>
    <h2>Defeating your Foe: the Red Dot is Ours!</h2>
    <p>Felines the world over have been waging war on the most persistent of foes. This red nemesis combines both cunning stealth and lightning speed. But chin up, fellow fighters, our time for victory may soon be near. Click here for <a href="">information about batteries</a></p>
  </article>
</body>
```
