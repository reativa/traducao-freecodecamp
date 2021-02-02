---
id: 587d7790367417b2b2512ab1
title: Use tabindex to Specify the Order of Keyboard Focus for Several Elements
challengeType: 0
videoUrl: 'https://scrimba.com/c/cmzRRcb'
forumTopicId: 301028
dashedName: use-tabindex-to-specify-the-order-of-keyboard-focus-for-several-elements
---

# --description--

O atributo `tabindex` também especifica a ordem de tabulação exata dos elementos. Isso é obtido quando o valor do atributo é definido como um número positivo de 1 ou superior.

Definir um `tabindex =" 1 "` trará o foco do teclado para esse elemento primeiro. Em seguida, ele percorre a sequência de valores `tabindex` especificados (2, 3, etc.), antes de mover para os itens padrão e o `tabindex = "0"`.

É importante observar que quando a ordem das guias é definida dessa forma, ela substitui a ordem padrão (que usa o código-fonte HTML). Isso pode confundir os usuários que esperam iniciar a navegação do topo da página. Esta técnica pode ser necessária em algumas circunstâncias, mas em termos de acessibilidade, tome cuidado antes de aplicá-la.

Aqui está um exemplo:

`<div tabindex="1">I get keyboard focus, and I get it first!</div>`

`<div tabindex="2">I get keyboard focus, and I get it second!</div>`

# --instructions--

Camper Cat tem um campo de pesquisa em sua página de citações inspiradoras, que ele planeja posicionar no canto superior direito com CSS. Ele deseja que os controles de formulário de pesquisa `input` e envio `input` sejam os dois primeiros itens na ordem das guias. Adicione um atributo `tabindex` definido como `"1"` para a pesquisa `input`, e um atributo `tabindex` definido como `"2"` para enviar `input`.

# --hints--

Seu código deve adicionar um atributo `tabindex` à tag search `input`.

```js
assert($('#search').attr('tabindex'));
```

Seu código deve adicionar um atributo `tabindex` à tag `input` do submit.

```js
assert($('#submit').attr('tabindex'));
```

Seu código deve definir o atributo `tabindex` na tag de pesquisa `input` para um valor de 1.

```js
assert($('#search').attr('tabindex') == '1');
```

Seu código deve definir o atributo `tabindex` na tag `input` do submit para um valor de 2.

```js
assert($('#submit').attr('tabindex') == '2');
```

# --seed--

## --seed-contents--

```html
<body>
  <header>
    <h1>Even Deeper Thoughts with Master Camper Cat</h1>
    <nav>
      <ul>
        <li><a href="">Home</a></li>
        <li><a href="">Blog</a></li>
        <li><a href="">Training</a></li>
      </ul>
    </nav>
  </header>
  <form>
    <label for="search">Search:</label>


    <input type="search" name="search" id="search">
    <input type="submit" name="submit" value="Submit" id="submit">


  </form>
  <h2>Inspirational Quotes</h2>
  <blockquote>
    <p>&ldquo;There's no Theory of Evolution, just a list of creatures I've allowed to live.&rdquo;<br>
    - Chuck Norris</p>
  </blockquote>
  <blockquote>
    <p>&ldquo;Wise men say forgiveness is divine, but never pay full price for late pizza.&rdquo;<br>
    - TMNT</p>
  </blockquote>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

# --solutions--

```html
<body>
  <header>
    <h1>Even Deeper Thoughts with Master Camper Cat</h1>
    <nav>
      <ul>
        <li><a href="">Home</a></li>
        <li><a href="">Blog</a></li>
        <li><a href="">Training</a></li>
      </ul>
    </nav>
  </header>
  <form>
    <label for="search">Search:</label>


    <input tabindex="1" type="search" name="search" id="search">
    <input tabindex="2" type="submit" name="submit" value="Submit" id="submit">


  </form>
  <h2>Inspirational Quotes</h2>
  <blockquote>
    <p>&ldquo;There's no Theory of Evolution, just a list of creatures I've allowed to live.&rdquo;<br>
    - Chuck Norris</p>
  </blockquote>
  <blockquote>
    <p>&ldquo;Wise men say forgiveness is divine, but never pay full price for late pizza.&rdquo;<br>
    - TMNT</p>
  </blockquote>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```
