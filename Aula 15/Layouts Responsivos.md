
# Responsividade em CSS com Flexbox

## Objetivos

- Compreender o conceito de design responsivo.
- Aprender a utilizar media queries.
- Implementar layouts responsivos com Flexbox.
- Aplicar práticas recomendadas para design responsivo.

## 1. Introdução ao Design Responsivo

**O que é Design Responsivo?**

- Design responsivo é uma abordagem de design que permite que uma página web se adapte a diferentes tamanhos de tela e dispositivos.

**Princípios do Design Responsivo:**

- Layout fluido.
- Imagens flexíveis.
- Media queries.

## 2. Media Queries

**O que são Media Queries?**

- Media queries são uma funcionalidade do CSS que permite aplicar estilos específicos para diferentes tamanhos de tela e dispositivos.

**Sintaxe Básica:**

```css
@media (min-width: 600px) {
  /* Estilos aplicados para telas com largura mínima de 600px */
}
```

**Exemplo Prático:**

```css
body {
  background-color: lightblue;
}

@media (min-width: 600px) {
  body {
    background-color: lightgreen;
  }
}

@media (min-width: 900px) {
  body {
    background-color: lightcoral;
  }
}
```

## 3. Layouts Flexíveis com Flexbox

**Flexbox:**

- Flexbox é um modelo de layout unidimensional que facilita a criação de layouts flexíveis e responsivos.

**Propriedades Principais:**

- `display: flex;` - Define um contêiner flexível.
- `flex-direction` - Define a direção dos itens no contêiner (row, column).
- `flex-wrap` - Permite que os itens do contêiner flexível envolvam para a próxima linha.
- `justify-content` - Alinha os itens ao longo do eixo principal.
- `align-items` - Alinha os itens ao longo do eixo transversal.
- `flex` - Define a capacidade de um item flexível de crescer, encolher e sua base flexível.

**Exemplo de Flexbox:**

```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
</div>
```

```css
.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.item {
  flex: 1 1 200px; /* Cresce, encolhe e tem uma base de 200px */
  background-color: lightblue;
  margin: 10px;
  padding: 20px;
  text-align: center;
}
```

## 4. Imagens e Vídeos Responsivos
**Tornando Imagens Responsivas:**
- Usar a propriedade `max-width` para garantir que a imagem nunca exceda a largura do seu contêiner.

**Exemplo:**
```css
img {
  max-width: 100%;
  height: auto;
}
```

**Vídeos Responsivos:**

- Envolver vídeos em um contêiner flexível.

**Exemplo:**
```html
<div class="video-container">
  <iframe src="..."></iframe>
</div>
```

```css
.video-container {
  position: relative;
  width: 100%;
  padding-bottom: 56.25%; /* 16:9 */
}

.video-container iframe {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
}
```

## 5. Práticas Recomendadas

**Mobile First:**

- Projetar primeiro para dispositivos móveis e, em seguida, adaptar para dispositivos maiores.

**Teste em Diversos Dispositivos:**

- Usar ferramentas como o DevTools do navegador para testar a responsividade.


## 6. Exercícios Práticos

**Exercício 1:**

- Criar uma página simples com um layout responsivo usando Flexbox.

**Exercício 2:**

- Criar uma galeria de imagens responsiva usando Flexbox.

**Exercício 3:**

- Tornar um vídeo responsivo em uma página web.