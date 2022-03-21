# JavaScript - Primeiros passos

* [JavaScript](#javascript---primeiros-passos)
    * [Introdução](#introdução)
    * [Variáveis](#variáveis)
        * [Conversão de tipos](#conversão-de-tipos)
        * [Atribuição e imutabilidade](#atribuição-e-imutabilidade)
    * [Arrays](#arrays)
        * [Criando um array](#criando-um-array)
        * [Adicionar um item no array](#adicionar-um-item-no-array)
        * [Acessar um item no array](#acessar-um-item-no-array)
        * [Remover itens do array](#remover-itens-do-array)
    * [Condicionais e fluxo de execução](#condicionais-e-fluxo-de-execução)
        * [If e Else](#if-e-else)
        * [Operadores lógicos](#operadores-lógicos)
    * [Iterações](#iterações)
        * [While](#while)
        * [For](#for)
        * [Break](#break)


## Introdução
---

JavaScript é uma linguagem de programação interpretada, estruturada, de script em alto nível com tipagem dinâmica fraca e multiparadigma que é bastante utilizada no mundo, principalmente para desenvolvimento web e desenvolvimento de software.
Podemos usar tanto no front-end, quanto no back-end. No primeiro caso, ele quando usado junto ao HTML e o CSS, permite criar interatividade para as páginas da web que são criadas com essas duas outras tecnologias.

## Variáveis
---

JavaScript é case sensitive, dessa forma as variáveis idade e Idade, são diferentes e podem possuir valores distintos.
Existem as palavras reservadas : var, let e const para trabalharmos com variáveis.
Quando não utilizada nenhuma dessas palavras no momento de declaração de uma variável, a mesma fica no escopo global, ou seja não é muito viável.
Uma boa prática esta no fato de inserir a declaração com const ou let. 

 ### Conversão de tipos

 Na conversão de tipos em JavaScript temos o parseInt e o parseDouble.

Função que recebe uma string e retorna um inteiro na base que foi enviada como parâmetro. O parâmetro da "base" é opcional:

> parseInt(string, base)

<br>

Função que recebe uma string e retorna um número de ponto flutuante:

> parseFloat(string)

<br>

### Atribuição e imutabilidade

O operador de atribuição (=) é o qual atribui um valor do operando à direita ao operando à esquerda.
No comando:

```
let name = "Leon"

```

A variável *name* recebe a string "Leon", no caso, foi atribuido esse valor à ela.

A imutabilidade se refere a questão de que os tipos primitivos serem imutáveis, ou seja, não alteram o original.

## Arrays
---

O objeto Array é um objeto global que pode armazenar una coleção de elementos em uma única variável.

### Criando um array

```javascript

    var users = [ "Paul", "Anna", "Steve" ];

    console.log(users.length);
    // 3
```

### Adicionar um item no array

```javascript

    var addUser = users.push("Zoey");

    // ["Paul", "Anna", "Steve", "Zoey" ]
```
> O método *push* adicionar o elemento no final do array, já para adicionar ao ínicio , devemos usar o método *unshift*.

### Acessar um item no array

```javascript

    var firstUser = users[0];

    // Paul

    var user = users[1];

    // Anna
```

### Remover itens do array

```javascript

    users.splice(1,1);

    // ["Paul", "Steve", "Zoey" ]
```

> O método *splice* recebe como parâmetros a posição do elemento que queremos remover e a quantidade.

## Condicionais e fluxo de execução
---

### If e Else

O *if* é uma estrutura condicional que tendo o resultado lógico como verdadeiro, é realizado o bloco de código que foi determinado dentro do mesmo, caso for falso, é executado o bloco que foi declado dentro do *else*.

```javascript

    if(2 > 0){
        console.log("Maior");
    }else{
        console.log("Menor");
    }

    // Maior
```

Podemos ter múltiplos *if... else* no nosso código:

```javascript
    
     if (condição1)
        instrução1
     else if (condição2)
        instrução2
     else if (condição3)
        instrução3
     ...
     else
       instruçãoN
     

```

### Operadores lógicos

São operadores utilizados para permitir comparar variáveis e com o resultado dessa comparação, executar o código programado para determinado resultado.

**!**  Operador lógico NÃO (NOT)

**||**  Operador lógico OU (OR)

**&&**  Operador lógico E (AND)

## Iterações
---

### While

Declaração **while** cria um laço que executa um bloco de código enquanto a condição de teste for verdadeira. Nesse caso a condição é avaliada antes de executar o bloco de código.

<pre>
while(condição) {
    bloco de código
}
</pre>

### For

Declaração **for** cria um loop que possui três expressões opcionais.A condição sendo verdadeira, o laço irá se repetir.

<pre>
for([expressaoInicial];[condicao];[incremento]){
    bloco de código
}
</pre>

### Break

Quando é preciso encerrar um loop, é utilizado o comando **break**. Ele possui um label opcional que permite o encerramento da execução da estrutura que foi informada na label.

<pre>
break [label]
</pre>

 