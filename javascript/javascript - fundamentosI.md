# JavaScript - Fundamentos I
- [Tipos primitivos](#tipos-primitivos)
    - [Tipo number](#tipo-number)
    - [Tipo string](#tipo-string)
    - [Tipo boolean](#tipo-boolean)
- [Declarando variáveis](#declarando-variáveis)
    - [Convenção para nomes de variáveis](#convenção-para-nomes-de-variáveis)
    - [Truthy e falsy](#truthy-e-falsy)
    - [Conversão de tipos](#conversão-de-tipos)
- [O JavaScript e o NodeJS](#o-javascript-e-nodejs)
    - [JavaScript e NodeJS](#javascript-e-nodejs)
    - [Erros e stacktrace](#erros-e-stacktrace)
    - [Console.api](#consoleapi)
- [Operadores](#operadores)
    - [Operadores de comparação](#operadores-de-comparação)
    -[Operador ternário](#operador-ternário)
    - [Template literal](#template-literal)
- [Funções e Arrow Function](#funções-e-arrow-function)
    - [Funções](#funções)
    - [Parâmetros e argumentos](#parâmetros-e-argumentos)
    - [Expressão de função](#expressão-de-função)
    - [Arrow Function](#arrow-function)

## Tipos primitivos
---
### Tipo number
O tipo de dado number(numérico) armazenar valores numéricos inteiros e os de ponto flutuante em uma variável.
```javascript
    const altura = 1.69
    const idade = 31
```
NaN é uma propriedade do objeto global e significa Not-A-Number.

### Tipo string
Para dados de texto em JavaScript, temos o tipo de dado string. 

O caractere \u quando usado no início de um código, se torna um caractere de escape, fazendo com que o JavaScript ao ler essa parte do código veja a mesma como um código Unicode.

Existem vários métodos no tipo string e podem ser acessados para manipular as strings.

### Tipo boolean

Esse tipo de dado possui dois valores, o true e false. Ele é bastante usado quando precisamos fazer uma comparação no nosso código. 

### Tipo null e undefined
O null é um tipo especial que representa “ausência de valor” e pode ser atribuído como valor de uma variável.

Já undefined representa a mesma coisa, entretanto ele esta associado ao valor de uma variável que não foi inicializada.
```javascript
let input = null;
let input2;

console.log(input);  // null
console.log(input2); // undefined
```
## Declarando variáveis
---

### Convenção para nomes de variáveis
<br>

camelCase → inicia com letra minúscula e a primeira letra de cada palavra seguida é com letra maiúscula. 

- Exemplo: minhaVariavel ou mediaTotal

snake_case → substituindo os espaços pelo caractere _(underline), sendo todas as palavras com letra minúscula.

- Exemplo: minha_variavel ou media_total

kebab-case → similar ao snake-case, contudo o hífen fica no lugar do _(underline).

- Exemplo: minha-variavel ou media-total

PascalCase → similar ao camelCase, entretanto , nesse caso toda as palavras começam com letra maiúscula.

- Exemplo : MinhaVariavel ou MediaTotal

<br>

> Nunca use espaço , caracteres especiais e números para iniciar o nome de uma variável.

**var** : possui escopo global e com isso pode ser acessada eme qualquer parte do código.

**let** : possui escopo local, dessa forma, não podem ser acessada em outros escopos.

**const**: igual a let,mas no caso do const, seu valor uma vez definido, não pode ser alterado.

### Truthy e Falsy

São valores que no contexto booleano, se comportam como tipo verdadeiro e tipo falso respectivamente.

Valores falsy:

- zero;
- zero BigInt;
- null;
- undefined;
- false;
- NaN;
- string vazia("")

Valores truthy:

Todos os valores, excetos os avaliados para serem falsy.

### Conversão de tipos

A conversão acontece automaticamente entre os tipos de valores , entretanto não é uma boa prática depender dessa conversão, pois podem ocorrer erros.

##  O JavaScript e NodeJS

### JavaScript e NodeJS

O JavaScript é uma linguagem interpretada e com tipagem dinâmica.

O NodeJS é um interpretador de JavaScript que nos permite executar o JavaScript sem precisar de um navegador e sim no servidor.

### Erros e stacktrace

Essas são as categorias de erros que o JavaScript possui:

* RangeError;
* ReferenceError;
* SyntaxError;
* TypeError.

O stacktrace nos auxilia no momento de saber qual e onde o erro esta localizado no nosso código.

### Console.api

O Console API traz funcionalidades que permitem obtemos a realização de tarefas de debug, registrar mensagens referentes a execução de determinados pontos do código entre outras que auxiliam as etapas do desenvolvimento de software.

Por meio do terminal ,o NodeJS consegue visualizar essas mensagens.

## Operadores
---

### Operadores de comparação

Usando o operador <code>==</code> o JavaScript faz conversão entre tipos de variáveis, enquanto ao operador <code>===</code>  o valor precisa ser igual ao tipo da variável.

### Operador ternário

O operador ternário realiza uma comparação com três operadores juntos em uma única linha da seguinte forma: <code>comparação ? true:false</code>.

### Template literal

Ao usarmos template literal temos uma facilidade na construção de strings que precisam de concatenação.Para utilizar é necessário escrever com a seguinte sintaxe: <code>`${variavel}`</code>

## Funções e Arrow Function
---

### Funções

Funções são trechos de código que viabilizam a facilidade da manutenção do código e podem ser executadas diversas vezes.

A palavra reservada <code>return</code> retorna as informações da função.

### Parâmetros e argumentos

Os argumentos de uma função são chamados de parâmetros da função e eles são responsáveis pela passagem de variáveis  para as mesmas.

No JavaScript temos o hoisting onde permite o içamento de variáveis "var"e funções para o ínicio do código.

### Expressão de função

Expressões de função se entende como uma outra forma de declarar uma função, onde com o uso de variáveis do tipo const, podemos chamar as funções e atribuir a essa const.Para esse tipo de declaração de função, o hoisting não possui suporte.

```javascript
const myFunction = function Soma(let n1, let n2){//code here}
```

### Arrow Function

Uma forma de declaração mais compacta que també utiliza uma const. Ess forma també não possui suporte de hoisting.

```javascript
const Soma = (a, b)=>{
    return a + b;
}
```