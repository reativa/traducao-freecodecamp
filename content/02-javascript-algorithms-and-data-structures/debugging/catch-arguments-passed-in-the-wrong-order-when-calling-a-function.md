---
id: 587d7b85367417b2b2512b3a
title: Pegar argumentos passados na ordem errada ao chamar uma função
challengeType: 1
forumTopicId: 301184
dashedName: catch-arguments-passed-in-the-wrong-order-when-calling-a-function
---

# --description--

Continuando a discussão sobre chamada de funções, o próximo bug a observar é quando os argumentos de uma função são fornecidos na ordem incorreta. Se os argumentos forem de tipos diferentes, como uma função que espera uma matriz e um inteiro, isso provavelmente gerará um erro de tempo de execução. Se os argumentos forem do mesmo tipo (todos inteiros, por exemplo), então a lógica do código não fará sentido. Certifique-se de fornecer todos os argumentos necessários, na ordem adequada para evitar esses problemas.

# --instructions--

A função `raiseToPower` eleva uma base a um expoente. Infelizmente, ela não foi chamada corretamente - corrija o código para que o valor de `power` seja 8, como esperado.

# --hints--

Seu código deve corrigir a variável `power` para que seja igual a 2 elevado à 3ª potência, não 3 elevado à 2ª potência.

```js
assert(power == 8);
```
Seu código deve usar a ordem correta dos argumentos para a chamada da função `raiseToPower`.

```js
assert(code.match(/raiseToPower\(\s*?base\s*?,\s*?exp\s*?\);/g));
```

# --seed--

## --seed-contents--

```js
function raiseToPower(b, e) {
  return Math.pow(b, e);
}

let base = 2;
let exp = 3;
let power = raiseToPower(exp, base);
console.log(power);
```

# --solutions--

```js
function raiseToPower(b, e) {
 return Math.pow(b, e);
}

let base = 2;
let exp = 3;
let power = raiseToPower(base, exp);
console.log(power);
```
