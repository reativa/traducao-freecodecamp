---
id: 587d78b0367417b2b2512b08
title: Create a Media Query
challengeType: 0
videoUrl: 'https://scrimba.com/p/pzrPu4/cqwKrtm'
forumTopicId: 301139
dashedName: create-a-media-query
---

# --description--

Media Queries são uma nova técnica introduzida no CSS3 que altera a apresentação do conteúdo baseando-se nas diferentes dimensões da janela de exibição (viewport). A janela de exibição é a área vísivel para o usuário de uma página web, e é diferente dependendo do dispositivo utilizado para acessar o site.

Media Queries consistem em media types, e se esse determinado media type corresponde ao dispositivo que está exibindo o documento, os estilos são aplicados. Você pode ter quantos seletores e estilos quiser dentro de sua media query.

Aqui está um exemplo de media query que retorna o conteúdo quando a largura do dispositivo é menor ou igual a 100px:

`@media (max-width: 100px) { /* Regras de CSS */ }`

e a seguinte media query retorna o conteúdo quando a altura do dispositivo é maior ou igual a 350px:

`@media (min-height: 350px) { /* Regras de CSS */ }`

Lembre-se, o CSS dentro da media query é aplicado somente quando a media corresponde com o dispositivo que está sendo usado.

# --instructions--

Adicione uma media query, então a tag `p` tem `font-size` de `10px`quando a altura do dispositivo for menos ou igual a `800px`.

# --hints--

Você deve declarar `@media` query para dispositivos com `height`menor ou igual a 800px.

```js
assert(
  $('style')
    .text()
    .replace(/\s/g, '')
    .match(/@media\(max-height:800px\)/g)
);
```

Seu elemento `p` deve ter `font-size` de 10px quando o `height`do dispositivo for menor ou igual a 800px. 


```js
assert(
  $('style')
    .text()
    .replace(/\s/g, '')
    .match(/@media\(max-height:800px\){p{font-size:10px;?}}/g)
);
```
Seu elemento `p` deve ter `font-size` inicial de 20px quando o `height`do dispositivo for maior que 800px. 

```js
assert(
  $('style')
    .text()
    .replace(/\s/g, '')
    .replace(/@media.*}/g, '')
    .match(/p{font-size:20px;?}/g)
);
```

# --seed--

## --seed-contents--

```html
<style>
  p {
    font-size: 20px;
  }

  /* Somente altere o código abaixo dessa linha*/

  /* Somente altere o código acima dessa linha */
</style>

<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus quis tempus massa. Aenean erat nisl, gravida vel vestibulum cursus, interdum sit amet lectus. Sed sit amet quam nibh. Suspendisse quis tincidunt nulla. In hac habitasse platea dictumst. Ut sit amet pretium nisl. Vivamus vel mi sem. Aenean sit amet consectetur sem. Suspendisse pretium, purus et gravida consequat, nunc ligula ultricies diam, at aliquet velit libero a dui.</p>
```

# --solutions--

```html
<style>
  p {
    font-size: 20px;
  }

  @media (max-height: 800px) {
    p {
      font-size: 10px;
    }
  }
</style>

<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus quis tempus massa. Aenean erat nisl, gravida vel vestibulum cursus, interdum sit amet lectus. Sed sit amet quam nibh. Suspendisse quis tincidunt nulla. In hac habitasse platea dictumst. Ut sit amet pretium nisl. Vivamus vel mi sem. Aenean sit amet consectetur sem. Suspendisse pretium, purus et gravida consequat, nunc ligula ultricies diam, at aliquet velit libero a dui.</p>
```
