Desafio da semana #4
--------------------

**Declare uma variável chamada `isTruthy`, e atribua a ela uma função que recebe um único parâmetro como argumento. Essa função deve retornar `true` se o equivalente booleano para o valor passado no argumento for `true`, ou `false` para o contrário.**
```js
var isTruthy = function(x) {
  return !!x;
};
```
**Invoque a função criada acima, passando todos os tipos de valores `falsy`.**
```js
isTruthy(0);
isTruthy(-0);
isTruthy(NaN);
isTruthy(null);
isTruthy(undefined);
isTruthy('');
isTruthy("");
isTruthy(false);
isTruthy();
```
**Invoque a função criada acima passando como parâmetro 10 valores `truthy`.**
```js
isTruthy('Kellen');
isTruthy(1);
isTruthy("2");
isTruthy('0');
isTruthy(8 + 4);
isTruthy(true);
isTruthy({});
isTruthy('Hello Word!');
isTruthy(2 <= 3);
isTruthy('Javascript');
```
**Declare uma variável chamada `carro`, atribuindo à ela um objeto com as seguintes propriedades (os valores devem ser do tipo mostrado abaixo):**

- `marca` - String
- `modelo` - String
- `placa` - String
- `ano` - Number
- `cor` - String
- `quantasPortas` - Number
- `assentos` - Number - cinco por padrão
- `quantidadePessoas` - Number - zero por padrão
```js
var carro = {
marca: 'Fiat', 
modelo: 'Uno', 
placa: 'KGL-8984', 
ano: 2016, 
cor: 'Preto',
quantasPortas: 4,
assentos: 5,
quantidadePessoas: 0
};
```
**Crie um método chamado `mudarCor` que mude a cor do carro conforme a cor passado por parâmetro.**
```js
carro.mudarCor = function(newCor) {
  carro.cor = newCor;
};
```
**Crie um método chamado `obterCor`, que retorne a cor do carro.**
```js
carro.obterCor = function() {
  return carro.cor;
};
```
**Crie um método chamado `obterModelo` que retorne o modelo do carro.**
```js
carro.obterModelo = function() {
  return carro.modelo;
};
```
**Crie um método chamado `obterMarca` que retorne a marca do carro.**
```js
carro.obterMarca = function() {
  return carro.marca;
};
```
**Crie um método chamado `obterMarcaModelo`, que retorne: "Esse carro é um [MARCA] [MODELO]"Para retornar os valores de marca e modelo, utilize os métodos criados.**
```js
carro.obterMarcaModelo = function() {
  return 'Esse carro é um ' +carro.obterMarca()+' ' +carro.obterModelo();
};
```
**Crie um método que irá adicionar pessoas no carro. Esse método terá as seguintes características:**

- Ele deverá receber por parâmetro o número de pessoas entrarão no carro. Esse número não precisa encher o carro, você poderá acrescentar as pessoas aos poucos.
- O método deve retornar a frase: "Já temos [X] pessoas no carro!"
- Se o carro já estiver cheio, com todos os assentos já preenchidos, o método deve retornar a frase: "O carro já está lotado!"
- Se ainda houverem lugares no carro, mas a quantidade de pessoas passadas por parâmetro for ultrapassar o limite de assentos do carro, então você deve mostrar quantos assentos ainda podem ser ocupados, com a frase:
"Só cabem mais [QUANTIDADE_DE_PESSOAS_QUE_CABEM] pessoas!" - Se couber somente mais uma pessoa, mostrar a palavra "pessoa" no retorno citado acima, no lugar de "pessoas".
```js
carro.addPessoas = function(nPessoas) {
    var qtd = carro.quantidadedePessoas + nPessoas;
    
    if(carro.quantidadedePessoas === carro.assentos && qtd >= carro.assentos) {
        return 'O carro já está lotado!';
    };
    
    if(qtd > carro.assentos) {   
	var newQtd = carro.assentos - carro.quantidadedePessoas; 
	var newAssentos = newQtd === 1 ? 'cabe' : 'cabem';
	var newPessoas = newQtd === 1 ? 'pessoa' : 'pessoas';
	return 'Só ' +newAssentos+ ' mais ' +newQtd+ ' ' +newPessoas+ '!';
    };
    
    carro.quantidadedePessoas += nPessoas;
    return 'Já temos ' +carro.quantidadedePessoas+ ' pessoas no carro!';
};
```
**Agora vamos verificar algumas informações do carro. Para as respostas abaixo, utilize sempre o formato de invocação do método (ou chamada da propriedade), adicionando comentários _inline_ ao lado com o valor retornado, se o método retornar algum valor.**

**Qual a cor atual do carro?**
```js
carro.obterCor(); // "Preto"
```
**Mude a cor do carro para vermelho.**
```js
carro.mudarCor('Vermelho');
```
**E agora, qual a cor do carro?**
```js
carro.obterCor(); // "Vermelho"
```
**Mude a cor do carro para verde musgo.**
```js
carro.mudarCor('Verde Musgo');
```
**E agora, qual a cor do carro?**
```js
carro.obterCor(); // "Verde Musgo"
```
**Qual a marca e modelo do carro?**
```js
carro.obterMarcaModelo(); // "Esse carro é um Fiat Uno"
```
**Adicione 2 pessoas no carro.**
```js
carro.addPessoa(2); // "Já temos 2 pessoas no carro!"
```
**Adicione mais 4 pessoas no carro.**
```js
carro.addPessoa(4); // "Só cabem mais 3 pessoas!"
```
**Faça o carro encher.**
```js
carro.addPessoa(3); // "Já temos 5 pessoas no carro!"
```
**Tire 4 pessoas do carro.**
```js
carro.addPessoa(-4); // "Já temos 1 pessoas no carro!"
```
**Adicione 10 pessoas no carro.**
```js
carro.addPessoa(10); // "Só cabem mais 4 pessoa!"
```
**Quantas pessoas temos no carro?**
```js
carro.quantidadedePessoas; // 1
```
