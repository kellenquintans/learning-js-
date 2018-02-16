Desafio da semana #7
--------------------

**Crie um array com 5 items (tipos variados).**
```js
var myArray = ['Kellen', {}, 5, true, null];
```

**Crie uma função chamada `addItem`, que irá adicionar itens no array criado. A função deverá retornar o array atualizado.**
```js
function addItem(itens) {
    myArray.push(itens);
    return myArray;
};
```

**Adicione um novo array ao array criado no início do desafio, com ao menos 3 itens de tipos diferentes, mostrando o resultado no console.**
```js
console.log(addItem(['14', 56, !!0]));
```

**Mostre no console o segundo elemento desse último array, criado acima, com a frase: "O segundo elemento do segundo array é [ELEMENTO]."**
```js
console.log('O segundo elemento do segundo array é '+myArray[5][1]+'.');
```

**Mostre no console quantos itens tem o primeiro array criado, com a frase: "O primeiro array tem [QUANTIDADE DE ITENS] itens."**
```js
console.log('O primeiro array tem '+myArray.length+' itens.');
```

**Agora mostre no console quantos itens tem o segundo array criado, com a frase: "O segundo array tem [QUANTIDADE DE ITENS] itens."**
```js
console.log('O segundo array tem '+myArray[5].length+' itens.');
```

**Utilizando a estrutura de repetição `while`, mostre no console todos os números pares entre 10 e 20, inclusive esses 2.**
```js
console.log( 'Números pares entre 10 e 20:' );
var pares = 10;
while(pares <= 20) {
  pares % 2 === 0 ? console.log(pares) : '';
  pares++;
};
```

**Na mesma ideia do exercício acima: mostre agora os números ímpares.**
```js
console.log( 'Números ímpares entre 10 e 20:' );
var impares = 10;
while(impares < 20) {
  impares % 2 !== 0 ? console.log(impares) : '';
  impares++;
};
```

**Repita os mesmos exercícios feitos acima, mas agora usando o loop "for". Só vamos mudar o range:**

- No primeiro "for", mostre os números pares entre 100 e 120, inclusive eles;
- No segundo "for", mostre os números ímpares entre 111 e 125, inclusive eles.
```js
console.log( 'Números pares entre 100 e 120:' );
for(var p = 100; p <= 120; p++) {
  p % 2 === 0 ? console.log(p) : '';
};
```

```js
console.log( 'Números ímpares entre 111 e 125:' );
for(var i = 111; i <= 125; i++) {
    i % 2 !== 0 ? console.log(i) : '';
};
```

