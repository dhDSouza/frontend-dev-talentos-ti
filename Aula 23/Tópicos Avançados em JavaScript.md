# Arrays, Objetos, Manipulação do DOM e Tópicos Avançados

## 1. Arrays e Objetos

- **Arrays**

  - `Arrays` são listas ordenadas de valores. Você pode acessar elementos individuais, adicionar novos elementos, e remover elementos existentes.

```javascript
let frutas = ["Maçã", "Banana", "Laranja"];
console.log(frutas[1]);  // retornará Banana

frutas.push("Uva");
console.log(frutas);  // retornará ["Maçã", "Banana", "Laranja", "Uva"]

frutas.pop();
console.log(frutas);  // retornará ["Maçã", "Banana", "Laranja"]
```

- **Objetos**

  - Objetos são coleções de pares chave-valor, onde cada valor pode ser acessado pela sua chave.

```javascript
let pessoa = {
    nome: "Daniel",
    idade: 28,
    cidade: "São Leopoldo"
};

console.log(pessoa.nome);  // retornará Daniel
pessoa.idade = 29;
console.log(pessoa.idade);  // retornará 29
```

## 2. Manipulação do DOM

- **Selecionando e Manipulando Elementos do DOM**

  - O *Document Object Model* (`DOM`) é uma interface que permite o `JavaScript` interagir com o `HTML` e `CSS`. Você pode selecionar elementos, alterar seus conteúdos, ou estilos.

```html
<html>
  <body>
    <h1 id="titulo">Olá, Mundo!</h1>
    <button onclick="mudaTexto()">Clique aqui</button>    
    <script>
      function mudaTexto() {
        document.getElementById("titulo").innerHTML = "Texto alterado!";
      }
    </script>
  </body>
</html>
  ```

## 3. Eventos

- **Capturando Eventos**

  - Eventos permitem que o `JavaScript` responda a ações do usuário, como cliques de botão, movimento do mouse ou pressionamento de teclas.

```html
<html>
  <body>

    <h1 id="titulo">Olá, Mundo!</h1>
    <button id="meuBotao">Clique aqui</button>

    <script>
      // Função que altera o texto do título ao clicar no botão
      function mudaTexto() {
        document.getElementById("titulo").innerHTML = "Texto alterado!";
      }
      // Adiciona um evento de clique ao botão
      document.getElementById("meuBotao").addEventListener("click", mudaTexto);
    </script>
    
  </body>
</html>
```

Neste exemplo, usamos `addEventListener` para capturar o evento de clique no botão e chamar a função `mudaTexto`, que altera o conteúdo do elemento `<h1>`.


## Exercícios

### Exercícios de Arrays e Objetos

1. **Manipulação de Arrays:**

   - Crie um array chamado `animais` contendo os nomes de quatro animais de sua escolha. 

   - Exiba o segundo animal no console.

   - Adicione um novo animal ao final do array e exiba o array atualizado.

   - Remova o primeiro animal do array e exiba o array atualizado.

   - Inverta a ordem dos elementos do array e exiba o resultado.

2. **Manipulação de Objetos:**

   - Crie um objeto chamado `carro` com as seguintes propriedades: `marca`, `modelo`, `ano`, `cor`.

   - Exiba o valor da propriedade `modelo` no console.

   - Altere a cor do carro para `vermelho` e exiba o objeto atualizado.

   - Adicione uma nova propriedade chamada `proprietario` com o valor do seu nome.

   - Crie uma função dentro do objeto `carro` que exibe uma frase no console com as propriedades do carro, por exemplo: "Este é um Toyota Corolla de 2020 na cor vermelho."

### Exercícios de Manipulação do DOM

3. **Interação com o DOM:**

   - Crie uma página HTML com um campo de texto (`input`) e um botão.

   - Adicione um evento de clique ao botão que captura o valor digitado no campo de texto e exibe esse valor em um parágrafo (`<p>`) na página.

   - Se o campo de texto estiver vazio, o parágrafo deve exibir "Por favor, insira um texto."

4. **Alteração de Estilos via DOM:**

   - Crie uma página HTML com um título (`<h1>`) e dois botões: "Mudar para Azul" e "Mudar para Verde".

   - Adicione eventos de clique aos botões para que, ao serem clicados, o título mude para a cor correspondente.

### Exercícios de Eventos

5. **Eventos de Mouse:**

   - Crie uma página HTML com uma `<div>` de 100x100 pixels com fundo cinza.

   - Adicione um evento que, ao passar o mouse sobre a `<div>`, ela mude para uma cor de sua escolha.

   - Quando o mouse sair da `<div>`, ela deve voltar à cor original.

6. **Eventos de Teclado:**

   - Crie uma página HTML com um campo de texto e uma `<div>` vazia abaixo dele.

   - Adicione um evento de teclado ao campo de texto que exiba na `<div>` o número de caracteres digitados sempre que o usuário pressionar uma tecla.
