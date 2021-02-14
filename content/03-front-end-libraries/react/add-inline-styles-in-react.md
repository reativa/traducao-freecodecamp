---
id: 5a24c314108439a4d4036182
title: Adicione estilos in-line com React
challengeType: 6
forumTopicId: 301378
dashedName: add-inline-styles-in-react
---

# --description--

Você deve ter notado que no último desafio havia várias sintaxes diferentes, partindo de estilos in-line com HTML e o atributo `style` até pra um objeto do JavaScript. Primeiro, os nomes de certas propriedades CSS usam camel case. Por exemplo, o último desafio seta o tamanho da fonte com a propriedade `fontSize` ao invés de `font-size`. Palavras com hífen como `font-size` são inválidas na sintaxe de objetos JavaScript, então o React usa camel case. Como uma regra, qualquer propriedade CSS com hífen em seu nome é escrita com camel case dentro do JSX.

Todas propriedades que contém um valor de unidade (como `height`, `width`, e `fontSize`) são supostas para ser em `px` a não ser que outra unidade seja especificada. Se você quer usar `em` por exemplo, basta encapsular o valor e a unidade entre aspas, como `{ fontSize: "4em" }`. Além de propriedades de tamanho que são por padrão em `px`, todas outras propriedades que esperam um valor devem ser contidas entre aspas.

# --instructions--

Se você tem uma grande quantidade de estilos, você pode atribuir o `object` de estilos a uma constante, para assim, manter seu código mais organizado. Inicialize uma constante `styles` e atribua a ela um `object` com três propriedades de estilo a seus respectivos valores. Dê à `div` um cor `"purple"`, um `font-size` de `40` e uma borda de `"2px solid purple"`. Então atribua o objeto `style` para o atributo `style` do elemento no JSX.

# --hints--

A variável `styles` deve ser um objeto(`object`) com três propriedades.

```js
assert(Object.keys(styles).length === 3);
```

A variável `styles` deve tem uma propriedade `color` com o valor de `purple`.

```js
assert(styles.color === 'purple');
```

A variável `styles` deve tem uma propriedade `fontSize` com o valor `40`.

```js
assert(styles.fontSize === 40);
```

A variável `styles` deve ter uma propriedade `border` com o valor de `2px solid purple`

```js
assert(styles.border === '2px solid purple');
```

O componente deve renderizar uma `div`.

```js
assert(
  (function () {
    const mockedComponent = Enzyme.shallow(React.createElement(Colorful));
    return mockedComponent.type() === 'div';
  })()
);
```

A `div` retornada deve ter seu estilo definido com o objeto `styles`.

```js
assert(
  (function () {
    const mockedComponent = Enzyme.shallow(React.createElement(Colorful));
    return (
      mockedComponent.props().style.color === 'purple' &&
      mockedComponent.props().style.fontSize === 40 &&
      mockedComponent.props().style.border === '2px solid purple'
    );
  })()
);
```

# --seed--

## --after-user-code--

```jsx
ReactDOM.render(<Colorful />, document.getElementById('root'))
```

## --seed-contents--

```jsx
// Change code above this line
class Colorful extends React.Component {
  render() {
    // Change code below this line
    return (
      <div style={{color: "yellow", fontSize: 24}}>Style Me!</div>
    );
    // Change code above this line
  }
};
```

# --solutions--

```jsx
const styles = {
  color: "purple",
  fontSize: 40,
  border: "2px solid purple"
};
// Change code above this line
class Colorful extends React.Component {
  render() {
    // Change code below this line
    return (
      <div style={styles}>Style Me!</div>
    );
    // Change code above this line
  }
};
```
