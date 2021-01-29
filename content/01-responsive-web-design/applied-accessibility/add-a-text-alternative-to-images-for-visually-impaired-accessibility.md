---
id: 587d774c367417b2b2512a9c
title: Add a Text Alternative to Images for Visually Impaired Accessibility
challengeType: 0
videoUrl: 'https://scrimba.com/c/cPp7VfD'
forumTopicId: 16628
dashedName: add-a-text-alternative-to-images-for-visually-impaired-accessibility
---

# --description--

É provável que você tenha visto um atributo `alt` em uma tag `img` em outros desafios. O texto `alt` descreve o conteúdo da imagem e fornece uma alternativa em texto para ela. Isso ajuda nos casos em que a imagem falha ao carregar ou não pode ser vista pelo usuário. Também é usado por mecanismos de pesquisa para entender o que uma imagem contém e incluí-la nos resultados da pesquisa. Aqui está um exemplo:

`<img src="importantLogo.jpeg" alt="Company logo">`

Pessoas com deficiência visual contam com leitores de tela para converter o conteúdo da web em uma interface de áudio. Eles não receberão informações se forem apresentadas apenas visualmente. Para imagens, os leitores de tela podem acessar o atributo `alt` e ler seu conteúdo para fornecer informações importantes.

Um bom texto `alt` fornece ao leitor uma breve descrição da imagem. Você deve sempre incluir um atributo `alt` em sua imagem. De acordo com a especificação do HTML5, isso agora é considerado obrigatório.

# --instructions--


Acontece que Camper Cat é um ninja do código e um ninja de verdade, que está construindo um site para compartilhar seus conhecimentos. A foto do perfil que ele deseja usar mostra suas habilidades e deve ser apreciada por todos os visitantes do site. Adicione um atributo `alt` na tag` img`, que explica que Camper Cat está fazendo caratê. (A imagem `src` não tem um link real, então você deve ver o texto `alt` no display.)

# --hints--

Sua  tag `img` deve ter um atributo `alt` e ele não deve estar vazio.

```js
assert($('img').attr('alt'));
```

# --seed--

## --seed-contents--

```html
<img src="doingKarateWow.jpeg">
```

# --solutions--

```html
<img src="doingKarateWow.jpeg" alt="Someone doing karate">
```
