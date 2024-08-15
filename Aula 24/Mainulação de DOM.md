# Manipulação de Elementos no DOM com `createElement`, `appendChild` e `removeChild`

## Objetivo:
Entender como criar, adicionar e remover elementos da árvore DOM usando JavaScript.

## 1. `createElement`
O método `createElement` cria um novo elemento HTML, mas ele não o insere automaticamente no DOM. Ele cria apenas o "esqueleto" do elemento.

### Exemplo:

```javascript
let novoElemento = document.createElement('div');
novoElemento.textContent = 'Olá, sou um novo elemento!';
```

Aqui, criamos uma `div` e definimos o conteúdo de texto para ela. Porém, ela ainda não aparece na página porque ainda não foi adicionada ao DOM.

## 2. `appendChild`

O método `appendChild` adiciona um elemento como o último filho de outro elemento no DOM. 

### Exemplo:

Vamos adicionar a `div` que criamos no exemplo anterior ao corpo do documento (`body`):

```javascript
document.body.appendChild(novoElemento);
```
Agora, o conteúdo `'Olá, sou um novo elemento!'` será exibido na página porque a `div` foi inserida no `body`.

## 3. `removeChild`

O método `removeChild` remove um elemento filho de um elemento pai no DOM.

### Exemplo:

Vamos remover o elemento que acabamos de adicionar:

```javascript
document.body.removeChild(novoElemento);
```
Esse código vai remover a `div` que inserimos no `body`.

### Exemplo Prático Completo

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Manipulando DOM</title>
</head>
<body>
  <button id="adicionar">Adicionar Elemento</button>
  <button id="remover">Remover Elemento</button>

  <script>
    let elementoCriado;

    // Adiciona novo elemento ao DOM
    document.getElementById('adicionar').addEventListener('click', function() {
      if (!elementoCriado) { // Verifica se o elemento já não foi criado
        elementoCriado = document.createElement('p');
        elementoCriado.textContent = 'Este é um parágrafo criado dinamicamente!';
        document.body.appendChild(elementoCriado);
      }
    });

    // Remove o elemento do DOM
    document.getElementById('remover').addEventListener('click', function() {
      if (elementoCriado) {
        document.body.removeChild(elementoCriado);
        elementoCriado = null; // Reseta a variável para poder criar de novo
      }
    });
  </script>
</body>
</html>
```
#### Explicação do Exemplo:

- Ao clicar no botão "Adicionar Elemento", um parágrafo será criado e adicionado ao `body`.
- Ao clicar no botão "Remover Elemento", o parágrafo será removido do `body`.
