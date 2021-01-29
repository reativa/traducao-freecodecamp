---
id: 587d778f367417b2b2512aad
title: >-
  Avoid Colorblindness Issues by Carefully Choosing Colors that Convey
  Information
challengeType: 0
videoUrl: 'https://scrimba.com/c/c437as3'
forumTopicId: 301011
dashedName: >-
  avoid-colorblindness-issues-by-carefully-choosing-colors-that-convey-information
---

# --description--

Existem várias formas de daltonismo. Isso pode variar de uma sensibilidade reduzida a um determinado comprimento de onda de luz até a incapacidade de ver as cores. A forma mais comum é uma sensibilidade reduzida para detectar verdes.

Por exemplo, se duas cores verdes semelhantes são as cores do primeiro e segundo plano do seu conteúdo, um usuário daltônico pode não ser capaz de distingui-las. Cores próximas podem ser consideradas vizinhas na roda de cores e essas combinações devem ser evitadas ao transmitir informações importantes.

**Nota:** Algumas ferramentas de seleção de cores online incluem simulações visuais de como as cores aparecem para diferentes tipos de daltonismo. Esses são ótimos recursos além das calculadoras de verificação de contraste online.

# --instructions--


Camper Cat está testando estilos diferentes para um botão importante, mas o `background-color`  amarelo (`#FFFF33`)e o `color` do texto verde (`# 33FF33`) são matizes vizinhos na roda de cores e virtualmente indistinguíveis para alguns usuários daltônicos. (Sua leve semelhança também falha na verificação da taxa de contraste). Altere o `color` do texto para um azul escuro (`# 003366`) para resolver os dois problemas.

# --hints--

Seu código deve mudar o `color` do texto do `button` para azul-escuro.

```js
assert($('button').css('color') == 'rgb(0, 51, 102)');
```

# --seed--

## --seed-contents--

```html
<head>
  <style>
  button {
    color: #33FF33;
    background-color: #FFFF33;
    font-size: 14px;
    padding: 10px;
  }
  </style>
</head>
<body>
  <header>
    <h1>Perigo!</h1>
  </header>
  <button>Delete Internet</button>
</body>
```

# --solutions--

```html
<head>
  <style>
    button {
      color: #003366;
      background-color: #FFFF33;
      font-size: 14px;
      padding: 10px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Perigo!</h1>
  </header>
  <button>Delete Internet</button>
</body>
```
