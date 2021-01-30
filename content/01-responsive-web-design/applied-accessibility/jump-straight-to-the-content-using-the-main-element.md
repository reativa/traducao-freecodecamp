---
id: 587d774e367417b2b2512a9f
title: Jump Straight to the Content Using the main Element
challengeType: 0
videoUrl: 'https://scrimba.com/c/cPp7zuE'
forumTopicId: 301018
dashedName: jump-straight-to-the-content-using-the-main-element
---

# --description--

O HTML5 introduziu uma série de novos elementos que fornecem aos desenvolvedores mais opções, ao mesmo tempo que incorporam recursos de acessibilidade. Essas tags incluem `main`,` header`, `footer`,` nav`, `article` e` section`, entre outros.

Por padrão, um navegador renderiza esses elementos de maneira semelhante a humilde `div`. No entanto, usá-los quando apropriado fornece um significado adicional à sua marcação. O nome da tag sozinha pode indicar o tipo de informação que ela contém, o que adiciona significado semântico a esse conteúdo. As tecnologias assistivas podem acessar essas informações para fornecer um melhor resumo da página ou opções de navegação para seus usuários.

O elemento `main` é usado para envolver (você adivinhou) o conteúdo principal, e deve haver apenas um por página. O objetivo é envolver as informações relacionadas ao tópico central da sua página. Não se destina a incluir itens que se repetem nas páginas, como links de navegação ou banners.

A tag `main` também possui um recurso de referência incorporado que a tecnologia de assistência pode usar para navegar rapidamente até o conteúdo principal. Se você já viu um link "Ir para o conteúdo principal" no topo de uma página, o uso de uma tag principal fornece automaticamente essa funcionalidade aos dispositivos assistentes.

# --instructions--

O Camper Cat tem grandes ideias para sua página de armas ninja. Ajude-o a configurar sua marcação adicionando tags de abertura e fechamento `main` entre o` header` e `footer` (cobertos em outros desafios). Mantenha as tags `main` vazias por enquanto.

# --hints--

Seu código deve ter uma tag `main`.

```js
assert($('main').length == 1);
```

As tags `main` devem estar entre a tag de fechamento` header` e a tag de abertura `footer`.

```js
assert(code.match(/<\/header>\s*?<main>\s*?<\/main>/gi));
```

# --seed--

## --seed-contents--

```html
<header>
  <h1>Weapons of the Ninja</h1>
</header>



<footer></footer>
```

# --solutions--

```html
<header>
  <h1>Weapons of the Ninja</h1>
</header>
<main>

</main>
<footer></footer>
```
