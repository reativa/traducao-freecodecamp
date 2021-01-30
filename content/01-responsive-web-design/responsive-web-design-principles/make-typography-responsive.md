---
id: 587d78b1367417b2b2512b0c
title: Make Typography Responsive
challengeType: 0
videoUrl: 'https://scrimba.com/p/pzrPu4/crzN7T8'
forumTopicId: 301141
dashedName: make-typography-responsive
---

# --description--

Ao invés de utilizar `em` ou `px` para dimensionar o texto, você pode utilizar as unidades da viewport para obter uma tipografia responsiva. As unidades da viewport, assim como porcentagens, são unidades relativas, mas são baseadas em itens diferentes. As unidades da viewport são relativas as dimensões da viewport (largura ou altura) do dispositivo, e as porcentagens são relativas ao tamanho do container que é elemento pai.

As quatro diferentes unidades da viewport são:

<ul><li><code>vw</code> (viewport width): <code>10vw</code> representa 10% da largura da viewport.</li><li><code>vh</code> (viewport height): <code>3vh</code> representa 3% da altura da viewport.</li><li><code>vmin</code> (viewport minimum): <code>70vmin</code> representa 70% da menor dimensão da viewport (altura ou largura).</li><li><code>vmax</code> (viewport maximum): <code>100vmax</code> representa 100% da maior dimensão da viewport (altura ou largura).</li></ul>

Aqui está um exemplo que faz a tag body ter 30% da largura da viewport.

`body { width: 30vw; }`

# --instructions--

Coloque a `width` da tag `h2` em 80% da largura da viewport e a `width` do parágrafo com 75% da viewport de menor dimensão.

# --hints--

Sua tag `h2` deve ter a `width` de 80vw.

```js
assert(code.match(/h2\s*?{\s*?width:\s*?80vw;\s*?}/g));
```

Sua tag `p` deve ter a `width` de 75vmin.

```js
assert(code.match(/p\s*?{\s*?width:\s*?75vmin;\s*?}/g));
```

# --seed--

## --seed-contents--

```html
<style>

</style>

<h2>Importantus Ipsum</h2>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus quis tempus massa. Aenean erat nisl, gravida vel vestibulum cursus, interdum sit amet lectus. Sed sit amet quam nibh. Suspendisse quis tincidunt nulla. In hac habitasse platea dictumst. Ut sit amet pretium nisl. Vivamus vel mi sem. Aenean sit amet consectetur sem. Suspendisse pretium, purus et gravida consequat, nunc ligula ultricies diam, at aliquet velit libero a dui.</p>
```

# --solutions--

```html
<style>
  h2 {
      width: 80vw;
  }
  p {
      width: 75vmin;
  }
</style>

<h2>Importantus Ipsum</h2>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus quis tempus massa. Aenean erat nisl, gravida vel vestibulum cursus, interdum sit amet lectus. Sed sit amet quam nibh. Suspendisse quis tincidunt nulla. In hac habitasse platea dictumst. Ut sit amet pretium nisl. Vivamus vel mi sem. Aenean sit amet consectetur sem. Suspendisse pretium, purus et gravida consequat, nunc ligula ultricies diam, at aliquet velit libero a dui.</p>
```
