# Controle de Fluxo e Funções

## 1. Estruturas de Controle

- **Condicionais (`if`, `else`, `else if`)**

    - As estruturas condicionais permitem que o código tome decisões com base em condições.

    - O `if` avalia uma condição, o `else if` permite adicionar mais condições, e o `else` é usado quando nenhuma das condições anteriores for verdadeira.

```javascript
let nota = 7;

if (nota >= 7) {
    console.log("Aprovado");
} else if (nota >= 5) {
    console.log("Recuperação");
} else {
    console.log("Reprovado");
}
```

- **Switch**

    - O `switch` é uma alternativa para `if else`, útil quando temos muitas condições diferentes que dependem do valor de uma única variável.

```javascript
let diaSemana = 3;

switch(diaSemana) {
    case 1:
        console.log("Domingo");
        break;
    case 2:
        console.log("Segunda-feira");
        break;
    case 3:
        console.log("Terça-feira");
        break;
    default:
        console.log("Dia inválido");
}
```

- **Laços de Repetição (`for`, `while`, `do while`)**

    - Laços permitem repetir um bloco de código várias vezes.
  
**Exemplo de `for`:**

```javascript
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```

**Exemplo de `while`:**

```javascript
let contador = 0;
while (contador < 5) {
    console.log(contador);
    contador++;
}
```

**Exemplo de `do while`:**

```javascript
let i = 0;
do {
    console.log(i);
    i++;
} while (i < 5);
```

## 2. Funções

- **Declaração de Funções**

    - Funções são blocos de código que realizam uma tarefa específica. Você pode definir uma função uma vez e reutilizá-la quantas vezes precisar.

```javascript
function soma(a, b) {
    return a + b;
}

console.log(soma(5, 3));  // retornará 8
```

- **Funções Anônimas e Arrow Functions**

    - Funções anônimas não têm nome e são geralmente usadas como funções de `callback`.

    - Arrow functions (`=>`) introduzidas no `ES6`, são uma forma concisa de escrever funções e não possuem seu próprio `this`.

```javascript
const multiplica = function(a, b) {
    return a * b;
};

const divide = (a, b) => a / b;

console.log(multiplica(5, 3));  // 15
console.log(divide(15, 3));  // 5
```