---
id: 587d7b84367417b2b2512b35
title: Identificar variáveis e nomes de funções com erros de digitação
challengeType: 1
forumTopicId: 301186
dashedName: catch-misspelled-variable-and-function-names
---

# --description--

Os métodos `console.log()` e `typeof` são as duas principais formas de verificar valores intermediários e tipos de saída do programa. Agora é hora de entrar nas formas comuns que os bugs assumem. Um problema de nível de sintaxe com o qual digitadores rápidos podem lamentar é o humilde erro de ortografia.

Caracteres transpostos, ausentes ou mal capitalizados em uma variável ou nome de função farão com que o navegador procure um objeto que não existe - e reclame na forma de um erro de referência. Os nomes de variáveis e funções em JavaScript diferenciam maiúsculas de minúsculas.

# --instructions--

Corrija os dois erros de digitação no código para que o cálculo `netWorkingCapital` funcione.

# --hints--

Verifique a grafia das duas variáveis usadas no cálculo de netWorkingCapital, a saída do console deve mostrar que "Net working capital is: 2".

```js
assert(netWorkingCapital === 2);
```

Não deve haver instâncias de variáveis com erros de digitação no código.

```js
assert(!code.match(/recievables/g));
```
A variável `receivables` deve ser declarada e usada corretamente no código.

```js
assert(code.match(/receivables/g).length == 2);
```

Não deve haver instâncias de variáveis com erros de digitação no código.

```js
assert(!code.match(/payable;/g));
```
A variável `payables` deve ser declarada e usada corretamente no código.

```js
assert(code.match(/payables/g).length == 2);
```

# --seed--

## --seed-contents--

```js
let receivables = 10;
let payables = 8;
let netWorkingCapital = recievables - payable;
console.log(`Net working capital is: ${netWorkingCapital}`);
```

# --solutions--

```js
let receivables = 10;
let payables = 8;
let netWorkingCapital = receivables - payables;
console.log(`Net working capital is: ${netWorkingCapital}`);
```
