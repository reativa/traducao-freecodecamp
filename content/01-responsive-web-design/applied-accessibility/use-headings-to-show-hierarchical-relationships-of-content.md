---
id: 587d774d367417b2b2512a9e
title: Use Headings to Show Hierarchical Relationships of Content
challengeType: 0
videoUrl: 'https://scrimba.com/c/cqVEktm'
forumTopicId: 301026
dashedName: use-headings-to-show-hierarchical-relationships-of-content
---

# --description--

Os cabeçalhos (elementos `h1` a `h6`) são tags burras que ajudam a fornecer estrutura e rotulagem ao seu conteúdo. Os leitores de tela podem ser configurados para ler apenas os cabeçalhos de uma página para que o usuário obtenha um resumo. Isso significa que é importante que as tags de título em sua marcação tenham significado semântico e se relacionem umas com as outras,e não sejam escolhidas apenas por seus valores de tamanho.

*Significado semântico* significa que a tag que você usa em torno do conteúdo indica o tipo de informação que ela contém.

Se você estivesse escrevendo um artigo com uma introdução, um corpo e uma conclusão, não faria muito sentido colocar a conclusão como uma subseção do corpo em seu esboço. Ela deveria  estar em sua própria seção. Da mesma forma, as tags de título em uma página da web precisam estar em ordem e indicar as relações hierárquicas de seu conteúdo.

Títulos com classificação igual (ou superior) iniciam novas seções implícitas, títulos com classificação inferior começam subseções da anterior.

Como exemplo, uma página com um elemento `h2` seguido por várias subseções rotuladas com tags `h4` confundiria um usuário de leitor de tela. Com seis opções, é tentador usar uma tag porque fica melhor em um navegador, mas você pode usar CSS para editar o tamanho relativo.

Um último ponto, cada página deve sempre ter um (e apenas um) elemento `h1`, que é o assunto principal do seu conteúdo. Este e outros cabeçalhos são usados ​​em parte pelos mecanismos de pesquisa para entender o tópico da página.

# --instructions--

Camper Cat quer uma página em seu site dedicada a se tornar um ninja. Ajude-o a corrigir os títulos para que sua marcação dê significado semântico ao conteúdo e mostre as relações pai-filho adequadas de suas seções. Mude todas as tags `h5` para o nível de cabeçalho apropriado para indicar que são subseções das tags `h2`. Use tags `h3` para esse propósito.

# --hints--

Seu código deve ter 6 tags `h3`.

```js
assert ($ ('h3'). length === 6);
```

Seu código deve ter 6 tags de fechamento `h3`.

```js
assert ((code.match (/ \ / h3 / g) || []). length === 6);
```

Seu código não deve ter nenhuma tag `h5`.

```js
assert ($ ('h5'). length === 0);
```

Seu código não deve ter nenhuma tag de fechamento `h5`.

```js
assert(/\/h5/.test(code) === false);
```

# --seed--

## --seed-contents--

```html
<h1>How to Become a Ninja</h1>
<main>
  <h2>Learn the Art of Moving Stealthily</h2>
  <h5>How to Hide in Plain Sight</h5>
  <h5>How to Climb a Wall</h5>

  <h2>Learn the Art of Battle</h2>
  <h5>How to Strengthen your Body</h5>
  <h5>How to Fight like a Ninja</h5>

  <h2>Learn the Art of Living with Honor</h2>
  <h5>How to Breathe Properly</h5>
  <h5>How to Simplify your Life</h5>
</main>
```

# --solutions--

```html
<h1>How to Become a Ninja</h1>
<main>
  <h2>Learn the Art of Moving Stealthily</h2>
  <h3>How to Hide in Plain Sight</h3>
  <h3>How to Climb a Wall</h3>

  <h2>Learn the Art of Battle</h2>
  <h3>How to Strengthen your Body</h3>
  <h3>How to Fight like a Ninja</h3>

  <h2>Learn the Art of Living with Honor</h2>
  <h3>How to Breathe Properly</h3>
  <h3>How to Simplify your Life</h3>
</main>
```
