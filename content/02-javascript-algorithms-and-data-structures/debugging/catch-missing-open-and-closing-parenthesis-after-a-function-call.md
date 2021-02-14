---
id: 587d7b85367417b2b2512b39
title: Capture a Falta de Parênteses Aberto e Fechado Após Chamada de Função
challengeType: 1
forumTopicId: 301185
dashedName: catch-missing-open-and-closing-parenthesis-after-a-function-call
---

# --description--

Quando uma função ou método não aceita nenhum argumento, você pode esquecer de incluir os parênteses de abertura e fechamento (vazios) ao chamá-lo. Muitas vezes o resultado de uma chamada de função é salvo em uma variável para outro uso em seu código. Esse erro pode ser detectado registrando os valores das variáveis (ou seus tipos) no console e vendo se um deles está definido como uma referência de função, em vez do valor esperado que a função retorna.

As variáveis no exemplo a seguir são diferentes:

```js
function myFunction() {
  return "You rock!";
}
let varOne = myFunction; // set to equal a function
let varTwo = myFunction(); // set to equal the string "You rock!"
```

# --instructions--

Corrija o código para que a variável `result` seja definida como o valor retornado da chamada da função `getNine`.

# --hints--

Seu código deve corrigir a variável `result` para que seja definido como o número que a função `getNine` retorna.

```js
assert(result == 9);
```

Seu código deve chamar a função `getNine`.

```js
assert(code.match(/getNine\(\)/g).length == 2);
```

# --seed--

## --seed-contents--

```js
function getNine() {
  let x = 6;
  let y = 3;
  return x + y;
}

let result = getNine;
console.log(result);
```

# --solutions--

```js
function getNine() {
 let x = 6;
 let y = 3;
 return x + y;
}

let result = getNine();
console.log(result);
```
