# JavaScript

O objetivo desse curso é ensinar JavaScript na prática para os alunos do curso
técnico de informática do Colégio Politec.

## Módulo 1: Introdução ao JavaScript

### História e Importância do JavaScript

História:
- [Wikipedia: JavaScript](https://en.wikipedia.org/wiki/JavaScript)
- [JavaScript Brasil](https://brasil.js.org/)
- [JavaScript: The First 20 Years](https://drive.google.com/file/d/10E4BBBCJaxccBCOAB1MbDZNQkPBFCmdj/view?usp=drive_link)

Usos:
- Servidor:
    - [NodeJS](https://nodejs.org/en)
    - [Bun.sh](https://bun.sh/)
    - [Deno](https://deno.com/)
- Aplicação Desktop:
    - [ElectronJS](https://www.electronjs.org/)
    - [Proton Native](https://proton-native.js.org/)
- Aplicação para Celular:
    - [React Native](https://reactnative.dev/)
    - [Ionic Framework](https://ionicframework.com/)
- Sistemas embarcados:
    - [Espruino](https://www.espruino.com/)
- Computação de borda:
    - [Fastly VCL](https://developer.fastly.com/learning/compute/javascript/),
    - [Cloudflare
      Workers](https://developers.cloudflare.com/workers/runtime-apis/)

Conferências:
- [BrazilJS](https://conf.braziljs.org/)
- [Front In Sampa](https://evento.frontinsampa.com.br/)

### Curiosidades e Conteúdo Extras

- [The old "var"](https://javascript.info/var)
- [The Modern JavaScript Tutorial](https://javascript.info/)
- [Introduction to Programming with JavaScript](https://launchschool.com/books/javascript)
- [JavaScript Eloquente](https://github.com/braziljs/eloquente-javascript)
- [JavaScript is Weird](https://www.youtube.com/watch?v=pZUTdw6zcck)

### Configuração do Ambiente de Desenvolvimento

- Navegador Google Chrome
- Editor de texto Visual Studio Code
- Repositório de código Git e GitHub

# Sintaxe Básica

Vamos ver como escrever e usar os principais recursos da linguagem.

## Variáveis

```javascript
const numero = 42
let mensagem;
var outraMensagem;

mensagem = 'uma mensagem motivacional'
outraMensagem = 'mais uma mensagem motivacional'
```

Referências

- [MDN - const](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/const)
- [MDN - let](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/let)
- [MDN - var](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/var)

## Números e Matemática

```javascript
const numero_inteiro = 10
console.log(numero_inteiro, typeof numero_inteiro)
const numero_fracionario = 10.3
console.log(numero_fracionario, typeof numero_fracionario)
const numero_grande = 0.3e8 // 0.3 * 10^8
console.log(numero_grande, typeof numero_grande)

// Soma
console.log(0.1 + 0.3)
console.log( 10 +  7)
console.log( 10 + -7)
console.log(-10 +  7)
console.log(-10 + -7)

// Subtração
console.log( 10 -  7)
console.log( 10 - -7)
console.log(-10 -  7)
console.log(-10 - -7)

// Multiplicação
console.log(0.2 * 1.38)
console.log( 10 *  7)
console.log( 10 * -7)
console.log(-10 *  7)
console.log(-10 * -7)

// Divisão
console.log( 12 /  3)
console.log( 10 /  7)
console.log( 10 / -7)
console.log(-10 /  7)
console.log(-10 / -7)

// Potenciação
Math.pow(2, 5) // 2^5 = 32
Math.pow(3, 3) // 3^3 = 27
Math.sqrt(4) // 2
Math.sqrt(9) // 3

// Seno, Cons e Tangente
Math.PI
Math.sin(Math.PI/2) // 1
Math.cos(0) // 1
Math.tan(Math.PI/4) + Number.EPSILON// 1

```

Referências:
- [MDN -
  Math](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Math)
- [MDN -
  Number](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Number)

## Strings e Textos

```javascript
const uma_string = "uma String"
const outra_string = 'outra String'
const mais_uma_string = `mais ${uma_string}
string`

console.log(uma_string, outra_string, mais_uma_string)

// Converter texto para número
console.log(Number.parseInt('1234'))  // 1234
console.log(Number.parseInt('1.234')) // 1
console.log(Number.parseFloat('1.234')) // 1.234
console.log(Number.parseFloat('1234')) // 1234

// Métodos das strings
'abc'.at(1) // 'b'
'abc'.concat('d') // 'abcd'
'abc'.includes('b') // true
'abc'.includes('d') // false

'Era uma vez'.endsWith('vez') // true
'Era uma vez'.endsWith('Era') // false
'Era uma vez'.substr(4) // 'uma vez'
'Era uma vez'.substr(4, 3) // 'uma'

'João,Maria,José'.split(',') // ['a', 'b', 'c']
'  Oi, tudo bem?  '.trim() // 'Oi, tudo bem?'
'oi, tudo bão?'.toUpperCase() // 'OI, TUDO BÃO?'
'OI, TUDO BÃO'.toLowerCase() // 'oi, tudo bão'

```
Referências:
- [MDN -
  String](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/String)

## Boolean

```javascript
true // verdadeiro
false // falso

new Boolean(null) // false
new Boolean(undefined) // false
new Boolean(0) // false
new Boolean(1) // true
new Boolean('') // false
new Boolean('uma string') // true
new Boolean([]) // true
new Boolean({}) // true

// Operador Lógico "E" (and)

true  && true   // true
true  && false  // false
false && true   // false
false && false  // false

// Operador Lógico "OU" (or)
true  || true   // true
true  || false  // true
false || true   // true
false || false  // false

// Operador Lógico "Negação" (not)
! true  // false
! false // true
```

Referências:
- [MDN -
  Boolean](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Boolean)
- [MDN - Expressões e
  operadores](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Expressions_and_Operators#operadores_l%C3%B3gicos)

## Arrays

```javascript
const um_array = ['ele', 'pode', 'armazenar', 'strings', 'ou', 1, 2, 3, 'numeros', {um_objeto: true}, function () { console.log("funcao") }]
const outro_array = ['um', 'outro', 'array']

um_array[0] // 'ele'
um_array.length // 11
um_array[um_array.length] // undefined
um_array[um_array.length - 1]() // "funcao"

for (let i = 0; i < um_array.length; i++) {
  console.log(um_array[i])
}

for (let e of um_array) {
  console.log(e)
}

um_array.forEach(console.log)

um_array.includes('numeros') // true
um_array.includes('nao existe') // false
outro_array.join(' ') // 'um outro array'
```

Referências:
- [MDN - Array](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [MDN - for](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/for)
- [MDN - for...of](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/for...of)
- [MDN - Array.prototype.forEach](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
- [MDN - Espalhamento ...](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/Spread_syntax)

## Objetos

```javascript
const um_objeto = {
  uma_string: 'ele pode armazenar string',
  ou_um_numero: 1,
  ou_um_booleano: true,
  ou_um_array: [],
  ou_um_outro_objeto: {
    outro_objeto: true
  },
  ou_uma_funcao: function (){
    console.log("Sou uma função")
  },
  "você também pode usar caracteres especiais": "aqui"
}

um_objeto.uma_string
um_objeto["um_numero"]
um_objeto.ou_uma_funcao()
um_objeto["ou_uma_funcao"]()

for (let x of um_objeto) {
  console.log(`um_objeto['${x}'] = ${um_objeto[x]}`)
}
```

Referências:
- [MDN -
  Objetos](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Object)

## Expressões Regulares

```javascript
const regex1 = /ab+c/
const regex2 = new RegExp("ab+c");

console.log(regex1.test("abc")) // true
console.log(regex1.test("abbbbbbc")) // true
console.log(regex1.test("acb")) // false
```

Referências:
- [Regex101](https://regex101.com/)
- [MDN - Expressão regulares](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Regular_Expressions)


## Tratamento de erros

```javascript
try {
  console.log("Passou aqui")
  throw new Error("Deu um erro aqui!")
  console.log("Não passou aqui")
} catch (erro) {
  console.log("Peguei esse erro aqui:", erro);
} finally {
  console.log("Independente de ter ou não um erro, passa aqui")
}
```

Referências:
- [MDN - try...catch](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/try...catch)
- [MDN - throw](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/throw)
- [MDN - Error](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Error)

## Estruturas de Controle

```javascript
const pontuacao = 75;
if (pontuacao > 90) {
  console.log('Excelente!');
} else if (pontuacao > 75) {
  console.log('Muito bom!');
} else if (pontuacao > 60) {
  console.log('Bom.');
} else {
  console.log('Precisa melhorar.');
}

const pessoa = {
  nome: 'João',
  idade: 30,
  profissao: 'Desenvolvedor'
};
for (const chave in pessoa) {
  console.log(`${chave}: ${pessoa[chave]}`);
}

const frutas = ['Maçã', 'Banana', 'Pera'];
for (const fruta of frutas) {
  console.log(fruta);
}

let contador = 0;
while (contador < 3) {
  console.log(`While loop: contador vale ${contador}.`);
  contador++;
}

const dia = 4;
switch (dia) {
  case 1:
    console.log('Segunda-feira');
    break;
  case 2:
    console.log('Terça-feira');
    break;
  case 3:
    console.log('Quarta-feira');
    break;
  case 4:
    console.log('Quinta-feira');
    break;
  case 5:
    console.log('Sexta-feira');
    break;
  default:
    console.log('Final de semana!');
}

let contador = 0;
do {
  console.log(`Do while loop: contador vale ${contador}.`);
  contador++;
} while (contador < 3);

```

Referências:
- [MDN - if...else](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/if...else)
- [MDN - switch](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/switch)
- [MDN - while](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/while)
- [MDN - do...while](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/do...while)

## Funções

```javascript
function umaFuncao(x) {
  console.log('Essa é uma função:', x)
}

const funcaoAnonima = function(x) {
  console.log('Essa é uma função anônima:', x)
}

const funcaoFlexa = (x) => console.log('Essa é uma função flexa:', x)
const funcaoFlexa2 = (x) => { console.log(x) }
```

Referências:
- [MDN - Funções](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Functions)
- [MDN - arguments](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments)
- [MDN - IIFE](https://developer.mozilla.org/en-US/docs/Glossary/IIFE)
- [MDN - function*](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/function*)
- [MDN - async function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/async_function)
- [MDN - await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/await)

## Classes

```javascript
class UmaClasse {
  umAtributo;
  umAtributoComValor = 'valor';
  #umAtributoPrivado;

  constructor(x) {
    this.#umAtributoPrivado = x
  }

  get umAtributoPrivado() {
    console.log(`umAtributoPrivado ${this.#umAtributoPrivado}`)
    return this.#umAtributoPrivado;
  }

  set umAtributoPrivado(x) {
    this.#umAtributoPrivado = x
  }
}

```

Referências:
- [MDN -
  Classes](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Classes)
- [MDN - Private
  properties](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes/Private_properties)
- [MDN -
  constructor](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes/constructor)
- [MDN -
  get](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/get)
- [MDN -
  set](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/set)
