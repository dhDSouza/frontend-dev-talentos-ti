# Aula sobre `grid-layout` em CSS

## O que é `grid-layout`?

O CSS Grid Layout é um modelo de layout bidimensional que permite criar designs complexos e responsivos de forma intuitiva. Ele organiza o conteúdo em uma grade de linhas e colunas, facilitando a criação de layouts tanto em linhas quanto em colunas.

## Como funciona o Grid Layout?

Ao aplicar `display: grid` a um container, ele se torna um **grid container**, e seus filhos se tornam **grid items**. O container é dividido em linhas e colunas, e você pode posicionar os itens nas células da grade.

## Propriedades do Grid Container

### `grid-template-columns`

Define o número e o tamanho das colunas da grade. Você pode usar valores absolutos, relativos, ou até mesmo funções como `fr` (fração).

**Exemplo:**
```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr; /* Três colunas com larguras proporcionais */
}
```

Neste exemplo, a largura das colunas é dividida em três partes, onde a coluna do meio é duas vezes mais larga que as outras duas.

### `grid-template-rows`

Define o número e o tamanho das linhas da grade, semelhante a `grid-template-columns`.

**Exemplo:**
```css
.container {
  display: grid;
  grid-template-rows: 100px auto 200px; /* Três linhas com tamanhos específicos */
}
```

Aqui, a primeira linha tem 100px de altura, a segunda se ajusta automaticamente ao conteúdo, e a terceira tem 200px de altura.

### `grid-template-areas`

Cria áreas nomeadas na grade para um layout mais intuitivo e fácil de visualizar.

**Exemplo:**
```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr;
  grid-template-rows: auto 1fr auto;
  grid-template-areas:
    "header header"
    "sidebar content"
    "footer footer";
}
.header {
  grid-area: header;
}
.sidebar {
  grid-area: sidebar;
}
.content {
  grid-area: content;
}
.footer {
  grid-area: footer;
}
```

Neste exemplo, você define áreas nomeadas que são atribuídas aos itens, facilitando a visualização e o gerenciamento do layout.

### `grid-column` e `grid-row`

Essas propriedades permitem que você especifique a posição e o tamanho dos itens nas linhas e colunas da grade.

**Exemplo:**
```css
.item {
  grid-column: 1 / 3; /* O item ocupa da coluna 1 até a 3 */
  grid-row: 2 / 4; /* O item ocupa da linha 2 até a 4 */
}
```

Esse item será posicionado na primeira e segunda coluna e na segunda e terceira linha.

### `grid-gap`

Define o espaço entre as linhas e colunas da grade.

**Exemplo:**
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto auto;
  grid-gap: 10px; /* Espaço de 10px entre colunas e linhas */
}
```

Aqui, o `grid-gap` adiciona 10px de espaço entre todas as células da grade.

### `justify-items` e `align-items`

Controlam o alinhamento dos itens dentro de suas células.

**Exemplo:**
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  justify-items: center; /* Alinha os itens horizontalmente ao centro */
  align-items: start; /* Alinha os itens verticalmente ao início */
}
```

Os itens serão centralizados horizontalmente e alinhados ao início da célula verticalmente.

### `justify-content` e `align-content`

Controlam o alinhamento da grade inteira dentro do container.

**Exemplo:**
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto auto;
  justify-content: space-between; /* Distribui o espaço horizontalmente entre a grade e as bordas do container */
  align-content: center; /* Alinha a grade verticalmente ao centro do container */
}
```

A grade será distribuída uniformemente horizontalmente, e verticalmente, será centralizada no container.

### `grid-auto-flow`

Controla o fluxo automático dos itens quando não são explicitamente posicionados.

**Exemplo:**
```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-flow: dense; /* Preenche espaços vazios de forma densa */
}
```

Com `grid-auto-flow: dense`, o Grid Layout tenta preencher os espaços vazios, ajustando o layout dos itens para usar o espaço disponível de forma mais eficiente.

## Exemplos Práticos

### Layout de Site

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    .container {
      display: grid;
      grid-template-columns: 1fr 2fr;
      grid-template-rows: auto 1fr auto;
      grid-template-areas:
        "header header"
        "sidebar content"
        "footer footer";
      grid-gap: 10px;
    }
    .header {
      grid-area: header;
      background-color: lightcoral;
      padding: 20px;
    }
    .sidebar {
      grid-area: sidebar;
      background-color: lightblue;
      padding: 20px;
    }
    .content {
      grid-area: content;
      background-color: lightgreen;
      padding: 20px;
    }
    .footer {
      grid-area: footer;
      background-color: lightgoldenrodyellow;
      padding: 20px;
    }
  </style>
  <title>Grid Layout Example</title>
</head>
<body>
  <div class="container">
    <div class="header">Header</div>
    <div class="sidebar">Sidebar</div>
    <div class="content">Content</div>
    <div class="footer">Footer</div>
  </div>
</body>
</html>
```

### Layout com Áreas Nomeadas

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    .container {
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-template-rows: 100px auto;
      grid-template-areas:
        "header header"
        "main aside";
      grid-gap: 20px;
    }
    .header {
      grid-area: header;
      background-color: lightcoral;
    }
    .main {
      grid-area: main;
      background-color: lightblue;
    }
    .aside {
      grid-area: aside;
      background-color: lightgreen;
    }
  </style>
  <title>Named Areas Example</title>
</head>
<body>
  <div class="container">
    <div class="header">Header</div>
    <div class="main">Main Content</div>
    <div class="aside">Aside</div>
  </div>
</body>
</html>
```