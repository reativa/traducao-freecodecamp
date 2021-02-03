---
id: 587d7789367417b2b2512aa4
title: Improve Accessibility of Audio Content with the audio Element
challengeType: 0
videoUrl: 'https://scrimba.com/c/cVJVkcZ'
forumTopicId: 301014
dashedName: improve-accessibility-of-audio-content-with-the-audio-element
---

# --description--

O elemento `audio` do HTML5 fornece significado semântico quando envolve o som ou o conteúdo do stream de áudio em sua marcação. O conteúdo de áudio também precisa de uma alternativa em texto para ser acessível a pessoas surdas ou com deficiência auditiva. Isso pode ser feito com um texto próximo na página ou um link para uma transcrição.

A tag `audio` suporta o atributo` controls`. Ele mostra o play, o pause e controles padrão do navegador além de oferecer suporte à funcionalidades do teclado. Este é um atributo booleano, o que significa que não precisa de um valor, sua presença na tag ativa a configuração.

Aqui está um exemplo:

```html
<audio id="meowClip" controls>
  <source src="audio/meow.mp3" type="audio/mpeg" />
  <source src="audio/meow.ogg" type="audio/ogg" />
</audio>
```

**Nota:** O conteúdo multimídia geralmente tem componentes visuais e auditivos. Ele precisa de legendas sincronizadas e uma transcrição para que usuários com deficiência visual e / ou auditiva possam acessá-lo. Geralmente, um desenvolvedor da Web não é responsável por criar as legendas ou transcrições, mas precisa saber como incluí-las.

# --instructions--

É hora de fazer uma pausa no Camper Cat e conhecer o colega campista Zersiax (@zersiax), um campeão de acessibilidade e usuário de leitor de tela. Para ouvir um clipe de seu leitor de tela em ação, adicione um elemento `audio` após o` p`. Incluindo o atributo `controls`. Em seguida, coloque uma tag `source` dentro das tags `audio` com o atributo `src` definido como " `https: // s3.amazonaws.com / freecodecamp / screen-reader.mp3`" e o atributo `type` definido como" audio / mpeg ".

**Note:** O clipe de áudio pode parecer rápido e difícil de entender, mas essa é uma velocidade normal para usuários de leitores de tela.

# --hints--

Seu código deve ter uma tag `audio`.

```js
assert($('audio').length === 1);
```

Seu elemento `audio` deve ter uma tag de fechamento.

```js
assert(
  code.match(/<\/audio>/g).length === 1 &&
    code.match(/<audio.*>[\s\S]*<\/audio>/g)
);
```

A tag `audio` deve ter o atributo` controls`.
```js
assert($('audio').attr('controls'));
```

Seu código deve ter uma tag `source`.
```js
assert($('source').length === 1);
```

Sua tag `source` deve estar dentro das tags` audio`.

```js
assert($('audio').children('source').length === 1);
```

O valor do atributo `src` na tag` source` deve corresponder exatamente ao link nas instruções.

```js
assert(
  $('source').attr('src') ===
    'https://s3.amazonaws.com/freecodecamp/screen-reader.mp3'
);
```

Seu código deve incluir um atributo `type` na tag` source` com um valor de audio / mpeg.

```js
assert($('source').attr('type') === 'audio/mpeg');
```

# --seed--

## --seed-contents--

```html
<body>
  <header>
    <h1>Real Coding Ninjas</h1>
  </header>
  <main>
    <p>A sound clip of Zersiax's screen reader in action.</p>



  </main>
</body>
```

# --solutions--

```html
<body>
  <header>
    <h1>Real Coding Ninjas</h1>
  </header>
  <main>
    <p>A sound clip of Zersiax's screen reader in action.</p>
    <audio controls>
      <source src="https://s3.amazonaws.com/freecodecamp/screen-reader.mp3" type="audio/mpeg"/>
    </audio>
  </main>
</body>
```
