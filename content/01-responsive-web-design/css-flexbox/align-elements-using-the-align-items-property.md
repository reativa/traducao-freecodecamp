---
id: 587d78ad367417b2b2512af8
title: Alinhe Elementos Usando a Propriedade align-items
challengeType: 0
videoUrl: 'https://scrimba.com/p/pVaDAv/c8aggtk'
forumTopicId: 301101
dashedName: align-elements-using-the-align-items-property
---

# --description--

A propriedade `align-items` é semelhante à `justify-content`. Lembre-se de que a propriedade `justify-content` alinhava os itens com flex ao longo do eixo principal. Para linhas, o eixo principal é uma linha horizontal e para colunas é uma linha vertical.

Os contêineres com flex possuiem também um **eixo transversal** que é o oposto do eixo principal. Para linhas, o eixo trasnversal é vertical e para colunas, o eixo transaversal é horizontal.

O CSS oferece a propriedade `align-items` para alinhar os itens com flex ao longo do eixo transversal. Para uma linha, ele diz ao CSS como empurrar os itens em toda a linha para cima ou para baixo dentro do contêiner. E para uma coluna, ele diz como empurrar todos os itens para a esquerda ou direita dentro do contêiner.

Os diferentes valores disponíveis para `align-items` são:

<ul><li><code>flex-start</code>: alinha os itens ao início do contêiner com flex. Para as linhas, alinha os itens ao topo do contêiner. Para colunas, alinha os itens à esquerda do contêiner.</li><li><code>flex-end</code>: alinha os itens ao final do contêiner com flex. Para linhas, alinha os itens na parte inferior do contêiner. Para colunas, alinha os itens à direita do contêiner.</li><li><code>center</code>: alinha os itens ao centro. Para as linhas, alinha os itens verticalmente (espaço igual acima e abaixo dos itens). Para colunas, alinha horizontalmente (espaço igual à esquerda e à direita dos itens).</li><li><code>stretch</code>: estica os itens para encher o contêiner com flex. Por exemplo, os itens das linhas são esticados para preencher o contêiner com flex de cima para baixo. Este é o valor padrão se nenhum valor for especificado para <code>align-items</code>.</li><li><code>baseline</code>: alinha os itens às suas linhas de base. A linha de base é um conceito de texto, pense nisso como a linha em que as letras ficam.</li></ul>

# --instructions--

Um exemplo ajuda a mostrar esta propriedade em ação. Adicione a propriedade `align-items` do CSS ao elemento `# box-container` e atribua a ele o valor `center`.

**Bônus**  
Experimente as outras opções para a propriedade `align-items` no editor de código para ver suas diferenças. Mas note que um valor de `center` é o único que vai passar neste desafio.

# --hints--

O elemento `#box-container` deve conter uma propriedade `align-items` definida como `center`.

```js
assert($('#box-container').css('align-items') == 'center');
```

# --seed--

## --seed-contents--

```html
<style>
  #box-container {
    background: gray;
    display: flex;
    height: 500px;

  }
  #box-1 {
    background-color: dodgerblue;
    width: 200px;
    font-size: 24px;
  }

  #box-2 {
    background-color: orangered;
    width: 200px;
    font-size: 18px;
  }
</style>

<div id="box-container">
  <div id="box-1"><p>Hello</p></div>
  <div id="box-2"><p>Goodbye</p></div>
</div>
```

# --solutions--

```html
<style>
  #box-container {
    background: gray;
    display: flex;
    height: 500px;
    align-items: center;
  }
  #box-1 {
    background-color: dodgerblue;
    width: 200px;
    font-size: 24px;
  }

  #box-2 {
    background-color: orangered;
    width: 200px;
    font-size: 18px;
  }
</style>

<div id="box-container">
  <div id="box-1"><p>Hello</p></div>
  <div id="box-2"><p>Goodbye</p></div>
</div>
```
