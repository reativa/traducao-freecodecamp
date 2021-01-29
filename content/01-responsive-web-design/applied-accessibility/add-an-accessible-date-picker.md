---
id: 587d778b367417b2b2512aa8
title: Add an Accessible Date Picker
challengeType: 0
videoUrl: 'https://scrimba.com/c/cR3bRbCV'
forumTopicId: 301008
dashedName: add-an-accessible-date-picker
---

# --description--

Os formulários geralmente incluem o campo `input`, que pode ser usado para criar vários e diferentes controles de formulário. O atributo `type` neste elemento indica que tipo de entrada será criada.

Você deve ter notado os tipos de entrada `text` e` submit` em desafios anteriores, e o HTML5 introduziu uma opção para especificar um campo `date`. Dependendo do suporte do navegador, um selecionador de data aparece no campo `input` quando ele está selecionado, o que torna o preenchimento de um formulário mais fácil para todos os usuários.

Para navegadores mais antigos, o tipo padrão será `texto`, então facilita para os usuários mostrar o formato de data esperado no título ou como texto no `placeholder` que é  reservado para o caso.

Aqui está um exemplo: 

```html
<label for="input1">Entre com uma data:</label>
<input type="date" id="input1" name="input1">
```

# --instructions--

Camper Cat está organizando um torneio de Mortal Kombat e quer perguntar a seus concorrentes para ver qual data é a melhor. Adicione uma tag `input` com um atributo `type` igual a "date", um atributo `id` igual "pickdate" e um atributo `name` igual "date".

# --hints--

Seu código deve ter uma tag `input` para o campo do seletor de date.

```js
assert($('input').length == 2);
```

Sua tag `input` deve ter um atributo `type` com um valor de date.

```js
assert($('input').attr('type') == 'date');
```
Sua tag `input` deve ter um  atributo `id` com o valor de pickdate.

```js
assert($('input').attr('id') == 'pickdate');
```

Sua tag `input` deve ter um atributo `name` com um valor de date

```js
assert($('input').attr('name') == 'date');
```

# --seed--

## --seed-contents--

```html
<body>
  <header>
    <h1>Torneios</h1>
  </header>
  <main>
    <section>
      <h2>Pesquisa do Torneio Mortal Kombat</h2>
      <form>
        <p>Diga-nos qual a melhor data para a competição</p>
        <label for="pickdate">Melhor Data:</label>

        <!-- Só mude o código abaixo dessa linha -->



        <!-- Só o mude o código acima dessa linha -->

        <input type="submit" name="submit" value="Submit">
      </form>
    </section>
  </main>
  <footer>&copy;Camper Cat 2018</footer>
</body>
```

# --solutions--

```html
<body>
  <header>
    <h1>Torneios</h1>
  </header>
  <main>
    <section>
      <h2>Pesquisa do Torneio Mortal Kombat</h2>
      <form>
        <p>Diga-nos qual a melhor data para a competição</p>
        <label for="pickdate">Melhor Data:</label>
        <input type="date" id="pickdate" name="date">
        <input type="submit" name="submit" value="Submit">
      </form>
    </section>
  </main>
  <footer>&copy;Camper Cat 2018</footer>
</body>
```
