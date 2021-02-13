---
id: 587d78a5367417b2b2512ad7
title: Use a propriedade 'Linear Gradient' do CSS para criar um elemento listrado.
challengeType: 0
videoUrl: 'https://scrimba.com/c/c6bmQh2'
forumTopicId: 301072
dashedName: use-a-css-linear-gradient-to-create-a-striped-element
---

# --description--

A função `repeating-linear-gradient()` é muito similar a função `linear-gradient()` com a principal diferença que essa repete o gradiente especificado em um padrão. `repeating-linear-gradient()` aceita uma variedade de valores mas, para simplificar, voce irá trabalhar com um valor angular e de parada de cor nesse desafio.

O valor angular é a direção do gradiente. O valor de parada de cor é como um valor de largura (width) que marca onde a transição será feita, e são dadas em porcentagem ou número de pixels.

No exemplo demonstrado no editor de código, o gradiente começa com a cor 'amarelo' (`yellow`) na posição de 0 pixels, se mistura com a segunda cor 'azul' (`blue`) e termina em  40 pixels depois do início. Como a segunda cor termina em 40 pixels, o gradiente imediatamente muda para a terceira cor 'verde' (`green`), e essa cor se mistura com a quarta cor 'vermelho' (`red`) e termina a 80 pixels de distância do início do gradiente. 

Para esse exemplo, ajuda pensar nas paradas de cores como pares onde cada duas cores se misturam.

`0px [amarelo -- mistura -- azul] 40px [verde -- mistura -- vermelho] 80px`

Se o valor de parada de cor da dupla for a mesma cor, a mistura não fica visivel porque são as mesmas cores, seguindo para uma transição forte para a próxima cor, então você tera listras.

# --instructions--

Faça listras mudando a função `repeating-linear-gradient()` para criar um gradiente com angulo de 45 graus (`45deg`), entao defina as primeiras duas paradas de cores para amarelo (`yellow`), então mude as próximas duas paradas de cores para preto (`black`).

# --hints--

O angulo da função `repeating-linear-gradient()` deve ser de 45 graus (45deg). 

```js
assert(code.match(/background:\s*?repeating-linear-gradient\(\s*?45deg/gi));
```

O angulo da função `repeating-linear-gradient()` não deve ser 90 graus (90deg).

```js
assert(!code.match(/90deg/gi));
```

A parada de cor na posição de 0 pixels deve ser amarela (`yellow`).

```js
assert(code.match(/yellow\s+?0(px)?/gi));
```

A primeira parada de cor na posição de 40 pixels deve ser amarela (`yellow`).

```js
assert(code.match(/yellow\s+?40px/gi));
```

A segunda parada de cor na posição de 40 pixels deve ser preta (`black`).

```js
assert(code.match(/yellow\s+?40px,\s*?black\s+?40px/gi));
```

A ultima parada de cor na posição de 80 pixels deve ser preta (`black`).

```js
assert(code.match(/black\s+?80px/gi));
```

# --seed--

## --seed-contents--

```html
<style>

  div{
    border-radius: 20px;
    width: 70%;
    height: 400px;
    margin:  50 auto;
    background: repeating-linear-gradient(
      90deg,
      yellow 0px,
      blue 40px,
      green 40px,
      red 80px
    );
  }

</style>

<div></div>
```

# --solutions--

```html
<style>
  div{
    border-radius: 20px;
    width: 70%;
    height: 400px;
    margin:  50 auto;
    background: repeating-linear-gradient(
      45deg,
      yellow 0px,
      yellow 40px,
      black 40px,
      black 80px
    );
  }
</style>
<div></div>
```
