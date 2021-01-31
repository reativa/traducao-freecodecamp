---
id: 5a24c314108439a4d4036163
title: Criando um componente React
challengeType: 6
forumTopicId: 301386
dashedName: create-a-react-component
---

# --description--

A outra forma de criar um componente React é com a sintaxe de classe do ES6(com a palavra reservada `class`). No exemplo a seguir, o componente ``Kitten` extende a classe `Component` de dentro do React.

```jsx
class Kitten extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return <h1>Hi</h1>;
  }
}
```

Isso irá criar uma classe usando a sintaxe de classes do ES6, essa classe terá o nome `Kitten`, e ela extenderá a classe `Component` do React(ou `React.Component` em outras palavras). Por causa disso a classe `Kitten` agora tem acesso a muitas funcionalidades úteis do React, como estado local e hooks de ciclo de vida. Não se preocupe se você ainda não é tão familiar com estes termos, eles serão vistos com mais detalhes em desafios futuros. Perceba também que a classe `Kitten` tem um método `constructor` definido dentro dela, este método por sua vez chama o método `super()`. O método `super` é usado para chamar o construtor da classe pai, que neste caso é a classe `Component` do React. O construtor é um método especial usado na inicialização de objetos que são criados com a palavra chave `class`. É uma boa prática chamar o construtor de um componente com o método `super` e passar as `props` para ambos. Isso garante que o componente foi inicializado corretamente. Logo você verá outros usos para o construtor(como as props por exemplo).

# --instructions--

`MyComponent` é definido usando uma sintaxe de classe. Termine de escrever o método `render` e então ele retornará uma `div` que contém um `h1` com o texto `Hello React!`.

# --hints--

O componente deve retornar um elemento com a tag `div`.

```js
assert(Enzyme.shallow(React.createElement(MyComponent)).type() === "div");
```

A `div` retornada deve ter um `h1` dentro dela.

```js
assert(/<div><h1>.*<\/h1><\/div>/.test(Enzyme.shallow(React.createElement(MyComponent)).html()));
```

O `h1` por sua vez deve conter o texto `Hello React!`.

```js
assert(
  Enzyme.shallow(React.createElement(MyComponent)).html() === "<div><h1>Hello React!</h1></div>"
);
```

# --seed--

## --after-user-code--

```jsx
ReactDOM.render(<MyComponent />, document.getElementById("root"));
```

## --seed-contents--

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    // Change code below this line
    // Change code above this line
  }
}
```

# --solutions--

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    // Change code below this line
    return (
      <div>
        <h1>Hello React!</h1>
      </div>
    );
    // Change code above this line
  }
}
```
