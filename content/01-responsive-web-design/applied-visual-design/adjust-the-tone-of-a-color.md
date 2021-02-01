---
id: 587d78a4367417b2b2512ad5
title: Adjust the Tone of a Color
challengeType: 0
videoUrl: 'https://scrimba.com/c/cEDJvT7'
forumTopicId: 301038
dashedName: adjust-the-tone-of-a-color
---

# --description--

A opção `hsl ()` em CSS também facilita o ajuste do tom de uma cor. A mistura de branco com um matiz puro cria uma tonalidade dessa cor, e a adição de preto criará uma sombra. Como alternativa, um tom é produzido adicionando cinza, ou o matizando e o sombreando. Lembre-se de que o 's' e 'l' de `hsl ()` representam saturação e leveza, respectivamente. A porcentagem de saturação altera a quantidade de cinza e a porcentagem de claridade determina quanto branco ou preto há na cor. Isso é útil quando você tem um matiz básico de que gosta, mas precisa de diferentes variações dele.
# --instructions--

Todos os elementos têm uma `background-color` padrão `transparent`. Nosso elemento `nav` atualmente parece ter um fundo `cyan`, porque o elemento atrás dele tem um `background-color` definido como `cyan`. Adicione um `background-color` ao elemento `nav` para que ele use o mesmo matiz `cyan`, mas tenha valores de `80% saturation` e `25% lightness` para alterar seu tom e sombra.
# --hints--

O elemento `nav` deve ter um `background-color` do tom ciano(cyan) ajustado, usando a propriedade `hsl ()`.

```js
assert(
  code.match(/nav\s*?{\s*?background-color:\s*?hsl\(180,\s*?80%,\s*?25%\)/gi)
);
```

# --seed--

## --seed-contents--

```html
<style>
  header {
    background-color: hsl(180, 90%, 35%);
    color: #FFFFFF;
  }

  nav {

  }

  h1 {
    text-indent: 10px;
    padding-top: 10px;
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
    color: inherit;
  }
</style>

<header>
  <h1>Cooking with FCC!</h1>
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Classes</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>
</header>
```

# --solutions--

```html
<style>
  header {
    background-color: hsl(180, 90%, 35%);
    color: #FFFFFF;
  }

  nav {
    background-color: hsl(180, 80%, 25%);
  }

  h1 {
    text-indent: 10px;
    padding-top: 10px;
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
    color: inherit;
  }
</style>
<header>
  <h1>Cooking with FCC!</h1>
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Classes</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>
</header>
```
