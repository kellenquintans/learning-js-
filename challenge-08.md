Desafio da semana #8
--------------------

**Declare uma variável chamada `sum` e atribua a ela uma função chamada `calculateSum`. A função deve receber dois parâmetros e retornar a soma desses parâmetros.**
```js
var sum = function calculateSum(x, y) {
  return x + y;
};
```

**Invoque a função criada acima, passando dois números que serão somados, e mostre o resultado no console, com a frase: "A soma de [VALOR 1] e [VALOR2] é igual a [RESULTADO]."**
```js
var num1 = 8;
var num2 = 3;
console.log('A soma de '+num1+' e '+num2+' é igual a '+sum(num1, num2)+'.');

```

**Mostre no console o nome da função criada acima, com a frase: "O nome da função que faz a soma é [NOME DA FUNÇÃO]."**
```js
console.log('O nome da função que faz a soma é '+sum.name+'.');

```

**Crie uma função literal chamada `showName`. Essa função deve retornar o seu nome.**
```js
function showName() {
  return 'Kellen Quintans';  
};
```

**Declare uma variável chamada `varShowName` que recebe a função criada acima.**
```js
var varShowName = showName;

```

**Usando a variável criada acima, mostre no console o nome e o retorno da função atribuída a ela, com a seguinte frase: "A função [NOME DA FUNÇÃO] retorna [RETORNO DA FUNÇÃO]."**
```js
console.log('A função '+varShowName.name+' retorna '+varShowName()+'.');

```

**Crie uma função literal chamada `calculator`, que funcione assim:**

- A função deve receber um parâmetro que dirá qual operação matemática ela
vai efetuar. Será uma string com os valores `+`, `-`, `*`, `/` ou `%`;
- Essa função deve retornar uma segunda função que fará o seguinte:
  - Essa segunda função deve receber dois parâmetros;
  - Esses dois parâmetros serão os operandos usados na operação matemática;
  - O retorno dessa segunda função é a operação matemática completa, com a frase:
  "Resultado da operação: [NUMERO1] [OPERADOR] [NUMERO2] = [RESULTADO]."
  - Se o operador não for válido, retornar a frase: "Operação inválida."
```js
function calculator(ope) {
    return function (x, y) {
        var result;
        switch(ope) {
            case '+':
                result = x + y;
                break;
            case '-':
                result = x - y;
                break;
			case '*':
                result = x * y;
                break;
			case '/':
                result = x / y;
                break;
			case '%':
                result = x % y;
                break;
                default:
		return 'Operação inválida.';
            };
	return ('Resultado da operação: '+x+' '+ope+' '+y+' = '+result+'.');
    };
};
```

**Declare uma variável chamada `sum`, que receberá a função acima, passando como parâmetro o operador de soma.**
```js
var newSum = calculator('+');

```

**Agora `sum` é uma função. Mostre no console a soma de dois números, usando ela.**
```js
console.log(newSum(2, 6));

```

**Agora, declare algumas variáveis com os nomes `subtraction`, `multiplication`, `division` e `mod`, e atribua a elas a função `calculator`, passando o operador correto por parâmetro para cada uma delas.**
```js
var subtraction = calculator('-');
var multiplication = calculator('*');
var division = calculator('/');
var mod = calculator('%');

```

**Faça uma operação com cada uma das funções criadas acima, mostrando o resultado no console.**
```js
console.log(subtraction(19, 6));
console.log(multiplication(21, 4));
console.log(division(25, 5));
console.log(mod(17, 8));

```

