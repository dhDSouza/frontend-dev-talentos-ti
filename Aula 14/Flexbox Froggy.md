# Flexbox Froggy Respostas

## Nível 1
**Código:**
```css
justify-content: flex-end;
/* ou */
justify-content: end;
/* ou */
flex-direction: row-reverse;
```
**Explicação:**
`justify-content` alinha os itens no eixo principal. No caso, `flex-end` posiciona os elementos no final, movendo o sapo para a vitória.

## Nível 2
**Código:**
```css
justify-content: center;
```
**Explicação:**
`justify-content: center` centraliza os sapos horizontalmente.

## Nível 3
**Código:**
```css
justify-content: space-around;
```
**Explicação:**
`space-around` divide o espaço igualmente entre os itens flexíveis, com metade do espaço em cada lado.

## Nível 4
**Código:**
```css
justify-content: space-between;
```
**Explicação:**
`space-between` coloca o espaço igualmente entre os itens, sem espaço nas extremidades.

## Nível 5
**Código:**
```css
align-items: flex-end;
/* ou */
align-items: end;
```
**Explicação:**
`align-items` alinha os itens no eixo cruzado, enviando os sapos para o fundo.

## Nível 6
**Código:**
```css
justify-content: center;
align-items: center;
/* ou */
justify-content: center;
place-items: center;
/* ou */
place-content: center;
align-items: center;
```
**Explicação:**
`justify-content` centraliza horizontalmente e `align-items` verticalmente. `place-items` e `place-content` são atalhos para os dois.

## Nível 7
**Código:**
```css
align-items: flex-end;
justify-content: space-around;
```
**Explicação:**
`align-items` posiciona os sapos no fundo e `justify-content` os espaça horizontalmente.

## Nível 8
**Código:**
```css
flex-direction: row-reverse;
```
**Explicação:**
`flex-direction: row-reverse` alinha os itens da direita para a esquerda.

## Nível 9
**Código:**
```css
flex-direction: column;
```
**Explicação:**
`flex-direction: column` alinha os itens verticalmente.

## Nível 10
**Código:**
```css
flex-direction: row-reverse;
justify-content: flex-end;
/* ou */
flex-direction: row-reverse;
justify-content: start;
```
**Explicação:**
`flex-direction: row-reverse` inverte a ordem dos elementos e `justify-content: flex-end` os move para a esquerda.

## Nível 11
**Código:**
```css
flex-direction: column;
justify-content: flex-end;
/* ou */
flex-direction: column;
justify-content: end;
```
**Explicação:**
`flex-direction: column` alinha verticalmente e `justify-content: flex-end` move os sapos para o fundo.

## Nível 12
**Código:**
```css
flex-direction: column-reverse;
justify-content: space-between;
```
**Explicação:**
`flex-direction: column-reverse` inverte a ordem vertical e `justify-content: space-between` espaça verticalmente.

## Nível 13
**Código:**
```css
flex-direction: row-reverse;
align-items: flex-end;
justify-content: center;
```
**Explicação:**
`flex-direction: row-reverse` inverte horizontalmente, `align-items: flex-end` move os sapos para o fundo e `justify-content: center` centraliza horizontalmente.

## Nível 14
**Código:**
```css
.yellow {
  order: 1;
}
```
**Explicação:**
`order` determina a ordem dos itens flexíveis.

## Nível 15
**Código:**
```css
.red {
  order: -1;
}
```
**Explicação:**
`order` negativo move o item para o início.

## Nível 16
**Código:**
```css
.yellow {
  align-self: flex-end;
/* ou */
  align-self: end;
}
```
**Explicação:**
`align-self` alinha individualmente no eixo cruzado.

## Nível 17
**Código:**
```css
.yellow {
  order: 1;
  align-self: flex-end;
}
```
**Explicação:**
`order` move para o final e `align-self` alinha no fundo.

## Nível 18
**Código:**
```css
flex-wrap: wrap;
```
**Explicação:**
`flex-wrap` permite quebra de linha.

## Nível 19
**Código:**
```css
flex-direction: column;
flex-wrap: wrap;
/* ou */
flex-direction: column-reverse;
flex-wrap: wrap;
```
**Explicação:**
`flex-direction: column` alinha verticalmente e `flex-wrap` permite múltiplas colunas.

## Nível 20
**Código:**
```css
flex-flow: column wrap;
/* ou */
flex-flow: column-reverse wrap;
```
**Explicação:**
`flex-flow` é um atalho para `flex-direction` e `flex-wrap`.

## Nível 21
**Código:**
```css
align-content: flex-start;
/* ou */
align-content: start;
```
**Explicação:**
`align-content` alinha linhas no eixo cruzado.

## Nível 22
**Código:**
```css
align-content: flex-end;
/* ou */
align-content: end;
```
**Explicação:**
`align-content` move linhas para o final.

## Nível 23
**Código:**
```css
flex-direction: column-reverse;
align-content: center;
```
**Explicação:**
`flex-direction: column-reverse` inverte verticalmente e `align-content: center` centraliza as colunas.

## Nível 24
**Código:**
```css
flex-direction: column-reverse;
flex-wrap: wrap-reverse;
align-content: space-between;
justify-content: center;
```
**Explicação:**
Combinação de `flex-direction`, `flex-wrap`, `align-content` e `justify-content` para posicionamento desejado.

**Repostas mais detalhadas podem ser encontradas no [link](https://utsavmeena.com/flexbox-froggy-answers/).**