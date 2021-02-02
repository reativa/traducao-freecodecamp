---
id: 587d7790367417b2b2512ab0
title: Use tabindex to Add Keyboard Focus to an Element
challengeType: 0
videoUrl: 'https://scrimba.com/c/cmzMDHW'
forumTopicId: 301027
dashedName: use-tabindex-to-add-keyboard-focus-to-an-element
---

# --description--

O atributo HTML `tabindex` tem três funções distintas relacionadas ao foco do teclado de um elemento. Quando está em uma tag, indica que o elemento pode ser focalizado. O valor (um número inteiro positivo, negativo ou zero) determina o comportamento.

Certos elementos, como links e controles de formulário, recebem automaticamente o foco do teclado quando um usuário passa por uma página, na mesma ordem em que os elementos vêm da marcação de origem HTML. Esta mesma funcionalidade pode ser dada a outros elementos, como `div`,`span` e `p`, colocando um atributo `tabindex = "0"` neles. Aqui está um exemplo:

`<div tabindex="0">I need keyboard focus!</div>`

**Nota:** Um valor `tabindex` negativo (normalmente -1) indica que um elemento pode ser focalizado, mas não pode ser alcançado pelo teclado. Este método geralmente é usado para trazer o foco para o conteúdo de forma programática (como quando uma `div` usada para que uma janela pop-up seja ativada), e isso está além do escopo desses desafios.

# --instructions--

Camper Cat criou uma nova pesquisa para coletar informações sobre seus usuários. Ele sabe que os campos de entrada obtêm o foco do teclado automaticamente, mas quer ter certeza de que os usuários do teclado pausem nas instruções enquanto percorrem os itens. Adicione um atributo `tabindex` à tag `p` e defina seu valor para `"0"`.
 Bônus - o uso de `tabindex` também permite que a pseudo-classe CSS `: focus` funcione na tag `p`.

# --hints--

Seu código deve adicionar um atributo `tabindex` à tag `p` que contém as instruções do formulário.

```js
assert($('p').attr('tabindex'));
```

Seu código deve definir o atributo `tabindex` na tag `p` para um valor de 0.

```js
assert($('p').attr('tabindex') == '0');
```

# --seed--

## --seed-contents--

```html
<head>
  <style>
  p:focus {
    background-color: yellow;
  }
  </style>
</head>
<body>
  <header>
    <h1>Ninja Survey</h1>
  </header>
  <section>
    <form>


      <p>Instructions: Fill in ALL your information then click <b>Submit</b></p>


      <label for="username">Username:</label>
      <input type="text" id="username" name="username"><br>
      <fieldset>
        <legend>What level ninja are you?</legend>
        <input id="newbie" type="radio" name="levels" value="newbie">
        <label for="newbie">Newbie Kitten</label><br>
        <input id="intermediate" type="radio" name="levels" value="intermediate">
        <label for="intermediate">Developing Student</label><br>
        <input id="master" type="radio" name="levels" value="master">
        <label for="master">9th Life Master</label>
      </fieldset>
      <br>
      <fieldset>
      <legend>Select your favorite weapons:</legend>
      <input id="stars" type="checkbox" name="weapons" value="stars">
      <label for="stars">Throwing Stars</label><br>
      <input id="nunchucks" type="checkbox" name="weapons" value="nunchucks">
      <label for="nunchucks">Nunchucks</label><br>
      <input id="sai" type="checkbox" name="weapons" value="sai">
      <label for="sai">Sai Set</label><br>
      <input id="sword" type="checkbox" name="weapons" value="sword">
      <label for="sword">Sword</label>
      </fieldset>
      <br>
      <input type="submit" name="submit" value="Submit">
    </form><br>
  </section>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

# --solutions--

```html
<head>
  <style>
  p:focus {
    background-color: yellow;
  }
  </style>
</head>
<body>
  <header>
    <h1>Ninja Survey</h1>
  </header>
  <section>
    <form>


      <p tabindex="0">Instructions: Fill in ALL your information then click <b>Submit</b></p>


      <label for="username">Username:</label>
      <input type="text" id="username" name="username"><br>
      <fieldset>
        <legend>What level ninja are you?</legend>
        <input id="newbie" type="radio" name="levels" value="newbie">
        <label for="newbie">Newbie Kitten</label><br>
        <input id="intermediate" type="radio" name="levels" value="intermediate">
        <label for="intermediate">Developing Student</label><br>
        <input id="master" type="radio" name="levels" value="master">
        <label for="master">9th Life Master</label>
      </fieldset>
      <br>
      <fieldset>
      <legend>Select your favorite weapons:</legend>
      <input id="stars" type="checkbox" name="weapons" value="stars">
      <label for="stars">Throwing Stars</label><br>
      <input id="nunchucks" type="checkbox" name="weapons" value="nunchucks">
      <label for="nunchucks">Nunchucks</label><br>
      <input id="sai" type="checkbox" name="weapons" value="sai">
      <label for="sai">Sai Set</label><br>
      <input id="sword" type="checkbox" name="weapons" value="sword">
      <label for="sword">Sword</label>
      </fieldset>
      <br>
      <input type="submit" name="submit" value="Submit">
    </form><br>
  </section>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```
