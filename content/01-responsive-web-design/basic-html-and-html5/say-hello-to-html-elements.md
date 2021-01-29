---
id: bd7123c8c441eddfaeb5bdef
title: Say Hello to HTML Elements
challengeType: 0
videoUrl: 'https://scrimba.com/p/pVMPUv/cE8Gpt2'
forumTopicId: 18276
dashedName: say-hello-to-html-elements
---

# --description--

Bem-vindo aos desafios de codificação HTML do freeCodeCamp. Eles o guiarão pelo desenvolvimento da Web passo a passo.

Primeiro, você começará construindo uma página da web simples usando HTML. Você pode editar o código em seu editor de código, que está embutido nesta página da web.

Você vê o código em seu editor de código que diz `<h1>Hello</h1>`? Esse é um elemento html.

A maioria dos elementos HTML tem uma tag de abertura e uma tag de fechamento.

As tags de abertura são assim:

`<h1>`

Tags de fechamento se parecem com isto:

`</h1>`

A única diferença entre abrir e fechar as tags é a barra após o colchete de abertura de uma tag de fechamento.

Cada desafio possui testes que você pode executar a qualquer momento clicando no botão "Executar testes". Quando você passar em todos os testes, será solicitado a enviar sua solução e passar para o próximo desafio de codificação.


# --instructions--

Para passar no teste deste desafio, mude seu texto do elemento `h1` para dizer "Hello World".

# --hints--

Seu elemento `h1` deve ter o texto "Hello World".

```js
assert.isTrue(/hello(\s)+world/gi.test($('h1').text()));
```

# --seed--

## --seed-contents--

```html
<h1>Hello</h1>
```

# --solutions--

```html
<h1>Hello World</h1>
```
