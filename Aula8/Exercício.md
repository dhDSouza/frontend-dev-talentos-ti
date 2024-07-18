## Exercício: Estruturando um Blog de Notícias com HTML5 Semântico

**Objetivo:** Criar um blog de notícias utilizando tags semânticas do HTML5, estruturando o conteúdo de forma adequada para receber a folha de estilo CSS fornecida pelo professor.

## Passo a Passo

1. Criação do Arquivo HTML

- Crie um novo arquivo chamado blog.html.
- Estrutura Básica do HTML

- Inicie o arquivo HTML com a declaração do tipo de documento `<!DOCTYPE html>`.
- Adicione a tag `<html>` para envolver todo o conteúdo da página.
- Dentro da tag `<html>`, adicione a tag `<head>` e a tag `<body>`.
- Cabeçalho da Página (Header)

- Dentro da tag `<body>`, adicione uma tag `<header>`.
- Dentro do `<header>`, insira a tag `<h1>` com o título do blog.
- Adicione uma tag `<nav>` para a navegação.
- Dentro da `<nav>`, crie uma lista não ordenada (`<ul>`) e adicione links de navegação (`<a>`) dentro de itens de lista (`<li>`).

2. Conteúdo Principal (Main)

- Adicione uma tag `<main>` para envolver o conteúdo principal da página.
- Dentro de `<main>`, crie várias seções (`<section>`) para diferentes categorias de notícias (por exemplo, Últimas Notícias, Mundo, Tecnologia, Esportes).

3. Seções de Notícias

- Dentro de cada `<section>`, adicione um título (`<h2>`) para a categoria de notícias.
- Crie vários artigos (`<article>`) dentro de cada seção para cada notícia.
- Dentro de cada `<article>`, adicione um cabeçalho do artigo (`<header>`).
- Dentro do `<header>`, insira o título da notícia (`<h3>`) e informações sobre a publicação (data e autor).
- Adicione um parágrafo (`<p>`) com o resumo da notícia.

4. Seção Lateral (Aside)

- Adicione uma tag `<aside>` dentro de `<main>` para incluir uma seção lateral com as notícias mais lidas.
- Dentro do `<aside>`, adicione um título (`<h2>`).
- Crie uma lista não ordenada (`<ul>`) com links (`<a>`) para as notícias populares.

5. Rodapé da Página (Footer)

- Adicione uma tag `<footer>` no final da tag `<body>`.
- Dentro do `<footer>`, insira um parágrafo (`<p>`) com informações de direitos autorais.

**Orientações**

- Verifique a Estrutura: Certifique-se de que todas as tags estão corretamente aninhadas e fechadas.
- Utilize Conteúdo Adequado: Preencha os títulos, resumos e links com informações fictícias ou baseadas em um tema de sua escolha.

- Integração com CSS: Certifique-se de incluir a referência ao arquivo CSS (estilo.css) dentro da tag `<head>` para estilizar a página corretamente.
- Teste no Navegador: Visualize a página no navegador para garantir que o layout esteja conforme o esperado.

**Resultado Esperado**

A página deve exibir um blog de notícias com uma navegação funcional, várias seções de notícias, uma seção lateral com links para notícias populares, e um rodapé com informações de direitos autorais.

O conteúdo deve estar claramente organizado e estilizado conforme a folha de estilo CSS fornecida.