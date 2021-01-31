---
id: bd7158d8c443edefaeb5bd0f
title: Microserviço de metadados de arquivos
challengeType: 4
forumTopicId: 301506
dashedName: file-metadata-microservice
---

# --description--
Construa um projeto Javascript full stack cuja funcionalidade seja a similar a esta: <https://file-metadata-microservice.freecodecamp.rocks/>. Para trabalhar nesse projeto será necessário que você escreva seu código utilizando um dos seguintes métodos:

- Clone [esse repositório GitHub](https://github.com/freeCodeCamp/boilerplate-project-filemetadata/) e complete seu projeto localmente.
- Utilize [nosso inicializador de projeto repl.it ](https://repl.it/github/freeCodeCamp/boilerplate-project-filemetadata) para completar seu projeto.
- Utilize um inicializador de sua preferência para completar o projeto. Assegure-se de incorporar todos os arquivos à partir do nosso repositório GitHub.

Ao terminar, assegure-se de que uma versão funcional do seu projeto esteja hospedada em algum lugar público. Em seguida, submeta a URL da sua versão no campo `Link da Solução`. Ainda, você pode, de forma opcional, submeter o link do código-fonte do seu projeto no campo `Link GitHub`.

# --instructions--

**HINT:** Você pode utilizar o pacote npm `multer` para lidar com o upload de arquivo. 

# --hints--

Você deve fornecer seu próprio projeto, não a URL utilizada como exemplo.

```js
(getUserInput) => {
  assert(
    !/.*\/file-metadata-microservice\.freecodecamp\.rocks/.test(
      getUserInput('url')
    )
  );
};
```

Você pode submeter um formulário que inclui o upload de um arquivo.

```js
async (getUserInput) => {
  const site = await fetch(getUserInput('url'));
  const data = await site.text();
  const doc = new DOMParser().parseFromString(data, 'text/html');
  assert(doc.querySelector('input[type="file"]'));
};
```
O campo de entrada do arquivo de formulário possui o atributo `name` definido como `upfile`.

```js
async (getUserInput) => {
  const site = await fetch(getUserInput('url'));
  const data = await site.text();
  const doc = new DOMParser().parseFromString(data, 'text/html');
  assert(doc.querySelector('input[name="upfile"]'));
};
```
Ao submter um arquivo, você receberá o arquivo `name`, `type` e `size` em bytes dentro da resposta JSON. 

```js
async (getUserInput) => {
  const formData = new FormData();
  const fileData = await fetch(
    'https://cdn.freecodecamp.org/weather-icons/01d.png'
  );
  const file = await fileData.blob();
  formData.append('upfile', file, 'icon');
  const data = await fetch(getUserInput('url') + '/api/fileanalyse', {
    method: 'POST',
    body: formData
  });
  const parsed = await data.json();
  assert.property(parsed, 'size');
  assert.equal(parsed.name, 'icon');
  assert.equal(parsed.type, 'image/png');
};
```

# --solutions--

```js
/**
  Desafios backend não precisam de soluções,
  uma vez que eles serão testados em um projeto totalmente funcional.
  Por favor, verifique nosso guia de contribuições para apreder mais.
*/
```
