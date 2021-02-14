---
id: bad87fee1348bd9aedf08816
title: Link para páginas externas com elementos âncora
challengeType: 0
videoUrl: 'https://scrimba.com/p/pVMPUv/c8EkncB'
forumTopicId: 18226
dashedName: link-to-external-pages-with-anchor-elements
---

# --description--

Você pode usar elementos `a` (*âncora*) para criar um link para conteúdos fora de sua página web.

Os elementos `a` precisam de um endereço web de destino, chamado de atributo `href`. Eles também precisam de texto âncora. Aqui está um exemplo:

`<a href="https://freecodecamp.org">this links to freecodecamp.org</a>`

Então o seu navegador exibirá o texto `this links to freecodecamp.org` como um link em que você pode clicar. E esse link o levará ao endereço web `https://www.freecodecamp.org`.

# --instructions--

Crie um elemento `a` vinculado a `https://freecatphotoapp.com` e que tenha "fotos de gatos" como texto âncora.

# --hints--

Seu elemento `a` deve ter o texto âncora de "fotos de gatos ".

```js
assert(/cat photos/gi.test($('a').text()));
```

Você precisa de um elemento `a` vinculado a `https://freecatphotoapp.com`

```js
assert(/https:\/\/(www\.)?freecatphotoapp\.com/gi.test($('a').attr('href')));
```

Seu elemento `a` deve possuir uma tag de fechamento.

```js
assert(
  code.match(/<\/a>/g) &&
    code.match(/<\/a>/g).length === code.match(/<a/g).length
);
```

# --seed--

## --seed-contents--

```html
<h2>CatPhotoApp</h2>
<main>



  <img src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back.">

  <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
  <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
</main>
```

# --solutions--

```html
<h2>CatPhotoApp</h2>
<main>
  
  <img src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back.">
  
  <a href="https://freecatphotoapp.com">cat photos</a>
  <p>Kitty ipsum dolor sit amet, shed everywhere shed everywhere stretching attack your ankles chase the red dot, hairball run catnip eat the grass sniff.</p>
  <p>Purr jump eat the grass rip the couch scratched sunbathe, shed everywhere rip the couch sleep in the sink fluffy fur catnip scratched.</p>
</main>
```
