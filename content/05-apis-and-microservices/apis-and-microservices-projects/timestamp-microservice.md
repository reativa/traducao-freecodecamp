---
id: bd7158d8c443edefaeb5bdef
title: Microserviço Timestamp
challengeType: 4
forumTopicId: 301508
dashedName: timestamp-microservice
---

# --description--

Construa um projeto Javascript full stack cuja funcionalidade seja a similar a esta: <https://timestamp-microservice.freecodecamp.rocks/>. Para trabalhar nesse projeto será necessário que você escreva seu código utilizando um dos seguintes métodos:

- Clone [esse repositório GitHub](https://github.com/freeCodeCamp/boilerplate-project-timestamp/) e complete seu projeto localmente.
- Utilize [nosso inicializador de projeto repl.it ](https://repl.it/github/freeCodeCamp/boilerplate-project-timestamp) para completar seu projeto.
- Utilize um inicializador de sua preferência para completar o projeto. Assegure-se de incorporar todos os arquivos à partir do nosso repositório GitHub.

Ao terminar, assegure-se de que uma versão funcional do seu projeto esteja hospedada em algum lugar público. Em seguida, submeta a URL da sua versão no campo `Link da Solução`. Ainda, você pode, de forma opcional, submeter o link do código-fonte do seu projeto no campo `Link GitHub`.

# --hints--

Você deve fornecer seu próprio projeto, não a URL utilizada como exemplo.

```js
(getUserInput) => {
  assert(
    !/.*\/timestamp-microservice\.freecodecamp\.rocks/.test(getUserInput('url'))
  );
};
```

Uma requisição `GET` para `/api/timestamp/:date?` com uma data válida deve retornar um objeto JSON com a chave `unix` que representa um Unix timestamp da data de entrada em millissegundos.

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/api/timestamp/2016-12-25').then(
    (data) => {
      assert.equal(
        data.unix,
        1482624000000,
        'Should be a valid unix timestamp'
      );
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

Uma requisição `GET` para `/api/timestamp/:date?` com uma data válida deve retornar um objeto JSON com a chave `utc` que representa a data de entrada como uma string no formato: `Thu, 01 Jan 1970 00:00:00 GMT`.

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/api/timestamp/2016-12-25').then(
    (data) => {
      assert.equal(
        data.utc,
        'Sun, 25 Dec 2016 00:00:00 GMT',
        'Should be a valid UTC date string'
      );
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

Uma requisição `GET` para `/api/timestamp/1451001600000` deve retornar `{ unix: 1451001600000, utc: "Fri, 25 Dec 2015 00:00:00 GMT" }`.

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/api/timestamp/1451001600000').then(
    (data) => {
      assert(
        data.unix === 1451001600000 &&
          data.utc === 'Fri, 25 Dec 2015 00:00:00 GMT'
      );
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

Seu projeto pode lidar com datas string que podem ser convertidas com sucesso por `new Date(date_string)`.

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/api/timestamp/05 October 2011').then(
    (data) => {
      assert(
        data.unix === 1317772800000 &&
          data.utc === 'Wed, 05 Oct 2011 00:00:00 GMT'
      );
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

Caso a data string de entrada seja inválida, a api retorna um objeto contendo a estrutura `{ error : "Invalid Date" }`

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/api/timestamp/this-is-not-a-date').then(
    (data) => {
      assert.equal(data.error.toLowerCase(), 'invalid date');
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

Um parâmetro data vazio deve retornar a hora atual em um objeto JSON com a chave `unix`.

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/api/timestamp').then(
    (data) => {
      var now = Date.now();
      assert.approximately(data.unix, now, 20000);
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

Um parâmetro data vazio deve retornar a hora atual em um JSON com a chave `utc`.

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/api/timestamp').then(
    (data) => {
      var now = Date.now();
      var serverTime = new Date(data.utc).getTime();
      assert.approximately(serverTime, now, 20000);
    },
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
