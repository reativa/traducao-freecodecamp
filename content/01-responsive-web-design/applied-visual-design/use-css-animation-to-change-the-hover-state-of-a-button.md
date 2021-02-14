---
id: 587d78a7367417b2b2512ae0
title: Use uma animação em CSS (CSS animation) para mudar o estado "Hover" de um botão.
challengeType: 0
videoUrl: 'https://scrimba.com/c/cg4vZAa'
forumTopicId: 301073
dashedName: use-css-animation-to-change-the-hover-state-of-a-button
---

# --description--

Você pode usar  o `@keyframes` do CSS para mudar a cor de um botão que esta em um estado "hover".

Aqui está um exempço de como mudar a largura de uma imagem com o "hover":

```html
<style>
  img:hover {
    animation-name: width;
    animation-duration: 500ms;
  }

  @keyframes width {
    100% {
      width: 40px;
    }
  }
</style>

<img src="https://bit.ly/smallgooglelogo" alt="Google's Logo" />
```

# --instructions--

Note que `ms` quer dizer milissegundos, onde 1000ms é igual a 1s.

Use o `@keyframes` do CSS para mudar a propriedade `background-color` do elemento `button` para se tornar `#4791d0` quando o usuário estiver com o mouse sobre ele (hover). O `@keyframes` deve ter apenas uma entrada para o estado de `100%`.

# --hints--

O @keyframes deve usar a propriedade `animation-name` como "background-color".

```js
assert(code.match(/@keyframes\s+?background-color\s*?{/g));
```

Deve haver uma entrade no `@keyframes` que muda a propriedade `background-color` para `#4791d0` no estado de 100%.

```js
assert(code.match(/100%\s*?{\s*?background-color:\s*?#4791d0;\s*?}/gi));
```

# --seed--

## --seed-contents--

```html
<style>
  button {
    border-radius: 5px;
    color: white;
    background-color: #0F5897;
    padding: 5px 10px 8px 10px;
  }

  button:hover {
    animation-name: background-color;
    animation-duration: 500ms;
  }


</style>

<button>Register</button>
```

# --solutions--

```html
<style>
  button {
    border-radius: 5px;
    color: white;
    background-color: #0F5897;
    padding: 5px 10px 8px 10px;
  }

  button:hover {
    animation-name: background-color;
    animation-duration: 500ms;
  }

  @keyframes background-color {
    100% {
      background-color: #4791d0;
    }
  }
</style>
<button>Register</button>
```
