---
id: 5a8b073d06fa14fcfde687aa
title: Rastreador de Exercícios
challengeType: 4
forumTopicId: 301505
dashedName: exercise-tracker
---

# --description--
Construa um projeto Javascript full stack cuja funcionalidade seja a similar a esta: <https://exercise-tracker.freecodecamp.rocks/>. Para trabalhar nesse projeto será necessário que você escreva seu código utilizando um dos seguintes métodos:

- Clone [esse repositório GitHub](https://github.com/freeCodeCamp/boilerplate-project-exercisetracker/) e complete seu projeto localmente.
- Utilize [nosso inicializador de projeto repl.it ](https://repl.it/github/freeCodeCamp/boilerplate-project-exercisetracker) para completar seu projeto.
- Utilize um inicializador de sua preferência para completar o projeto. Assegure-se de incorporar todos os arquivos à partir do nosso repositório GitHub.

Ao terminar, assegure-se de que uma versão funcional do seu projeto esteja hospedada em algum lugar público. Em seguida, submeta a URL da sua versão no campo `Link da Solução`. Ainda, você pode, de forma opcional, submeter o link do código-fonte do seu projeto no campo `Link GitHub`.

# --hints--

Você deve fornecer seu próprio projeto, não a URL utilizada como exemplo.

```js
(getUserInput) => {
  const url = getUserInput('url');
  assert(
    !/.*\/exercise-tracker\.freecodecamp\.rocks/.test(getUserInput('url'))
  );
};
```

Você pode realizar uma requisição `POST` para `/api/exercise/new-user` com o dado de formulário `username` para criar um novo usuário. A resposta retornada será um objeto com as propriedades `username` e `_id`.


```js
async (getUserInput) => {
  const url = getUserInput('url');
  const res = await fetch(url + '/api/exercise/new-user', {
    method: 'POST',
    headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
    body: `username=fcc_test_${Date.now()}`.substr(0, 29)
  });
  if (res.ok) {
    const { _id, username } = await res.json();
    assert.exists(_id);
    assert.exists(username);
  } else {
    throw new Error(`${res.status} ${res.statusText}`);
  }
};
```
Você pode realizar uma requisição `GET` para `api/exercise/users` para obter um array de todos os usuários. Cada elemento do array é um objeto contendo o `username` e `_id` de um usuário.


```js
async (getUserInput) => {
  const url = getUserInput('url');
  const res = await fetch(url + '/api/exercise/users');
  if (res.ok) {
    const data = await res.json();
    assert.isArray(data);
    assert.isString(data[0].username);
    assert.isString(data[0]._id);
  } else {
    throw new Error(`${res.status} ${res.statusText}`);
  }
};
```

Você pode realizar uma requisição `POST` para `/api/exercise/add` com os dados de formulário `userId=_id`, `description`, `duration` e, opcionalmente, `date`. Caso nenhuma data seja fornecida, a data atual será utilizada. A resposta retornada será um objeto do tipo user com os campos de exercício adicionados. 

```js
async (getUserInput) => {
  const url = getUserInput('url');
  const res = await fetch(url + '/api/exercise/new-user', {
    method: 'POST',
    headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
    body: `username=fcc_test_${Date.now()}`.substr(0, 29)
  });
  if (res.ok) {
    const { _id, username } = await res.json();
    const expected = {
      username,
      description: 'test',
      duration: 60,
      _id,
      date: 'Mon Jan 01 1990'
    };
    const addRes = await fetch(url + '/api/exercise/add', {
      method: 'POST',
      headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
      body: `userId=${_id}&description=${expected.description}&duration=${expected.duration}&date=1990-01-01`
    });
    if (addRes.ok) {
      const actual = await addRes.json();
      assert.deepEqual(actual, expected);
    } else {
      throw new Error(`${addRes.status} ${addRes.statusText}`);
    }
  } else {
    throw new Error(`${res.status} ${res.statusText}`);
  }
};
```

Você pode realizar uma requisição `GET` para `/api/exercise/log` com o parâmetro `userId=_id` para obter os logs de exercícios de qualquer usuário. A resposta retornada será um objeto do tipo user com um `log` array de todos os exercícios adicionados. Cada item log possui as propriedades `description`, `duration` e `date`.


```js
async (getUserInput) => {
  const url = getUserInput('url');
  const res = await fetch(url + '/api/exercise/new-user', {
    method: 'POST',
    headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
    body: `username=fcc_test_${Date.now()}`.substr(0, 29)
  });
  if (res.ok) {
    const { _id, username } = await res.json();
    const expected = {
      username,
      description: 'test',
      duration: 60,
      _id,
      date: new Date().toDateString()
    };
    const addRes = await fetch(url + '/api/exercise/add', {
      method: 'POST',
      headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
      body: `userId=${_id}&description=${expected.description}&duration=${expected.duration}`
    });
    if (addRes.ok) {
      const logRes = await fetch(url + `/api/exercise/log?userId=${_id}`);
      if (logRes.ok) {
        const { log } = await logRes.json();
        assert.isArray(log);
        assert.equal(1, log.length);
      } else {
        throw new Error(`${logRes.status} ${logRes.statusText}`);
      }
    } else {
      throw new Error(`${addRes.status} ${addRes.statusText}`);
    }
  } else {
    throw new Error(`${res.status} ${res.statusText}`);
  }
};
```

Uma requisição para os logs de um usuário (`/api/exercise/log`) retorna um objeto com a propriedade `count` representando o número de exercícios retornados.

```js
async (getUserInput) => {
  const url = getUserInput('url');
  const res = await fetch(url + '/api/exercise/new-user', {
    method: 'POST',
    headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
    body: `username=fcc_test_${Date.now()}`.substr(0, 29)
  });
  if (res.ok) {
    const { _id, username } = await res.json();
    const expected = {
      username,
      description: 'test',
      duration: 60,
      _id,
      date: new Date().toDateString()
    };
    const addRes = await fetch(url + '/api/exercise/add', {
      method: 'POST',
      headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
      body: `userId=${_id}&description=${expected.description}&duration=${expected.duration}`
    });
    if (addRes.ok) {
      const logRes = await fetch(url + `/api/exercise/log?userId=${_id}`);
      if (logRes.ok) {
        const { count } = await logRes.json();
        assert(count);
      } else {
        throw new Error(`${logRes.status} ${logRes.statusText}`);
      }
    } else {
      throw new Error(`${addRes.status} ${addRes.statusText}`);
    }
  } else {
    throw new Error(`${res.status} ${res.statusText}`);
  }
};
```

Você pode acrescentar os parâmetros `from`, `to` e `limit` em uma requisição para `/api/exercise/log` a fim de obter logs parciais de qualquer usuário. Os parâmetros `from` e `to` são datas no formato `yyyy-mm-dd`. O parâmetro `limit` é um inteiro que representa quantos logs devem ser retornados. 


```js
async (getUserInput) => {
  const url = getUserInput('url');
  const res = await fetch(url + '/api/exercise/new-user', {
    method: 'POST',
    headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
    body: `username=fcc_test_${Date.now()}`.substr(0, 29)
  });
  if (res.ok) {
    const { _id, username } = await res.json();
    const expected = {
      username,
      description: 'test',
      duration: 60,
      _id,
      date: new Date().toDateString()
    };
    const addExerciseRes = await fetch(url + '/api/exercise/add', {
      method: 'POST',
      headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
      body: `userId=${_id}&description=${expected.description}&duration=${expected.duration}&date=1990-01-01`
    });
    const addExerciseTwoRes = await fetch(url + '/api/exercise/add', {
      method: 'POST',
      headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
      body: `userId=${_id}&description=${expected.description}&duration=${expected.duration}&date=1990-01-02`
    });
    if (addExerciseRes.ok && addExerciseTwoRes.ok) {
      const logRes = await fetch(
        url + `/api/exercise/log?userId=${_id}&from=1989-12-31&to=1990-01-03`
      );
      if (logRes.ok) {
        const { log } = await logRes.json();
        assert.isArray(log);
        assert.equal(2, log.length);
      } else {
        throw new Error(`${logRes.status} ${logRes.statusText}`);
      }
      const limitRes = await fetch(
        url + `/api/exercise/log?userId=${_id}&limit=1`
      );
      if (limitRes.ok) {
        const { log } = await limitRes.json();
        assert.isArray(log);
        assert.equal(1, log.length);
      } else {
        throw new Error(`${limitRes.status} ${limitRes.statusText}`);
      }
    } else {
      throw new Error(`${res.status} ${res.statusText}`);
    }
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
  Por favor, verifique nosso guia de contribuições para aprender mais.
*/
```
