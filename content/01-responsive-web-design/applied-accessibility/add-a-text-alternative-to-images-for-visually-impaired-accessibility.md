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

People with visual impairments rely on screen readers to convert web content to an audio interface. They won't get information if it's only presented visually. For images, screen readers can access the `alt` attribute and read its contents to deliver key information.

Good `alt` text provides the reader a brief description of the image. You should always include an `alt` attribute on your image. Per HTML5 specification, this is now considered mandatory.

# --instructions--

Camper Cat happens to be both a coding ninja and an actual ninja, who is building a website to share his knowledge. The profile picture he wants to use shows his skills and should be appreciated by all site visitors. Add an `alt` attribute in the `img` tag, that explains Camper Cat is doing karate. (The image `src` doesn't link to an actual file, so you should see the `alt` text in the display.)

# --hints--

Your `img` tag should have an `alt` attribute and it should not be empty.

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
