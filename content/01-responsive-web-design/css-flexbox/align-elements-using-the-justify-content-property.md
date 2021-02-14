---
id: 587d78ac367417b2b2512af6
title: Alinhe Elementos Usando a Propriedade justify-content
challengeType: 0
videoUrl: 'https://scrimba.com/p/pVaDAv/c43gnHm'
forumTopicId: 301102
dashedName: align-elements-using-the-justify-content-property
---

# --description--

Às vezes, os itens com flex dentro de um contêiner com flex não preenchem todo o espaço do contêiner. É comum querer dizer ao CSS como alinhar e espaçar os itens com flex de uma determinada maneira. Felizmente, a propriedade `justify-content` tem várias opções para fazer isso. Mas, primeiro, há alguma terminologia importante a ser entendida antes de revisar essas opções.

[Aqui está uma imagem útil mostrando uma linha para ilustrar os conceitos abaixo.](https://www.w3.org/TR/css-flexbox-1/images/flex-direction-terms.svg)

Lembre-se de que um contêiner com flex é definido como uma linha que coloca os itens com flex lado a lado da esquerda para a direita. Um contêiner com flex é definido como uma coluna coloca os flex items em uma pilha vertical de cima para baixo. Para cada um, a direção em que os itens com flex são organizados é chamada de **eixo principal**. Para uma linha, esta é uma linha horizontal que corta cada item. E para uma coluna, o eixo principal é uma linha vertical que passa pelos itens.

Existem várias opções para espaçar os itens com flex ao longo da linha que é o eixo principal. Um dos mais comumente usados ​​é `justify-content: center;`, que alinha todos os itens com flex ao centro dentro do contêiner com flex. Outras opções incluem:

<ul><li><code>flex-start</code>: alinha os itens ao início do contêiner com flex. Para uma linha, empurra os itens para a esquerda do contêiner. Para uma coluna, empurra os itens para o topo do contêiner. Este é o alinhamento padrão se nenhum valor é especificado no <code>justify-content</code>.</li><li><code>flex-end</code>: alinha os itens ao final do contêiner com flex. Para uma linha, empurra os itens para a direita do contêiner. Para uma coluna,empurra os itens para o fundo do contêiner.</li><li><code>space-between</code>: alinha os itens ao centro do eixo principal, com espaço extra colocado entre os itens. O primeiro e o último itens são empurrados até a borda do contêiner com flex. Por exemplo, em uma fileira, o primeiro item fica do lado esquerdo do contêiner, o último item fica do lado direito do contêiner e o espaço restante é distribuído uniformemente entre os outros itens.</li><li><code>space-around</code>: semelhante ao <code>space-between</code> 
mas o primeiro e o último itens não são travados nas bordas do contêiner, o espaço é distribuído ao redor de todos os itens com meio espaço em cada extremidade do contêiner com flex.</li><li><code>space-evenly</code>: distribui o espaço uniformemente entre os itens com flex com um espaço completo em cada extremidade do contêiner com flex.</li></ul>

# --instructions--

Um exemplo ajuda a mostrar esta propriedade em ação. Adicione à propriedade `justify-content` no CSS no elemento`#box-container` e atribua a ele o valor `center`.

**Bônus**
Experimente as outras opções da propriedade `justify-content` no editor de código para ver suas diferenças. Mas note que um valor de `center` é o único que vai passar neste desafio.  
# --hints--

O elemento `#box-container` deve conter a propriedade `justify-content` property definida como `center`.

```js
assert($('#box-container').css('justify-content') == 'center');
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
    width: 25%;
    height: 100%;
  }

  #box-2 {
    background-color: orangered;
    width: 25%;
    height: 100%;
  }
</style>

<div id="box-container">
  <div id="box-1"></div>
  <div id="box-2"></div>
</div>
```

# --solutions--

```html
<style>
  #box-container {
    background: gray;
    display: flex;
    height: 500px;
    justify-content: center;
  }
  #box-1 {
    background-color: dodgerblue;
    width: 25%;
    height: 100%;
  }

  #box-2 {
    background-color: orangered;
    width: 25%;
    height: 100%;
  }
</style>

<div id="box-container">
  <div id="box-1"></div>
  <div id="box-2"></div>
</div>
```