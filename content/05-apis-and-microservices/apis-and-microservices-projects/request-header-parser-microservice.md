---
id: bd7158d8c443edefaeb5bdff
title: Request Header Parser Microservice
challengeType: 4
forumTopicId: 301507
dashedName: request-header-parser-microservice
---

# --description--

Construa um projeto Javascript full stack cuja funcionalidade seja a similar a esta: <https://request-header-parser-microservice.freecodecamp.rocks/>. Para trabalhar nesse projeto será necessário que você escreva seu código utilizando um dos seguintes métodos:

- Clone [esse repositório GitHub](https://github.com/freeCodeCamp/boilerplate-project-headerparser/) e complete seu projeto localmente.
- Utilize [nosso inicializador de projeto repl.it ](https://repl.it/github/freeCodeCamp/boilerplate-project-headerparser) para completar seu projeto.
- Utilize um inicializador de sua preferência para completar o projeto. Assegure-se de incorporar todos os arquivos à partir do nosso repositório GitHub.

Ao terminar, assegure-se de que uma versão funcional do seu projeto esteja hospedada em algum lugar público. Em seguida, submeta a URL da sua versão no campo `Link da Solução`. Ainda, você pode, de forma opcional, submeter o link do código-fonte do seu projeto no campo `Link GitHub`.

# --hints--

Você deve fornecer seu próprio projeto, não a URL utilizada como exemplo.

```js
(getUserInput) => {
  assert(
    !/.*\/request-header-parser-microservice\.freecodecamp\.rocks/.test(
      getUserInput('url')
    )
  );
};
```

Uma requisição `GET` para `/api/whoami` deve retornar um objeto JSON com o seu endereço IP na chave `ipaddress`.

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/api/whoami').then(
    (data) => assert(data.ipaddress && data.ipaddress.length > 0),
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

Uma requisição `GET` para `/api/whoami` deve retornar um objeto JSON com sua linguagem de preferência na chave `language`.

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/api/whoami').then(
    (data) => assert(data.language && data.language.length > 0),
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

Uma requisição `GET` para `/api/whoami` deve retornar um objeto JSON com seu software na chave `software`.

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/api/whoami').then(
    (data) => assert(data.software && data.software.length > 0),
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

# --solutions--

```js
/**
  Desafios backend não precisam de soluções,
  uma vez que eles serão testados em um projeto totalmente funcional.
  Por favor, verifique nosso guia de contribuições para apreder mais.
*/
```
