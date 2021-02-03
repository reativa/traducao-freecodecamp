---
id: 587d778a367417b2b2512aa5
title: Improve Chart Accessibility with the figure Element
challengeType: 0
videoUrl: 'https://scrimba.com/c/cGJMqtE'
forumTopicId: 301015
dashedName: improve-chart-accessibility-with-the-figure-element
---

# --description--


HTML5 introduziu o elemento `figure`, junto com o `figcaption` relacionado. Usados juntos, esses itens envolvem uma representação visual (como uma imagem, diagrama ou gráfico) junto com sua legenda. Isso aumenta a acessibilidade em duas partes, agrupando semanticamente o conteúdo relacionado e fornecendo uma alternativa em texto que explica a `figura`.


Para visualizações de dados como gráficos, a legenda pode ser usada para observar brevemente as tendências ou conclusões para usuários com deficiência visual. Outro desafio abrange como mover uma versão de tabela dos dados do gráfico para fora da tela (usando CSS) para usuários de leitores de tela.

Aqui está um exemplo - observe que a `figcaption` vai dentro das tags `figure` e pode ser combinada com outros elementos:

```html
<figure>
  <img src="roundhouseDestruction.jpeg" alt="Photo of Camper Cat executing a roundhouse kick">
  <br>
  <figcaption>
    Master Camper Cat demonstrates proper form of a roundhouse kick.
  </figcaption>
</figure>
```

# --instructions--

O Camper Cat está trabalhando arduamente na criação de um gráfico de barras que mostra a quantidade de tempo por semana para gastar em treinamento furtivo, combate e armas. Ajude-o a estruturar melhor sua página alterando a tag `div` que ele usou para uma tag `figure`, e a tag `p` que envolva a legenda para uma tag `figcaption`.

# --hints--

Seu código deve ter uma tag `figure`.

```js
assert($('figure').length == 1);
```

Seu código deve ter uma tag `figcaption`.

```js
assert($('figcaption').length == 1);
```

Seu código não deve ter nenhuma tag `div`.

```js
assert($('div').length == 0);
```
Seu código não deve ter nenhuma tag `p`.

```js
assert($('p').length == 0);
```

A `figcaption` deve ser um filho da tag `figure`.

```js
assert($('figure').children('figcaption').length == 1);
```

Seu elemento `figure` deve ter uma tag de fechamento.

```js
assert(
  code.match(/<\/figure>/g) &&
    code.match(/<\/figure>/g).length === code.match(/<figure>/g).length
);
```

# --seed--

## --seed-contents--

```html
<body>
  <header>
    <h1>Training</h1>
    <nav>
      <ul>
        <li><a href="#stealth">Stealth &amp; Agility</a></li>
        <li><a href="#combat">Combat</a></li>
        <li><a href="#weapons">Weapons</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section>

      <!-- Only change code below this line -->
      <div>
        <!-- Stacked bar chart will go here -->
        <br>
        <p>Breakdown per week of time to spend training in stealth, combat, and weapons.</p>
      </div>
      <!-- Only change code above this line -->

    </section>
    <section id="stealth">
      <h2>Stealth &amp; Agility Training</h2>
      <article><h3>Climb foliage quickly using a minimum spanning tree approach</h3></article>
      <article><h3>No training is NP-complete without parkour</h3></article>
    </section>
    <section id="combat">
      <h2>Combat Training</h2>
      <article><h3>Dispatch multiple enemies with multithreaded tactics</h3></article>
      <article><h3>Goodbye world: 5 proven ways to knock out an opponent</h3></article>
    </section>
    <section id="weapons">
      <h2>Weapons Training</h2>
      <article><h3>Swords: the best tool to literally divide and conquer</h3></article>
      <article><h3>Breadth-first or depth-first in multi-weapon training?</h3></article>
    </section>
  </main>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

# --solutions--

```html
<body>
  <header>
    <h1>Training</h1>
    <nav>
      <ul>
        <li><a href="#stealth">Stealth &amp; Agility</a></li>
        <li><a href="#combat">Combat</a></li>
        <li><a href="#weapons">Weapons</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section>
      <figure>
        <!-- Stacked bar chart will go here -->
        <br>
        <figcaption>Breakdown per week of time to spend training in stealth, combat, and weapons.</figcaption>
      </figure>
    </section>
    <section id="stealth">
      <h2>Stealth &amp; Agility Training</h2>
      <article><h3>Climb foliage quickly using a minimum spanning tree approach</h3></article>
      <article><h3>No training is NP-complete without parkour</h3></article>
    </section>
    <section id="combat">
      <h2>Combat Training</h2>
      <article><h3>Dispatch multiple enemies with multithreaded tactics</h3></article>
      <article><h3>Goodbye world: 5 proven ways to knock out an opponent</h3></article>
    </section>
    <section id="weapons">
      <h2>Weapons Training</h2>
      <article><h3>Swords: the best tool to literally divide and conquer</h3></article>
      <article><h3>Breadth-first or depth-first in multi-weapon training?</h3></article>
    </section>
  </main>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```
