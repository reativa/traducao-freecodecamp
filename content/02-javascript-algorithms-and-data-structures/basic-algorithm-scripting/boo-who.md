---
id: a77dbc43c33f39daa4429b4f
title: Boo who
challengeType: 5
forumTopicId: 16000
dashedName: boo-who
---

# --description--

Verifique se um valor é classificado como boleano primitivo. Retorne verdadeiro (true) ou falso (false).

Boleanos primitivos são *true* ou *false*.

# --hints--

`booWho(true)` Devemos retornar true.

```js
assert.strictEqual(booWho(true), true);
```

`booWho(false)` Devemos retornar true.

```js
assert.strictEqual(booWho(false), true);
```

`booWho([1, 2, 3])` Devemos retornar false.

```js
assert.strictEqual(booWho([1, 2, 3]), false);
```

`booWho([].slice)` Devemos retornar false.

```js
assert.strictEqual(booWho([].slice), false);
```

`booWho({ "a": 1 })` Devemos retornar false.

```js
assert.strictEqual(booWho({ a: 1 }), false);
```

`booWho(1)` Devemos retornar false.

```js
assert.strictEqual(booWho(1), false);
```

`booWho(NaN)` Devemos retornar false.

```js
assert.strictEqual(booWho(NaN), false);
```

`booWho("a")` Devemos retornar false.

```js
assert.strictEqual(booWho('a'), false);
```

`booWho("true")` Devemos retornar false.

```js
assert.strictEqual(booWho('true'), false);
```

`booWho("false")` Devemos retornar false.

```js
assert.strictEqual(booWho('false'), false);
```

# --seed--

## --seed-contents--

```js
function booWho(bool) {
  return bool;
}

booWho(null);
```

# --solutions--

```js
function booWho(bool) {
  return typeof bool === "boolean";
}

booWho(null);
```
