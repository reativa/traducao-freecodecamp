---
id: 5a24bbe0dba28a8d3cbd4c5e
title: Adicionando comentários em JSX
challengeType: 6
forumTopicId: 301376
dashedName: add-comments-in-jsx
---

# --description--

JSX é uma sintáxe que é compilada para JavaScript válido. por vezes, por questões de leitura, você precise adicionar comentários no seu código. Assim como todas linguagens de programação, JSX tem o seu próprio jeito de fazer isso.

Para colocar comentários dentro de um trecho de código em JSX, você precisa usar a sintaxe `{/* */}` para encapsular o texto do seu comentário.

# --instructions--

O editor tem um elemento JSX similar ao que você criou no desafio passado. Adicione um comentário em algum lugar dentro do elemento por tag `div` que está disponível, sem modificar os elementos `h1` e `p` já existentes.

# --hints--

A constante `JSX` deve retornar uma `div`.

```js
assert(JSX.type === 'div');
```

A `div` deve conter um `h1` como seu primeiro elemento.

```js
assert(JSX.props.children[0].type === 'h1');
```

A `div` deve conter um `p` como seu segundo elemento.

```js
assert(JSX.props.children[1].type === 'p');
```

O `h1` e o `p` existente não devem ser alterados.

```js
assert(
  JSX.props.children[0].props.children === 'This is a block of JSX' &&
    JSX.props.children[1].props.children === "Here's a subtitle"
);
```

O `JSX` deve ter um comentário válido seguindo a sintáxe esperada.

```js
assert(/<div>[\s\S]*{\s*\/\*[\s\S]*\*\/\s*}[\s\S]*<\/div>/.test(code));
```

# --seed--

## --after-user-code--

```jsx
ReactDOM.render(JSX, document.getElementById('root'))
```

## --seed-contents--

```jsx
const JSX = (
  <div>
    <h1>This is a block of JSX</h1>
    <p>Here's a subtitle</p>
  </div>
);
```

# --solutions--

```jsx
const JSX = (
<div>
  <h1>This is a block of JSX</h1>
  { /* this is a JSX comment */ }
  <p>Here's a subtitle</p>
</div>);
```
