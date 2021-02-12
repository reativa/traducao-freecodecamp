---
id: bad87fee1348bd9aedf08829
title: Crie um Campo de Texto
challengeType: 0
videoUrl: 'https://scrimba.com/p/pVMPUv/c2EVnf6'
forumTopicId: 16823
dashedName: create-a-text-field
---

# --description--

Agora vamos criar um formulário web.

Os elementos `input` são uma maneira conveniente de obter informações do seu usuário.

Você pode criar uma entrada de texto como esta:

`<input type="text">`

Observe que os elementos `input` se fecham sozinhos

# --instructions--

Crie um elemento `input` do tipo `text` abaixo de suas listas.

# --hints--

Seu aplicativo deve ter um elemento `input` do tipo `text`.

```js
assert($('input[type=text]').length > 0);
```

# --seed--

## --seed-contents--

```html
<h2>CatPhotoApp</h2>
<main>
  <p>Click here to view more <a href="#">cat photos</a>.</p>

  <a href="#"><img src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back."></a>

  <p>Things cats love:</p>
  <ul>
    <li>cat nip</li>
    <li>laser pointers</li>
    <li>lasagna</li>
  </ul>
  <p>Top 3 things cats hate:</p>
  <ol>
    <li>flea treatment</li>
    <li>thunder</li>
    <li>other cats</li>
  </ol>


</main>
```

# --solutions--

```html
<h2>CatPhotoApp</h2>
<main>
  <p>Click here to view more <a href="#">cat photos</a>.</p>

  <a href="#"><img src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back."></a>

  <p>Things cats love:</p>
  <ul>
    <li>cat nip</li>
    <li>laser pointers</li>
    <li>lasagna</li>
  </ul>
  <p>Top 3 things cats hate:</p>
  <ol>
    <li>flea treatment</li>
    <li>thunder</li>
    <li>other cats</li>
  </ol>
  <form>
    <input type="text">
  </form>
</main>
```
