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

Existem diversas formas de daltonismo. Eles podem variar de uma sensibilidade reduzida à um certo comprimento de onda de luz até a incapacidade de ver as cores. A forma mais comum é a sensibilidade reduzida para detectar verdes.

Por exemplo, se duas cores verdes similares são o primeiro plano e o plano de fundo do seu conteúdo, o usuário com daltonismo pode não ser capaz de distingui-las. Cores próximas podem consideradas vizinhas na Roda de Cores, e essas combinações devem ser evitadas ao transmitir informações importantes.

**Nota:** Algumas ferramentas de seleção de cores incluem simulações visuais de como as cores aparecem para diferentes tipos de daltonismo. Esses são excelentes recursos além das calculadoras online de verificação de contraste.

# --instructions--

O Camper Cat está testando diferentes estilos para um botão importantes, mas o `background-color` amarelo (`#FFFF33`) e o texto com a propriedade `color` verde (`#33FF33`) são tons vizinhos na roda de cores e virtualmente indistinguíveis para alguns usuários com daltonismo. Suas luminosidades também falham na verificação da taxa de contraste. Mude o a propriedade `color` do texto para azul escuro (`#003366`) para resolver ambos os problemas.


# --hints--

Seu código deve mudar a cor do texto do botão para azul escuro.

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
    <h1>Danger!</h1>
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
    <h1>Danger!</h1>
  </header>
  <button>Delete Internet</button>
</body>
```
