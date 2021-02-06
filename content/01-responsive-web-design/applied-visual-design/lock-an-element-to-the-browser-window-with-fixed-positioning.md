---
id: 587d781e367417b2b2512acc
title: Bloquear um elemento para a janela do navegador com posição fixa 
challengeType: 0
videoUrl: 'https://scrimba.com/c/c2MDNUR'
forumTopicId: 301061
dashedName: lock-an-element-to-the-browser-window-with-fixed-positioning
---

# --description--

O próximo esquema de layout que o CSS oferece é a posição `fixed`, que é um tipo de posicionamento absoluto que bloqueia um elemento em relação à janela do navegador. Semelhante ao posicionamento absoluto, é utilizado com as propriedades de deslocamento do CSS e também remove o elemento do fluxo normal do documento. Outros items não "notam" onde está posicionado, o que pode exigir alguns ajustes em outros lugares.

Uma principal diferença entre as posições `fixed` e `absolute` é que o elemento com uma posição fixa não se moverá quando o usuário usar a barra de rolagem.

# --instructions--

A barra de navegação no código está rotulado com um id de `navbar`. Mude sua `position` para `fixed`, e desloque-o 0 pixels a partir do `top` e 0 pixels a partir `left`. Após ter adicionado o código, role a janela de visualização para ver como a navegação continua no lugar.

# --hints--

O elemento `#navbar` deverá ter uma `position` definido como `fixed`.

```js
assert($('#navbar').css('position') == 'fixed');
```

Seu código deve usar o deslocamento `top` do CSS de 0 pixels no elemento `#navbar`.

```js
assert($('#navbar').css('top') == '0px');
```

Seu código deve usar o deslocamento `left` do CSS de 0 pixels no elemento `#navbar`.

```js
assert($('#navbar').css('left') == '0px');
```

# --seed--

## --seed-contents--

```html
<style>
  body {
    min-height: 150vh;
  }
  #navbar {
    width: 100%;
    background-color: #767676;
  }
  nav ul {
    margin: 0px;
    padding: 5px 0px 5px 30px;
  }
  nav li {
    display: inline;
    margin-right: 20px;
  }
  a {
    text-decoration: none;
  }
</style>
<body>
  <header>
    <h1>Welcome!</h1>
    <nav id="navbar">
      <ul>
        <li><a href="">Home</a></li>
        <li><a href="">Contact</a></li>
      </ul>
    </nav>
  </header>
  <p>I shift up when the #navbar is fixed to the browser window.</p>
</body>
```

# --solutions--

```html
<style>
  body {
    min-height: 150vh;
  }
  #navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background-color: #767676;
  }
  nav ul {
    margin: 0px;
    padding: 5px 0px 5px 30px;
  }
  nav li {
    display: inline;
    margin-right: 20px;
  }
  a {
    text-decoration: none;
  }
</style>
<body>
  <header>
    <h1>Welcome!</h1>
    <nav id="navbar">
      <ul>
        <li><a href="">Home</a></li>
        <li><a href="">Contact</a></li>
      </ul>
    </nav>
  </header>
  <p>I shift up when the #navbar is fixed to the browser window.</p>
</body>
```
