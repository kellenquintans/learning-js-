Desafio da semana #5
--------------------

**Crie uma variável qualquer, que receba um array com alguns valores aleatórios - ao menos 5 - (fica por sua conta os valores do array).**
```js
var myArray = ['Kellen', 12, 'Hello', 4, '0'];
```
**Crie uma função que receba um array como parâmetro, e retorne esse array.**
```js
function rParametro(arg) {
  return arg;
};
```
**Imprima o segundo índice do array retornado pela função criada acima.**
```js
console.log(rParametro(myArray)[1]);
```
**Crie uma função que receba dois parâmetros: o primeiro, um array de valores; e o segundo, um número. A função deve retornar o valor de um índice do array que foi passado no primeiro parâmetro. O índice usado para retornar o valor, deve ser o número passado no segundo parâmetro.**
```js
function newArray(a, index) {
    return a[index];
};
```
**Declare uma variável que recebe um array com 5 valores, de tipos diferentes.**
```js
var Arr = ['Kellen', true, null, {}, 14];
```
**Invoque a função criada acima, fazendo-a retornar todos os valores do último array criado.**
```js
console.log(newArray(Arr,0));
console.log(newArray(Arr,1));
console.log(newArray(Arr,2));
console.log(newArray(Arr,3));
console.log(newArray(Arr,4));
```
**Crie uma função chamada `book`, que recebe um parâmetro, que será o nome do livro. Dentro dessa função, declare uma variável que recebe um objeto com as seguintes características:**

- esse objeto irá receber 3 propriedades, que serão nomes de livros;
- cada uma dessas propriedades será um novo objeto, que terá outras 3
propriedades:
    - `quantidadePaginas` - Number (quantidade de páginas)
    - `autor` - String
    - `editora` - String
- A função deve retornar o objeto referente ao livro passado por parâmetro.
- Se o parâmetro não for passado, a função deve retornar o objeto com todos os livros.
```js
function book(names) {
    var books = {
        'Extraordinário': {
        quantidadedePaginas: 320,
        autor: 'R. J. Palacio',
        editora: 'Intrínseca'
    },
		'Dom Casmurro': {
        quantidadedePaginas: 290,
        autor: 'Machado de Assis',
        editora: 'Globo Editora'
    },
		'Como Eu Era Antes de Você': {
        quantidadedePaginas: 320,
        autor: 'Jojo Moyes',
        editora: 'Intrinseca'
    }
	};
	return names ? books[names] : books;
};
```
**Usando a função criada acima, imprima o objeto com todos os livros.**
```js
console.log(book());
```
**Ainda com a função acima, imprima a quantidade de páginas de um livro qualquer, usando a frase: "O livro [NOME_DO_LIVRO] tem [X] páginas!"**
```js
console.log('O livro Extraordinário tem '+book('Extraordinário').quantidadedePaginas+' páginas!');
```
**Ainda com a função acima, imprima o nome do autor de um livro qualquer, usando a frase: "O autor do livro [NOME_DO_LIVRO] é [AUTOR]."**
```js
console.log('O autor do livro Extraordinário é '+book('Extraordinário').autor+'.');
```
**Ainda com a função acima, imprima o nome da editora de um livro qualquer, usando a frase: "O livro [NOME_DO_LIVRO] foi publicado pela editora [NOME_DA_EDITORA]."**
```js
console.log('O livro Extraordinário foi publicado pela editora '+book('Extraordinário').editora+'.');
```
