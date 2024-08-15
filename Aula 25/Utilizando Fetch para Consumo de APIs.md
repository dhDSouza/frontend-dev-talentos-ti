# Uso do `fetch`

- **O que é `fetch`?**

  `fetch` é uma função embutida em navegadores modernos que permite fazer requisições HTTP de maneira assíncrona. Com ele, podemos interagir com APIs, obtendo dados ou enviando informações.

- **Sintaxe básica:**

  ```javascript
  fetch(url, options)
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('Erro:', error));
  ```

  - **url**: O endpoint da API que você deseja acessar.

  - **options**: Objeto opcional para configurar o método, cabeçalhos, corpo, etc.

  - **response.json()**: Converte a resposta da API em JSON (geralmente o formato de dados de uma API REST).

  - **.catch()**: Trata erros na requisição.

## 2. Exemplos Práticos

### Exemplo 1: Fazendo uma Requisição GET

Vamos consumir uma API pública que retorna uma lista de usuários. Neste exemplo, usaremos a API da [JSONPlaceholder](https://jsonplaceholder.typicode.com).

```javascript
// Fazendo uma requisição GET para obter dados de usuários
fetch('https://jsonplaceholder.typicode.com/users')
  .then(response => response.json()) // Converte a resposta em JSON
  .then(data => {
    console.log(data); // Exibe os dados no console
  })
  .catch(error => console.error('Erro na requisição:', error)); // Tratamento de erros
```

### Exemplo 2: Fazendo uma Requisição POST

Neste exemplo, enviaremos dados para a API usando o método POST.

```javascript
// Enviando dados com uma requisição POST
fetch('https://jsonplaceholder.typicode.com/posts', {
  method: 'POST', // Define o método como POST
  headers: {
    'Content-Type': 'application/json' // Cabeçalhos indicando o formato dos dados enviados
  },
  body: JSON.stringify({
    title: 'Novo Post',
    body: 'Este é o conteúdo do post.',
    userId: 1
  }) // Convertendo o objeto para JSON
})
  .then(response => response.json())
  .then(data => console.log('Sucesso:', data))
  .catch(error => console.error('Erro na requisição:', error));
```

### Exemplo 3: Requisição GET para uma API de Filmes

- Consumindo a [OMDb API](http://www.omdbapi.com/) para buscar informações sobre um filme. Exibindo os dados retornados na página, como o título, ano de lançamento e uma imagem do pôster.

```javascript
const apiKey = 'sua_api_key_aqui'; // Lembre-se de substituir pela sua chave de API
fetch(`http://www.omdbapi.com/?t=Inception&apikey=${apiKey}`)
  .then(response => response.json())
  .then(data => {
    document.getElementById('title').textContent = data.Title;
    document.getElementById('year').textContent = data.Year;
    document.getElementById('poster').src = data.Poster;
  })
  .catch(error => console.error('Erro:', error));
```

### Exemplo 4: Requisição POST para uma API Fictícia

- Criando um formulário no HTML que permite ao usuário enviar dados para uma API. Ao submeter o formulário, captura os dados e envia-os com uma requisição `POST` usando `fetch`.

```html
<form id="postForm">
  <input type="text" id="title" placeholder="Título" required />
  <textarea id="body" placeholder="Conteúdo" required></textarea>
  <button type="submit">Enviar</button>
</form>

<script>
  document.getElementById('postForm').addEventListener('submit', function (e) {
    e.preventDefault(); // Evita o comportamento padrão do formulário

    const title = document.getElementById('title').value;
    const body = document.getElementById('body').value;

    fetch('https://jsonplaceholder.typicode.com/posts', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json'
      },
      body: JSON.stringify({ title, body, userId: 1 })
    })
      .then(response => response.json())
      .then(data => console.log('Post criado:', data))
      .catch(error => console.error('Erro ao enviar:', error));
  });
</script>
```

### Considerações Finais

- **Trate os erros**: Sempre use `.catch()` para tratar possíveis erros na comunicação com a API.

- **Manipule o DOM**: Após obter os dados da API, exiba-os na página manipulando o DOM com JavaScript.
