---
id: 587d778c367417b2b2512aa9
title: Standardize Times with the HTML5 datetime Attribute
challengeType: 0
videoUrl: 'https://scrimba.com/c/cmzMgtz'
forumTopicId: 301025
dashedName: standardize-times-with-the-html5-datetime-attribute
---

# --description--

Continuando com o tema de datas, o HTML5 também introduziu o elemento `time` junto com um atributo `datetime` para padronizar os horários. Este é um elemento embutido que pode envolver uma data ou hora em uma página. Um formato válido dessa data é mantido pelo atributo `datetime`. Este é o valor acessado por dispositivos auxiliares. Ajuda a evitar confusão ao declarar uma versão padronizada de um horário, mesmo que seja escrito de maneira informal ou coloquial no texto.

Aqui está um exemplo:

`<p>Master Camper Cat officiated the cage match between Goro and Scorpion <time datetime="2013-02-13">last Wednesday</time>, which ended in a draw.</p>`

# --instructions--

Os resultados da pesquisa de Mortal Kombat do Camper Cat chegaram! Envolva uma tag `time` em torno do texto "Thursday, September 15&lt;sup>th&lt;/sup>" e adicione um atributo `datetime` a ele, definido como "2016-09-15".

# --hints--

Seu código deve ter um elemento `p` que inclui o texto `Thank you to everyone for responding to Master Camper Cat's survey.` e incluir um elemento `time`.

```js
assert (timeElement.length);
```

Suas tags `time` adicionadas devem envolver o texto `Thursday, September 15<sup>th</sup>`.

```js
afirmar(
   timeElement.length &&
     $ (timeElement) .html (). trim () === 'Quinta-feira, 15 de setembro <sup> th </sup>'
);
```

A tag `time` adicionada deve ter um atributo `datetime` não vazio.

```js
assert (datetimeAttr && datetimeAttr.length);
```

O atributo `datetime` adicionado deve ser definido para um valor igual a `2016-09-15`.

```js
assert(datetimeAttr === '2016-09-15');
```

# --seed--

## --after-user-code--

```html
<script>
const pElement = $("article > p")
  .filter((_, elem) => $(elem).text().includes("Thank you to everyone for responding to Master Camper Cat's survey."));
const timeElement = pElement[0] ? $(pElement[0]).find("time") : null;
const datetimeAttr = $(timeElement).attr("datetime");
</script>
```

## --seed-contents--

```html
<body>
  <header>
    <h1>Tournaments</h1>
  </header>
  <article>
    <h2>Mortal Kombat Tournament Survey Results</h2>

    <!-- Only change code below this line -->

    <p>Thank you to everyone for responding to Master Camper Cat's survey. The best day to host the vaunted Mortal Kombat tournament is Thursday, September 15<sup>th</sup>. May the best ninja win!</p>

    <!-- Only change code above this line -->

    <section>
      <h3>Comments:</h3>
      <article>
        <p>Posted by: Sub-Zero on <time datetime="2016-08-13T20:01Z">August 13<sup>th</sup></time></p>
        <p>Johnny Cage better be there, I'll finish him!</p>
      </article>
      <article>
        <p>Posted by: Doge on <time datetime="2016-08-15T08:12Z">August 15<sup>th</sup></time></p>
        <p>Wow, much combat, so mortal.</p>
      </article>
      <article>
        <p>Posted by: The Grim Reaper on <time datetime="2016-08-16T00:00Z">August 16<sup>th</sup></time></p>
        <p>Looks like I'll be busy that day.</p>
      </article>
    </section>
  </article>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

# --solutions--

```html
<body>
  <header>
    <h1>Tournaments</h1>
  </header>
  <article>
    <h2>Mortal Kombat Tournament Survey Results</h2>

    <p>Thank you to everyone for responding to Master Camper Cat's survey. The best day to host the vaunted Mortal Kombat tournament is <time datetime="2016-09-15">Thursday, September 15<sup>th</sup></time>. May the best ninja win!</p>

    <section>
      <h3>Comments:</h3>
      <article>
        <p>Posted by: Sub-Zero on <time datetime="2016-08-13T20:01Z">August 13<sup>th</sup></time></p>
        <p>Johnny Cage better be there, I'll finish him!</p>
      </article>
      <article>
        <p>Posted by: Doge on <time datetime="2016-08-15T08:12Z">August 15<sup>th</sup></time></p>
        <p>Wow, much combat, so mortal.</p>
      </article>
      <article>
        <p>Posted by: The Grim Reaper on <time datetime="2016-08-16T00:00Z">August 16<sup>th</sup></time></p>
        <p>Looks like I'll be busy that day.</p>
      </article>
    </section>
  </article>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```
