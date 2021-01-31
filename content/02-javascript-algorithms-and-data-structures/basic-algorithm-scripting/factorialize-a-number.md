---
id: a302f7aae1aa3152a5b413bc
title: Fatorialize um número
challengeType: 5
forumTopicId: 16013
dashedName: factorialize-a-number
---

# --description--

Retorne o fatorial do número inteiro fornecido.

Se o número é representado pela letra n, um fatorial é o produto de todos os números positivos menores ou iguais a n.

Fatoriais são geralmente representados com a notação abreviada `n!`

Por exemplo: `5! = 1 * 2 * 3 * 4 * 5 = 120`

Somente inteiros maiores ou iguais a 0 deverão ser passados para a função.


# --hints--

`factorialize(5)` deve retornar um número.

```js
assert(typeof factorialize(5) === 'number');
```

`factorialize(5)` deve retornar 120.

```js
assert(factorialize(5) === 120);
```

`factorialize(10)` deve retornar 3628800.

```js
assert(factorialize(10) === 3628800);
```

`factorialize(20)` deve retornar 2432902008176640000.

```js
assert(factorialize(20) === 2432902008176640000);
```

`factorialize(0)` deve retornar 1.

```js
assert(factorialize(0) === 1);
```

# --seed--

## --seed-contents--

```js
function factorialize(num) {
  return num;
}

factorialize(5);
```

# --solutions--

```js
function factorialize(num) {
  return num < 1 ? 1 : num * factorialize(num - 1);
}

factorialize(5);
```
