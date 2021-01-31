---
id: 5a24c314108439a4d4036162
title: Criar um componente funcional sem estado
challengeType: 6
forumTopicId: 301392
dashedName: create-a-stateless-functional-component
---

# --description--

Componentes são o coração do React. Tudo no React é um componente e aqui você aprenderá como criar um.

Existem duas formas de se criar um componente do React. A primeira forma é usando uma função do Javascript. Definindo um componente dessa forma você ira criar um *componente funcional sem estado* ou em outras palavras um *stateless functional component*. O conceito de estado em uma aplicação será abordado em desafios futuros. Por enquanto, pense em um componente sem estado/stateless component como um componente que pode receber dados e renderizá-los, mas não gerencia ou rastreia as alterações desses dados. (Nós vamos abordar a segunda forma de se criar um componente React no próximo desafio.)

Para criar um componente com uma função, você simplesmente escreve uma função normal do JavaScript que retorna ou um JSX ou `null`. Uma coisa importante de se notar é que o React requer que sua função começe com uma letra maiúscula. Segue um exemplo abaixo de um componente sem estado que retorna um elemento HTML com JSX:

```jsx
// After being transpiled, the <div> will have a CSS class of 'customClass'
const DemoComponent = function() {
  return (
    <div className='customClass' />
  );
};
```

Por causa que um componente JSX representa HTML, você poderia colocar vários componentes juntos para criar uma página HTML mais complexa. Essa é uma das principais vantagens da arquitetura de componentes que o React provê. Isso permite que você componha sua UI(User interface, que traduzindo é Interface do usuário) de vários componentes separados e isolados. Isso deixa mais fácil a construção e manutenção de interfaces complexas.

# --instructions--

O editor tem uma função chamada `My Component`. Complete esta função de forma que ela retorna uma única `div` que contém algum texto.

**Nota:** O texto é considerado um filho da `div`, então você não poderá usar uma tag que fecha nela mesma(por exemplo: `<div />`)

# --hints--

`MyComponent` deve retornar JSX.

```js
assert(
  (function () {
    const mockedComponent = Enzyme.mount(React.createElement(MyComponent));
    return mockedComponent.length === 1;
  })()
);
```

`MyComponent` deve retornar um elemento `div`.

```js
assert(
  (function () {
    const mockedComponent = Enzyme.mount(React.createElement(MyComponent));
    return mockedComponent.children().type() === 'div';
  })()
);
```

A `div` deve conter um texto.

```js
assert(
  (function () {
    const mockedComponent = Enzyme.mount(React.createElement(MyComponent));
    return mockedComponent.find('div').text() !== '';
  })()
);
```

# --seed--

## --after-user-code--

```jsx
ReactDOM.render(<MyComponent />, document.getElementById('root'))
```

## --seed-contents--

```jsx
const MyComponent = function() {
  // Change code below this line



  // Change code above this line
}
```

# --solutions--

```jsx
const MyComponent = function() {
  // Change code below this line
  return (
    <div>
      Demo Solution
    </div>
  );
  // Change code above this line
}
```
