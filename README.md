# 30 Dias para aprender Javascript

## Por: Edier Dario Bravo Bravo

En este curso aprenderas JavaScriprt en 30 dias y 30 retos.

# DIA 1: [Curso Básico de JavaScript](https://platzi.com/cursos/basico-javascript/) 

## Variables

Las variables son ubicaciones de almacenamiento en la memoria de la computadora que se utilizan para guardar valores que se pueden utilizar más tarde en el programa. En JavaScript, existen 3 formas de declarar variables: var, let y const.

Las variables declaradas con var y let pueden cambiar su valor a lo largo del tiempo, mientras que las variables declaradas con const son constantes y no pueden cambiar su valor una vez asignado.

```js
// Variables que pueden cambiar con el tiempo
var edad = 30
let hora = 12

// Constante que no pueden cambiar
const nombre = "Platzi"
```

**Declarar e inicializar**
Declarar una variable es especificar su nombre sin asignarle ningún valor, esto solo se puede hacer con variables (let y var) debido a que const al no poder cambiar su valor, no podremos inicializarla sin declararla al mismo tiempo.

Inicializar una variable es el asignarles cualquier valor.

```js
// Declaración
var edad
let hora

// Inicialización
edad = 30
hora = 12

// Declaración & inicialización
const name = "Platzi"
```

## Funciones

Las funciones son una de las características más importantes y poderosas de JavaScript. Una función es un bloque de código que se puede reutilizar en diferentes partes de un programa.

Las funciones se usan para realizar una tarea específica y pueden recibir uno o más argumentos (también conocidos como parámetros dependiendo la situación) y pueden devolver un valor como resultado.

Se utiliza la palabra clave `function` para declarar una funcion

```js
function miFuncion(parametro1, parametro2) {
  // Código de la función
}
```

Para llama una funcion:

```js
miFuncion(valor1, valor2);
```

Las funciones también pueden devolver un valor como resultado usando la palabra clave return. El valor devuelto se puede asignar a una variable o utilizar en una expresión.

```js
function suma(a, b) {
  return a + b;
}

let resultado = suma(2, 3);
console.log(resultado); // Imprime 5
```

**Formas de hacer usu de funciones**
- Function declaration, que es la foma tradicional

    ```js
    function saludar() {
    console.log("Hola");
    };

    saludar();
    ```


- IIFE (Immediately Invoked Function Expression): una función que se autoejecuta inmediatamente después de ser definida. Esta función es anónima y no se puede reutilizar.

    ```js
    (function () {
    console.log("Soy una IIFE");
    })();
    ```

- Función expresión: una función que se define como una expresión y puede ser asignada a una variable. Esta función también puede ser llamada y reutilizada.

    ```js
    let saluda = function () {
    console.log("Hola");
    };

    saluda();
    ```

- Arrow function: una función que se define utilizando la sintaxis () =>. Esta función es una forma más concisa de escribir funciones y es útil para funciones de una sola línea.

    ```js
    let saluda = () => console.log("Hola");

    saluda();
    ```

## Sintaxis basica

**Punto y coma**
 Es opcional, a excepción de algunos casos especiales como en ciclos o cuando se quiere separar declaraciones en una misma línea.

**Corchetes o llaves {}**
Se utilizan para encapsular bloques de código, funciones, bucles y otros elementos en JavaScript. También se utilizan para declarar objetos

```js
const carro = {
  color: "rojo",
  llantas: 4,
  marca: "Audi"
}
```

## Tipos de datos

**Numbers**
Podemos crear números utilizando la notación numérica, que incluye dígitos y puede incluir un punto decimal para representar números con decimales.

```js
let edad = 30;
let salario = 1500.50;
const PI = 3.14;
```

También podemos utilizar la notación científica para representar números muy grandes o muy pequeños.

```js
const numeroGrande = 1e6; // 1 millón
const numeroPequeño = 1e-6; // 0.000001
```

**Strings**
Las cadenas de texto (strings) son un tipo de dato que representa una secuencia de caracteres. En JavaScript, podemos crear strings utilizando comillas simples o comillas dobles. 

```js
const nombre = "Platzi";
const apellido = 'Academy';
```

Podemos concatenar dos strings utilizando el operador +:

```js
console.log("Hola, " + nombre + " " + apellido + "!"); // "Hola, Platzi Academy!"
```

También podemos utilizar la notación template literal para crear strings que incluyen variables y expresiones:

```js
console.log(`Hola, ${nombre} ${apellido}!`); // "Hola, Platzi Academy!"
```

JavaScript proporciona una serie de métodos para manipular strings.

- length: Devuelve la longitud de un string.
- toUpperCase(): Devuelve el string en mayúsculas.
- toLowerCase(): Devuelve el string en minúsculas.
- substring(): Devuelve una parte del string.

```js
const nombre = "Platzi";

console.log(nombre.length) // 6
console.log(nombre.toUpperCase()) // PLATZI
console.log(nombre.toLowerCase()) // platzi
console.log(nombre.substring(0, 5)) // Platz
```

**Objects**
Los objetos son estructuras de datos que nos permiten almacenar un conjunto de pares clave-valor. Estos pares son conocidos como propiedades del objeto.

Para crear un objeto, debemos utilizar las llaves {} y especificar las propiedades del objeto mediante la sintaxis nombrePropiedad: valorPropiedad. Los valores de las propiedades pueden ser de cualquier tipo de dato, incluyendo otros objetos.

```js
const persona = {
    nombre: "Fulanita",
    platziRank: 9567,
    cursoFavorito: {
		nombre: "Básico de JavaScript",
		clases: 30,
		duración: "2 horas"
	}
};
```

Para acceder a las propiedades de un objeto, podemos utilizar el operador . o la notación de corchetes [].

```js
console.log(persona.nombre); // "Fulanita"
console.log(persona.cursoFavorito.nombre); // "Básico de JavaScript"
console.log(persona["platziRank"]); // 9567
```

**Booleanos**
Los valores booleanos (boolean) son un tipo de dato que representa un valor verdadero o falso. En JavaScript, podemos utilizar la palabra clave true para representar el valor verdadero y false para representar el valor falso.

```js
let cursoCompletado = true;
let lecturaCompletada = false;
```

**Null**
El valor null es un tipo de dato que representa un valor vacío o nulo. En JavaScript, podemos utilizar la palabra clave null para representar el valor nulo.

```js
const nombre = null;
console.log(nombre); // imprime "null"
```

**Undefined**
El valor undefined es un tipo de dato que representa un valor que aún no ha sido asignado o que no tiene un valor válido. En JavaScript, podemos utilizar la palabra clave undefined para representar el valor undefined.

```js
let nombre;
console.log(nombre); // imprime "undefined"
```

**Symbol**
Los simbolos son un tipo de dato único en JavaScript que se utiliza para crear identificadores únicos. Cada vez que se crea un símbolo, se genera un nuevo identificador único, lo que lo hace ideal para usar como claves de objetos o para identificar elementos de manera única en una aplicación.

```js
const simbolo = Symbol();

let perrito = {
  nombre: "Firulais",
  edad: 3,
  [simbolo]: "Identificador único"
};

console.log(perrito[simbolo]); // "Identificador único"
```

También puedes proporcionar una descripción opcional al crear un símbolo, lo que puede ser útil para depurar y mantener el código:

```js
const simbolo = Symbol("Identificador único de gatitos");
```

**BigInt**
Los bigint son un nuevo tipo de dato en JavaScript que se usa para representar números enteros de un tamaño mayor al que puede manejar JavaScript de manera nativa. Los bigint se escriben con el sufijo n, por ejemplo: 12345678901234567890n.

```js
const numeroGrande = 12345678901234567890n;

console.log(numeroGrande + 1n); // 12345678901234567891n
console.log(numeroGrande * 2n); // 2469135780246913578n
console.log(numeroGrande / 3n); // 411218936707805260n
```
Es importante tener en cuenta que los bigint solo pueden ser usados para operaciones matemáticas y no pueden ser usados con operadores de comparación, como == o ===. En su lugar, debes usar los métodos BigInt.asIntN y BigInt.asUintN para hacer comparaciones entre bigint y números normales.

También es importante tener en cuenta que los bigInt no son compatibles con todas las funciones y métodos de JavaScript que aceptan números, por lo que debes asegurarte de verificar la documentación de la función o método que quieres usar antes de intentar usar bigInt con ellos.


# DIA 2: [Curso Básico de JavaScript](https://platzi.com/cursos/basico-javascript/)

## Operadores

Los operadores son elementos de lenguaje que nos permiten realizar cálculos y comparaciones en JavaScript. 

**Operadores aritméticos**
Los operadores aritméticos nos permiten realizar operaciones matemáticas básicas, como la suma, la resta, la multiplicación y la división.

```js
// Suma
console.log(1 + 2); // 3

// Resta
console.log(5 - 2); // 3

// Multiplicación
console.log(3 * 4); // 12

// División
console.log(10 / 2); // 5

// Módulo (devuelve el resto de una división)
console.log(10 % 3); // 1
```

**Operadores de asignación**
Los operadores de asignación nos permiten asignar valores a variables.

```js
let x = 10;
x += 5; // x = x + 5
console.log(x); // 15

x -= 3; // x = x - 3
console.log(x); // 12

x *= 2; // x = x * 2
console.log(x); // 24

x /= 4; // x = x / 4
console.log(x); // 6
```

**Operadores de comparación**
Los operadores de comparación nos permiten comparar valores y nos devuelven true o false según el resultado de la comparación.

```js
console.log(1 < 2); // true
console.log(2 > 1); // true
console.log(1 <= 2); // true
console.log(2 >= 1); // true
console.log("2" != 2); // false, compara solo contenido
console.log(2 !== 2); // false, compara contenido y typo
console.log(1 == "1") // true, compara solo contenido
console.log(1 === "1") // false, compara contenido y typo
```

**Operadores lógicos**
Los operadores lógicos son aquellos que nos permiten realizar operaciones lógicas, es decir, comparaciones y evaluaciones. En JavaScript tenemos disponibles los siguientes operadores lógicos:

- AND (&&): Este operador lógico evalúa si ambas expresiones son verdaderas. Si ambas expresiones son verdaderas, devuelve true, de lo contrario, devuelve false.

- OR (||): Este operador lógico evalúa si al menos una de las expresiones es verdadera. Si al menos una de las expresiones es verdadera, devuelve true, de lo contrario, devuelve false

- NOT (!): Este operador lógico invierte el valor de la expresión. Si la expresión es verdadera, devuelve false, de lo contrario, devuelve true.

## Hoisting

El hoisting es un comportamiento de JavaScript en el que las declaraciones de variables y funciones son movidas al comienzo del ámbito actual antes de que cualquier otro código sea ejecutado. Esto significa que las declaraciones de variables y funciones pueden ser utilizadas antes de haber sido declaradas en el código.

```js
// codigo que se escribe
console.log(x);
var x = 5;

// como lo interpreta JavaScript
var x;
console.log(x);
x = 5;
```

## Coerción

Es el proceso en el cual JavaScript intenta convertir automáticamente un valor de un tipo a otro, para que puedan ser comparados o operados. Esto puede dar lugar a algunos resultados inesperados si no se tiene en cuenta.

**Alcance de las variables**

En este lenguaje existen dos tipos de scope (alcance) de variables: **global** y **local**.

Las variables declaradas fuera de cualquier función tienen alcance global, lo que significa que pueden ser accedidas y modificadas desde cualquier parte del código. Por otro lado, las variables declaradas dentro de una función tienen alcance local, lo que significa que solo pueden ser accedidas y modificadas dentro de esa función.

Es importante tener en cuenta que cuando se declara una variable con var dentro de una función, esta variable tendrá alcance global, aunque esté dentro de una función. Sin embargo, si se declara con let o const, la variable tendrá alcance local.

```js
const number1 = 10; // alcance global
let number2 = 20; // alcance global
var number3 = 30; // alcance global

function miFuncion(number1, number2, number3) {
    const number4 = 40; // alcance local
    let number5 = 50; // alcance local
    var number6 = 60;  // alcance global

    return true;
}

miFuncion();
```

# DIA 3: [Curso Básico de JavaScript](https://platzi.com/cursos/basico-javascript/)

## Condicionales

**if, if else, else**

La estructura de control “if” sirve para tomar decisiones en función de si una determinada condición es verdadera o falsa. 

```js
let calificacion = 75;

if (calificacion >= 90) {
  console.log("Obtuviste una A");
} else if (calificacion >= 80) {
  console.log("Obtuviste una B");
} else if (calificacion >= 70) {
  console.log("Obtuviste una C");
} else {
  console.log("Obtuviste una calificación insuficiente");
}
```

**switch**

La estructura de control switch permite ejecutar diferentes bloques de código en función de un valor específico.

```js
switch (variable) {
	case valor1:
	  // código a ejecutar si variable es igual a valor1
	  break;
	case valor2:
	  // código a ejecutar si variable es igual a valor2
	  break;
	default:
	  // código a ejecutar si variable no es igual a ninguno de los valores anteriores
}
```

## Ciclos

**for**

El ciclo “for” es utilizado para repetir un bloque de código un número específico de veces. Su sintaxis básica es la siguiente:

```js
for (inicialización; condición; actualización) {
  // código a ejecutar
}

for (let i = 1; i <= 10; i++) {
  console.log(i);
}
// 1
// 2
// 3
// 4
// 5
// 6
// 7
// 8
// 9
// 10
```

**for in**

El ciclo for-in se utiliza para recorrer las propiedades de un objeto

```js
const user = {
	name: "Pepito",
  age: 20,
  role: "JavaScript developer"
}

for (const prop in user) {
	console.log(user[prop])
}

// "Pepito"
// 20
// "JavaScript developer"
```

En este ejemplo, se establece una variable **`prop`** que se utilizará para recorrer las propiedades del objeto

**for of**

El ciclo for-of se utiliza para recorrer los elementos de una colección como un array

```js
const technologies = ["js", "html", "node", "php"]

for (const element of technologies) {
  console.log(element)
}

// "js"
// "html"
// "node"
// "php"
```

En este ejemplo, se establece una variable “element” que se utilizará para recorrer cada elemento en el array.

**while**

El ciclo while se utiliza para repetir un bloque de código mientras se cumpla una determinada condición. 

```js
while (condición) {
  // código a ejecutar
}

let i = 1;
while (i <= 10){
  console.log(i);
  i++;
}
```

**do while**

Similar al while, a diferencia que el código dentro del ciclo se ejecutará al menos una vez antes de evaluar la condición.

```js
let i = 1;
do {
  console.log(i);
  i++;
  } while (i <= 10);
```

# DIA 4: [Curso Básico de JavaScript](https://platzi.com/cursos/basico-javascript/)

## Arrays

son un tipo de objeto que permite almacenar una colección de valores. Estos valores pueden ser de cualquier tipo, como números, cadenas, objetos, incluso otros arrays.

```js
let miArray = [valor1, valor2, valor3];
```

**Metodo push()**

Este método permite agregar un nuevo elemento al final del array.

```js
colores.push("amarillo");
console.log(colores); // ["rojo", "azul", "verde", "amarillo"]
```

**Metodo pop()**

Permite eliminar el último elemento del array

```js
colores.pop();
console.log(colores); // ["rojo", "azul", "verde"]
```

**Metodo map()**

Permite aplicar una función a cada elemento del array y devolver un nuevo array con los valores modificados.

```js
const numeros = [1, 2, 3, 4, 5];
const cuadrados = numeros.map(function(numero) {
  return numero * numero;
});
console.log(cuadrados); // [1, 4, 9, 16, 25]
```

**Metodo reduce()**

Permite combinar todos los elementos del array en un solo valor.

```js
const suma = numeros.reduce(function(acumulador, numero) {
  return acumulador + numero;
}, 0);
console.log(suma); // 15
```

Existen muchos otros métodos populares en los arrays de JavaScript, como “filter()”, “sort()” y “slice()”

## Objetos

Los objetos en JavaScript son un tipo de dato que permite almacenar una colección de pares clave-valor. Estos pares representan las propiedades y sus valores correspondientes de un objeto. Los objetos son similares a los arrays en cuanto a que también son una forma de almacenar y manejar datos, pero en lugar de tener un índice numérico, tienen una clave de string.

```js
const miObjeto = {
	clave1: valor1, 
	clave2: valor2, 
	clave3: valor3
};
```

Por ejemplo, el siguiente código crea un objeto llamado “curso” que tiene cinco propiedades: “Clases”, “Duración”, “Nombre”, “detalles” y comentarios:

```js
const curso = {
	nombre: "30 días de JS", 
	duración: "20 horas", 
	clases: 100,
	detalles: {
		tecnologias: ["js", "node", "web browser"],
		calificacion: 5,	
	},
	comentarios: ["¡Excelente curso!", "Javscript no es lo mismo que Java", "hola"]
};
```

Para acceder a las propiedades de un objeto, se utiliza la notación de punto o la notación de corchetes.

```js
console.log(curso.nombre); // "30 días de JS"
console.log(curso["nombre"]); // "30 días de JS"
```

**Ejercicio desarrollado**

```js
function getStudentAverage(students) {
  let avgTotal = 0;
  var outPut = {};
  var averageEstudents = students.map(function (student) {

    var avg = student.grades.reduce(function (a, b) {
      return a + b;
    }, 0) / student.grades.length;

    avg = Number(avg.toFixed(2));
    avgTotal = avgTotal + avg;
    delete student.grades;
    student.average = avg;

    return student;
  });

  outPut.classAverage = Number((avgTotal / students.length).toFixed(2));
  outPut.students = averageEstudents;
  return outPut;
}

var estu = [
  { name: "Diego", grades: [90, 87, 88, 90] },
  { name: "Maria", grades: [90, 87, 88, 90] },
  { name: "Luis", grades: [90, 87, 88, 90] },
];

console.log(getStudentAverage(estu));

```

# DIA 5: [Curso Básico de JavaScript](https://platzi.com/cursos/basico-javascript/)

**Ejercicio desarrollado**

Se crea una función que encuentra el palíndromo más largo en una lista de palabras.

Se recibe un único parámetro: un array de palabras. Si no hay ningún palíndromo en la lista, la función devuelve null. Si hay más de un palíndromo con la misma longitud máxima, se devuelve el primer palíndromo encontrado en la lista.

Un palíndromo es una palabra que se puede leer de la misma manera tanto hacia adelante como hacia atrás.

```js
function findLargestPalindrome(words) {
  // Tu código aquí 👈
  let wordMax = null;
  let maxlength = 0;
  for (let word of words) {
    let wordInverse = word.split("").reverse().join("");
    if (word == wordInverse && word.length > maxlength) {
      wordMax = word;
      maxlength = word.length;
    }
  }

  return wordMax;
}

findLargestPalindrome(["racecar", "level", "world", "hello"]);
```

# DIA 6: [Curso de Closures y Scope en JavaScript](https://platzi.com/cursos/javascript-closures-scope/)