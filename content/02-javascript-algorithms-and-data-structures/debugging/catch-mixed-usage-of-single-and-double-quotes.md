---
id: 587d7b84367417b2b2512b37
title: Capturar Uso Misto de Aspas Simples e Duplas
challengeType: 1
forumTopicId: 301188
dashedName: catch-mixed-usage-of-single-and-double-quotes
---

# --description--

JavaScript permite o uso de aspas simples (`'`) e duplas (`"`) para declarar uma string. A decisão de qual usar geralmente se resume à preferência pessoal, com algumas exceções.

Ter duas opções é ótimo quando uma string tem contrações ou outro pedaço de texto entre aspas. Apenas tome cuidado para não fechar a string muito cedo, o que causa um erro de sintaxe.

Aqui estão alguns exemplos de mixagem de aspas:

```js
// These are correct:
const grouchoContraction = "I've had a perfectly wonderful evening, but this wasn't it.";
const quoteInString = "Groucho Marx once said 'Quote me as saying I was mis-quoted.'";
// This is incorrect:
const uhOhGroucho = 'I've had a perfectly wonderful evening, but this wasn't it.';
```

Claro, não há problema em usar apenas um estilo de aspas. Você pode escapar das aspas dentro da string usando o caractere de escape da barra invertida (<code> \\ </code>):

```js
// Correct use of same quotes:
const allSameQuotes = 'I\'ve had a perfectly wonderful evening, but this wasn\'t it.';
```

# --instructions--

Corrija a string para que use aspas diferentes para o valor `href` ou escape das existentes. Mantenha as aspas duplas em toda a string.

# --hints--

Seu código deve corrigir as aspas em torno do valor `href` "#Home" alterando-as ou escapando-as.

```js
assert(code.match(/<a href=\s*?('|\\")#Home\1\s*?>/g));
```

Seu código deve manter as aspas duplas ao redor de toda a string.

```js
assert(code.match(/"<p>.*?<\/p>";/g));
```

# --seed--

## --seed-contents--

```js
let innerHtml = "<p>Click here to <a href="#Home">return home</a></p>";
console.log(innerHtml);
```

# --solutions--

```js
let innerHtml = "<p>Click here to <a href=\"#Home\">return home</a></p>";
console.log(innerHtml);
```
