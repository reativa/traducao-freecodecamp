---
id: 587d774c367417b2b2512a9d
title: Know When Alt Text Should be Left Blank
challengeType: 0
videoUrl: 'https://scrimba.com/c/cM9P4t2'
forumTopicId: 301019
dashedName: know-when-alt-text-should-be-left-blank
---

# --description--

No último desafio, você aprendeu que incluir um atributo `alt` ao usar as tags `img` é obrigatório. No entanto, às vezes as imagens são agrupadas com uma legenda que já as descreve ou são usadas apenas para decoração. Nestes casos, o texto `alt` pode parecer redundante ou desnecessário.

Em situações em que uma imagem já é explicada com conteúdo de texto, ou não adiciona significado a uma página, o `img` ainda precisa de um atributo `alt`, mas pode ser definido como uma string vazia. Aqui está um exemplo:

`<img src ="visualDecoration.jpeg" alt ="">`

As imagens de fundo também costumam ser classificadas como "decorativas". No entanto, eles são normalmente aplicados com regras CSS e, portanto, não fazem parte do processo de leitores de tela de marcação.

**Nota:** Para imagens com legenda, você ainda pode querer incluir o texto `alt`, pois ajuda os mecanismos de busca a catalogar o conteúdo da imagem.

# --instructions--

Camper Cat codificou um esqueleto de página para a parte do blog do seu site. Ele está planejando adicionar uma pausa visual entre seus dois artigos com uma imagem decorativa de uma espada de samurai. Adicione um atributo `alt` à tag `img` e defina-o como uma string vazia. (Observe que a imagem `src` não está vinculada a um arquivo real - não se preocupe se não houver espadas aparecendo na tela.)
# --hints--

Sua tag `img` deve ter um atributo `alt`.

```js
assert(!($('img').attr('alt') == undefined));
```
O atributo `alt` deve ser definido como uma string vazia.

```js
assert($('img').attr('alt') == '');
```

# --seed--

## --seed-contents--

```html
<h1>Deep Thoughts with Master Camper Cat</h1>
<article>
  <h2>Defeating your Foe: the Red Dot is Ours!</h2>
  <p>To Come...</p>
</article>

<img src="samuraiSwords.jpeg">

<article>
  <h2>Is Chuck Norris a Cat Person?</h2>
  <p>To Come...</p>
</article>
```

# --solutions--

```html
<h1>Deep Thoughts with Master Camper Cat</h1>
<article>
  <h2>Defeating your Foe: the Red Dot is Ours!</h2>
  <p>To Come...</p>
</article>

<img src="samuraiSwords.jpeg" alt="">

<article>
  <h2>Is Chuck Norris a Cat Person?</h2>
  <p>To Come...</p>
</article>
```
