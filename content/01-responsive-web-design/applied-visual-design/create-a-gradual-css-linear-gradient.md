---
id: 587d78a5367417b2b2512ad6
title: Create a Gradual CSS Linear Gradient
challengeType: 0
videoUrl: 'https://scrimba.com/c/cg4dpt9'
forumTopicId: 301047
dashedName: create-a-gradual-css-linear-gradient
---

# --description--

A aplicação de uma cor em elementos HTML não se limita a um matiz plano. CSS fornece a capacidade de usar transições de cores, também conhecidas como gradientes, em elementos. Isso é acessado por meio da função `linear-gradient()`. Aqui está a sintaxe geral:

`background: linear-gradient(gradient_direction, color 1, color 2, color 3, ...);`

O primeiro argumento especifica a direção a partir da qual a transição de cor começa - pode ser declarada como um grau, onde `90deg` cria um gradiente horizontal (da esquerda para a direita) e `45deg` cria um gradiente diagonal (da parte inferior esquerda para a direita superior) . Os argumentos a seguir especificam a ordem das cores usadas no gradiente.

Exemplo:

`background: linear-gradient(90deg, red, yellow, rgb(204, 204, 255));`

# --instructions--

Use um `linear-gradient ()` para o elemento `div``s`, e defina-o a partir de uma direção de 35 graus para alterar a cor de `# CCFFFF` para `# FFCCCC`.

# --hints--

O elemento `div` deve ter um `linear-gradient` seguindo com a direção e cores especificadas.

```js
assert(
  $('div')
    .css('background-image')
    .match(
      /linear-gradient\(35deg, rgb\(204, 255, 255\), rgb\(255, 204, 204\)\)/gi
    )
);
```

# --seed--

## --seed-contents--

```html
<style>
  div {
    border-radius: 20px;
    width: 70%;
    height: 400px;
    margin: 50px auto;

  }

</style>

<div></div>
```

# --solutions--

```html
<style>
  div {
    border-radius: 20px;
    width: 70%;
    height: 400px;
    margin: 50px auto;
    background: linear-gradient(35deg, #CCFFFF, #FFCCCC);
  }
</style>
<div></div>
```
