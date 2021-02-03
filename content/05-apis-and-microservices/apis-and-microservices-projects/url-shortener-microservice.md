---
id: bd7158d8c443edefaeb5bd0e
title: Microserviço Encurtador de URL
challengeType: 4
forumTopicId: 301509
dashedName: url-shortener-microservice
---

# --description--

Construa um projeto Javascript full stack cuja funcionalidade seja a similar a esta: <https://url-shortener-microservice.freecodecamp.rocks/>. Para trabalhar nesse projeto será necessário que você escreva seu código utilizando um dos seguintes métodos:

- Clone [esse repositório GitHub](https://github.com/freeCodeCamp/boilerplate-project-urlshortener/) e complete seu projeto localmente.
- Utilize [nosso inicializador de projeto repl.it ](https://repl.it/github/freeCodeCamp/boilerplate-project-urlshortener) para completar seu projeto.
- Utilize um inicializador de sua preferência para completar o projeto. Assegure-se de incorporar todos os arquivos à partir do nosso repositório GitHub.

Ao terminar, assegure-se de que uma versão funcional do seu projeto esteja hospedada em algum lugar público. Em seguida, submeta a URL da sua versão no campo `Link da Solução`. Ainda, você pode, de forma opcional, submeter o link do código-fonte do seu projeto no campo `Link GitHub`.

# --instructions--

**HINT:** Não se esqueça de utilizar um body parsing middleware para lidar com as requisições `POST`. Além disso, você pode utilizar a função `dns.lookup(host, cb)` do módulo central `dns` para verificar uma URL submetida.

# --hints--

Você deve fornecer seu próprio projeto, não a URL utilizada como exemplo.

```js
(getUserInput) => {
  assert(
    !/.*\/url-shortener-microservice\.freecodecamp\.rocks/.test(
      getUserInput('url')
    )
  );
};

```
Você pode realizar uma requisição `POST` da URL para `/api/shorturl/new` e receber um JSON como reposta com as propriedades `original_url` e `short_url`. Exemplo: `{ original_url : 'https://freeCodeCamp.org', short_url : 1}`.

```js
async (getUserInput) => {
  const url = getUserInput('url');
  const urlVariable = Date.now();
  const res = await fetch(url + '/api/shorturl/new/', {
    method: 'POST',
    headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
    body: `url=https://timestamp-microservice.freecodecamp.rocks/api/timestamp/${urlVariable}`
  });
  if (res.ok) {
    const { short_url, original_url } = await res.json();
    assert.isNotNull(short_url);
    assert.match(
      original_url,
      new RegExp(
        `https://timestamp-microservice.freecodecamp.rocks/api/timestamp/${urlVariable}`
      )
    );
  } else {
    throw new Error(`${res.status} ${res.statusText}`);
  }
};
```

Ao visitar `/api/shorturl/<short_url>`, você será redirecionado à URL original. 

```js
async (getUserInput) => {
  const url = getUserInput('url');
  const urlVariable = Date.now();
  let shortenedUrlVariable;
  const postResponse = await fetch(url + '/api/shorturl/new/', {
    method: 'POST',
    headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
    body: `url=https://timestamp-microservice.freecodecamp.rocks/api/timestamp/${urlVariable}`
  });
  if (postResponse.ok) {
    const { short_url } = await postResponse.json();
    shortenedUrlVariable = short_url;
  } else {
    throw new Error(`${postResponse.status} ${postResponse.statusText}`);
  }
  const getResponse = await fetch(
    url + '/api/shorturl/' + shortenedUrlVariable
  );
  if (getResponse) {
    const { redirected, url } = getResponse;
    assert.isTrue(redirected);
    assert.strictEqual(
      url,
      `https://timestamp-microservice.freecodecamp.rocks/api/timestamp/${urlVariable}`
    );
  } else {
    throw new Error(`${getResponse.status} ${getResponse.statusText}`);
  }
};
```

Se você fornecer uma URL inválida, a qual não corresponde ao formato válido `http://www.example.com`, a resposta JSON conterá `{ error: 'invalid url' }`.

```js
async (getUserInput) => {
  const url = getUserInput('url');
  const res = await fetch(url + '/api/shorturl/new/', {
    method: 'POST',
    headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
    body: `url=ftp:/john-doe.org`
  });
  if (res.ok) {
    const { error } = await res.json();
    assert.isNotNull(error);
    assert.strictEqual(error.toLowerCase(), 'invalid url');
  } else {
    throw new Error(`${res.status} ${res.statusText}`);
  }
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
