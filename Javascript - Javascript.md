# Função em Javascript:


## Função (normal):
Exemplo: function nomeDaFuncao (parametrosAqui) {
	     // instruções aqui
	     // causa queira pausar a função, podemos usar o 'return;'
         }

## Funções que representam expressões:

Exemplo: const soma = function (a, b) {
	    return a + b;
         }

	 soma (1, 2) // resultado: 3
	 soma (5, 4) // resultado: 9


-----------------------------------------------------------

## Função autoinvocada:

Uma função anônima entre parênteses, seguida por outro par de parênteses,
que representa sua chamada. Resumidamente, é uma função que já é invocada 
na sua declaração, quando já é criada.

Exemplo 1: (function () {
	     let name = "Digital Innovation One";
	     return name;
	   })();


Exemplo 2: const multiplicacao =
           (function() {
	      return a * b; 	
	   })(2, 5);

	   console.log (multiplicacao)  // resultado: 10


-----------------------------------------------------------

## Callbacks:

Uma função passada como argumento para outra.

Exemplo: 

const calc = function (operacao, num1, num2){
	return operacao (num1, num2);
}

const soma = function (num1, num2) {
	return num1 + num2;
}

const sub = function (num1, num2) {
	return num1 - num2;
}

const resultSoma = calc (soma, 1, 2); 
const resultSub = calc (sub, 1, 2);

console.log (resultSoma);  // resultado: 3
console.log (resultSub);  // resultado: -1


-----------------------------------------------------------

# Objetos:

## Objeto "Arguments":

É um array com todos os parâmetros passados quando a função foi invocada.

Exemplo: 

function showArgs () {
	return arguments;   // resultado: retorna um array com os argumentos passados quando
			       a função foi invocada
}


-----------------------------------------------------------

## Objeto Destructuring:

Entre chaves {}, podemos filtrar apenas os dados que nos insteressam
em um objeto.

const user = {
	id: 42,
	displayName: 'jdoe',
	fullName: {
	  firstName: 'John',
	  lastName: 'Doe'
	}
};

function userId ({id}) {
	return id;
}

function getFullName ({fullName: {firstName: first, lastName: last}}) {
	return '$(first) $(last)';
}

userID(user);   // resultado: 42 - nos retorna apenas a id da 'const user'

getFullName(user);   // resultado: John Doe - nos retorna apenas o nome
		     // e o sobrenome da 'const usert'


-----------------------------------------------------------

# Arrays:

## Função Spread:

Uma forma de lidar separadamente com elementos. O que era
um array se torna um elemento independente.

Exemplo:

function sum (x, y, z) {
	return x + y + z;
}

const numbers = [1, 2, 3];

console.log (sum (...numbers));   // os três pontos '...' possibilitam
				     usar o array como argumento para o método


-----------------------------------------------------------

# Função

## Função Rest:


Faz o oposto da função Spread! Combina os argumentos em um array.
O que era um elemento independente se torna parte de um array.

function confereTamanho (...args) {
	console.log (args.length)
}

confereTamanho ();   // resultado: Tamanho 0
confereTamanho (1, 2);   // resultado: Tamanho 2 
confereTamanho (3, 4, 5);   // resultado: Tamanho 3 


-----------------------------------------------------------

# Loops:

## Método push():

Método para adicionar um novo elemento no final do array.

Exemplo:


var adicionar = [];
adicionar.push(5);


-----------------------------------------------------------

## For... of:

Loop entre estruturas iteráveis (arrays, strings).

function logNumeros (nums) {
	for (num of nums) { // o loop vai percorrer cada elemento do array
		               e realizar uma ação para cada elemento. 
	    console.log(num);
	}
}

const nums = [30, 20, 233, 2];

logLetras(nums);
// 30
// 20
// 233
// 2


-----------------------------------------------------------

# Arrow Functions:

## Como usar uma Arrow Function:

Maneira simplificada de escrever um código. Os dois códigos seguintes fazem a mesma
coisa, mas são escritos de maneira diferentes, a grande diferença é o tamanho do código.

Exemplo:

const helloWorld = function () {
	return "Hello World";
}

const helloWorld = () => "Hello World";
// Ambos retornam um "Hello World"

*OBS: Caso exista apenas uma linha, pode dispensar as chaves e o return.
*OBS: Caso exista apenas um parâmetro, pode dispensar os parênteses.


-----------------------------------------------------------

## Outras Restrições:

- "this" sempre será o objeto global. Métodos para modificar seu 
valor não irão funcionar;

- Não existe o objeto "arguments";

- O construtur (ex: new MeuObjeto()) também não pode ser utilizado.


-----------------------------------------------------------

