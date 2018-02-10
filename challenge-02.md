**Desafio da semana #2**
------------------------

Nesse exercício, você está livre para escolher os nomes para suas variáveis e funções! 😄

**Crie uma função que receba dois argumentos e retorne a soma dos mesmos.**
```js
function soma(a , b){
  return a + b;
}
```
**Declare uma variável que receba a invocação da função criada acima, passando dois números quaisquer por argumento, e somando `5` ao resultado retornado da função.**
```js
var r = soma(3, 9) + 5;
```
**Qual o valor atualizado dessa variável?**
```js
17
```
**Declare uma nova variável, sem valor.**
```js
var x;
```
**Crie uma função que adicione um valor à variável criada acima, e retorne a string: O valor da variável agora é VALOR. Onde VALOR é o novo valor da variável.**
```js
function newValue() {
  x = 8;
  return 'O valor da variável agora é ' + x;
}
```
**Invoque a função criada acima.**
```js
newValue()
```
**Qual o retorno da função? (Use comentários de bloco).**
```js
/* 'O valor da variável agora é 8' */
```
**Crie uma função com as seguintes características:**
1. A função deve receber 3 argumentos;
2. Se qualquer um dos três argumentos não estiverem preenchidos, a função deve retornar a string: `Preencha todos os valores corretamente!`
3. O retorno da função deve ser a multiplicação dos 3 argumentos, somando `2` ao resultado da multiplicação.
```js
function args(a, b, c) {
  if(a === undefined || b === undefined || c === undefined) {
    return 'Preencha todos os valores corretamente!';
  } else {
    return (a * b * c) + 2;
  }
}
```
**Invoque a função criada acima, passando só dois números como argumento.**
```js
args(2, 5)
```
**Qual o resultado da invocação acima? (Use comentários para mostrar o valor retornado).**
```js
// 'Preencha todos os valores corretamente!'
```
**Agora invoque novamente a função criada acima, mas passando todos os três argumentos necessários.**
```js
args(5, 2, 3)
```
**Qual o resultado da invocação acima? (Use comentários para mostrar o valor retornado).**
```js
// 32
```
**Crie uma função com as seguintes características:**
1. A função deve receber 3 argumentos.
2. Se somente um argumento for passado, retorne o valor do argumento.
3. Se dois argumentos forem passados, retorne a soma dos dois argumentos.
4. Se todos os argumentos forem passados, retorne a soma do primeiro com o segundo, e o resultado, dividido pelo terceiro.
5. Se nenhum argumento for passado, retorne o valor booleano `false`.
6. E ainda, se nenhuma das condições acima forem atendidas, retorne `null`.
```js
function newArgs(x, y, z) {
  if(x !== undefined && y === undefined && z === undefined) {
    return x;
  
  } else if(x !== undefined && y !== undefined && z === undefined) {
    return x + y;
    
  } else if(x !== undefined && y !== undefined && z !== undefined) {
    return (x + y) / z;
  
  } else if(x === undefined && y === undefined && z === undefined) {
    return false;
  
  } else {
    return null;
  }
}
```
**Invoque a função acima utilizando todas as possibilidades (com nenhum argumento, com um, com dois e com três.) Coloque um comentário de linha ao lado da função com o resultado de cada invocação.**
```js
newArgs(); // false
newArgs(3); // 3
newArgs(4, 5); // 9
newArgs(3, 6, 2); // 4.5
```
