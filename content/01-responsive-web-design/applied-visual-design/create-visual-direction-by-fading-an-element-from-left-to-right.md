---
id: 587d78a7367417b2b2512ae2
title: Crie uma direção visual, desvanecendo (fading) um elemento da esquerda para a direita
challengeType: 0
videoUrl: 'https://scrimba.com/c/cGJqqAE'
forumTopicId: 301054
dashedName: create-visual-direction-by-fading-an-element-from-left-to-right
---

# --description--

Para este desafio, você alterará a `opacity` de um elemento animado para que desapareça gradualmente conforme atinge o lado direito da tela.

Na animação exibida, o elemento redondo com o fundo gradiente se move para a direita pela marca de 50% da animação de acordo com a `@keyframes`.

# --instructions--

Direcione o elemento com o id `ball` e adicione a propriedade `opacity` definida como 0,1 em `50%`, para que o elemento desapareça conforme se move para a direita.

# --hints--

Para desvaneçer a `keyframes` deve definir a propriedade `opacity` para 0,1 a 50%.

```js
assert(
  code.match(
    /@keyframes fade\s*?{\s*?50%\s*?{\s*?(?:left:\s*?60%;\s*?opacity:\s*?0?\.1;|opacity:\s*?0?\.1;\s*?left:\s*?60%;)/gi
  )
);
```

# --seed--

## --seed-contents--

```html
<style>

  #ball {
    width: 70px;
    height: 70px;
    margin: 50px auto;
    position: fixed;
    left: 20%;
    border-radius: 50%;
    background: linear-gradient(
      35deg,
      #ccffff,
      #ffcccc
    );
    animation-name: fade;
    animation-duration: 3s;
  }

  @keyframes fade {
    50% {
      left: 60%;

    }
  }

</style>

<div id="ball"></div>
```

# --solutions--

```html
<style>
  #ball {
    width: 70px;
    height: 70px;
    margin: 50px auto;
    position: fixed;
    left: 20%;
    border-radius: 50%;
    background: linear-gradient(
      35deg,
      #ccffff,
      #ffcccc
    );
    animation-name: fade;
    animation-duration: 3s;
  }

  @keyframes fade {
    50% {
      left: 60%;
      opacity: 0.1;
    }
  }
</style>
<div id="ball"></div>
```
