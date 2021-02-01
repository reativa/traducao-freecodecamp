---
id: 5a24c314108439a4d4036164
title: Crie um componente com composição
challengeType: 6
forumTopicId: 301383
dashedName: create-a-component-with-composition
---

# --description--

Agora veremos como nós podemos compor múltiplos componentes React juntos. Imagine que você está construindo um App e criou três componentes, uma `Navbar`, `Dashboard` e um `Footer`.

Para compor esses componentes juntos, você poderia criar um componente *pai* `App` que renderiza cada um desses três componentes como componentes *filhos*. Para renderizar um componente como um componente filho no React, você precisa incluir o nome do componente escrito como uma tag HTML no JSX. Por exemplo, no método `render` você poderia escrever:

```jsx
return (
 <App>
  <Navbar />
  <Dashboard />
  <Footer />
 </App>
)
```

Quando o React encontra uma tag HTML personalizada que faz referência a outro componente (que está encapsulado em `< />` como neste exemplo), ele renderiza as marcações daquele componente no lugar da tag. Isso deveria ilustrar a relação de pai e filho entre o componente `App` e os componentes `Navbar`, `Dashboard` e `Footer`.

# --instructions--

No editor, há um simples componente em forma de função chamado `ChildComponent` e um componente em forma de classe chamado `ParentComponent`. Componha os dois componentes juntos ao renderizar o `ChildComponent` dentro do `ParentComponent`. Se certifique de fechar a tag do `ChildComponent` com uma `/>`, por exemplo: `<ChildComponent />`.

**Note:** `ChildComponent` está definido com uma arrow function do ES6, essa é uma prática muito comum no React. Todavia, saiba que isso é somente uma função. Se você não é familiar com essa sintáxe de arrow function, veja a seção de Javascript.

# --hints--

O componente deve retornar um único elemento, que é uma `div`.

```js
assert(
  (function () {
    var shallowRender = Enzyme.shallow(React.createElement(ParentComponent));
    return shallowRender.type() === 'div';
  })()
);
```

O componente deve retornar dois elementos aninhados.

```js
assert(
  (function () {
    var shallowRender = Enzyme.shallow(React.createElement(ParentComponent));
    return shallowRender.children().length === 2;
  })()
);
```

O componente deve retornar o ChildComponent como seu segundo filho.

```js
assert(
  (function () {
    const mockedComponent = Enzyme.mount(React.createElement(ParentComponent));
    return (
      mockedComponent.find('ParentComponent').find('ChildComponent').length ===
      1
    );
  })()
);
```

# --seed--

## --after-user-code--

```jsx
ReactDOM.render(<ParentComponent />, document.getElementById('root'))
```

## --seed-contents--

```jsx
const ChildComponent = () => {
  return (
    <div>
      <p>I am the child</p>
    </div>
  );
};

class ParentComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>I am the parent</h1>
        { /* Change code below this line */ }


        { /* Change code above this line */ }
      </div>
    );
  }
};
```

# --solutions--

```jsx
const ChildComponent = () => {
  return (
    <div>
      <p>I am the child</p>
    </div>
  );
};

class ParentComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>I am the parent</h1>
        { /* Change code below this line */ }
        <ChildComponent />
        { /* Change code above this line */ }
      </div>
    );
  }
};
```
