![[Pasted image 20240408162743.png]]

![[Pasted image 20240408162749.png]]

>Multlipes variables: Podemos trabajar con multlipes variables declarando y luego inicializando o declarando e inicializando dentro de la misma linea de codigo 

```javascript
let numeros = 12;

/* O podemos hacer de esta manera */

let numero1;

numero1 = 10;
```

### Console.log()
Es una herramienta que nos permite visualizar en consola la informacion que yo requiero

### Console.warn()
Nos va a mostrar un mensaje de advertencia 

### Console.error()
Nos va a mostrar un mensaje de error

### Console.table()
Nos muestra el mensaje en una tabla

---
# Operadores de Asignacion

![[Pasted image 20240408164829.png]]
![[Pasted image 20240408164833.png]]

![[Pasted image 20240408112830.png]]

---
# Encasillamiento
Es el proceso de convertir un valor de un tipo de dato en otro tipo

## Typeof
Metodo que nos va a ayudar a saber cual es el tipo de dato que estoy trabajando 


## Conversion numero a bolean

```JavaScript
//Conversion de number a boolean, siempre que el numero sea distinto a cero el resultado va a ser true

let cambioBolean = Boolean(numero);

console.log(typeof cambioBolean);
```
![[Pasted image 20240408123245.png]]

## De Boolean a String

```JavaScript
let mayordeEdad = true;

let converString = mayordeEdad.toString();

console.log(typeof converString);
```
![[Pasted image 20240408123347.png]]

## Conversion de String a Number

```JavaScript
let apellido = "Ramirez";

let cambioNumero = parseInt(apellido);

console.log(typeof cambioNumero);
```
![[Pasted image 20240408123256.png]]


## Ejercicios

```JavaScript
/*Ejercicio 1 Conversión a Booleano

Los valores "false" incluyen 0, "" (cadena vacía), null, undefined, NaN, y por supuesto, false.

*/

let valor = ""; // Prueba cambiando este valor por los ejemplos proporcionados

let resultadoBooleano = Boolean(valor);

console.log(typeof resultadoBooleano, resultadoBooleano);

  
  

/*Ejercicio 2 Conversión a Cadenas de Texto

Convierte diferentes tipos de datos a cadenas de texto.

Ejemplos de datos para convertir: true, false, 123, null, undefined.

*/

let valor2 = 1234; // Prueba cambiando este valor por los ejemplos proporcionados

let resultadoString = valor2.toString();

console.log(typeof resultadoString, resultadoString);

  

/*Ejercicio 3 Conversión a Números

Utiliza parseInt, parseFloat, y el constructor Number para convertir diferentes tipos de datos a números.

Ejemplos de datos para convertir: "123", "123.456", true, false, "abc".

*/

let valor3 = "123.213"; // Prueba cambiando este valor por los ejemplos proporcionados

let resultadoNumero = parseInt(valor3);

console.log(typeof resultadoNumero, resultadoNumero);

  

/*Desafío Adicional: Combinando Operaciones

Trata de combinar varias conversiones y operaciones en una sola línea de código

*/

let valorInicial = "123";

let resultadoComplejo = Boolean(parseInt(valorInicial) * 0);

console.log(typeof resultadoComplejo, resultadoComplejo);****
```
![[Pasted image 20240408132250.png]]

---

# Declarar y usar Funciones
![[Pasted image 20240408134741.png]]
![[Pasted image 20240408134909.png]]
## Funciones
Una función es un bloque de código reutilizable en el cual vamos a tener un conjunto de instrucciones/tareas que podemos ejecutar las veces que sea requerido invocando dicha función

* Reutilizable
* Modulariza el codigo
* Podemos hacer pruebas en codigos especifico

### Funcion de Declaracion
```JavaScript
//Funcion de Declaracion

function saludar(i) {

    console.log("Holi Crayoli "+i);

}

  

for (let i = 1; i < 5; i++) {

 saludar(i);

}
```

### Funcion de Retorno
```JavaScript
//Funcion de Retorno

function deRetorno() {

    return "Funcion que retorna";

}

console.log(deRetorno());
```


### Hoisting
Carcateristica de una funcion que nos permite invocarla antes de su inicializacion, es decir que se puede invacar antes del bloque de codigo o despues

```JavaScript
saluda();
```

## Funcion Flecha
Son funciones que no tienen nombre pero que se pueden invocar a través del nombre de la variable en la que se encuentra

```JavaScript
//Funcion Flecha

const calcularCuadrado = (number) => {

    return number * number;

}

let resCuadrado = calcularCuadrado(8);

console.log(resCuadrado);
```

## Funcion Anonima
Son funciones que no tienen un nombre pero que se pueden invocar a través del nombre de la variable en la que se encuentran 
```JavaScript
//Funciones Anonimas

const  sinNombre = function(){

    return "Esto es una funcion anonima";

}

console.log(sinNombre());
```

## Callback
Una función callback es una función que se pasa a otra función como argumento, la cual es luego invocada dentro de la función exterior para completar algún tipo de rutina o acción. En otras palabras, es una función que se entrega a otra para que la ejecute en un momento determinado.
```JavaScript
//Callbacks

const funcionB = function (){

    console.log("Esta es la funcion B");

}

  

const funcionA = function (callback){

    callback();


}

funcionA(funcionB);
```

Ejemplo:
```JavaScript
function hacerAlgo(resultado) {

    console.log("El resultado es: " + resultado);

}

  

function calcular(operacion, num1, num2, callback) {

    let resultado = operacion(num1, num2);

    callback(resultado);

}

  

// Uso de la función calcular con una función callback

calcular((x, y) => x + y, 5, 7, hacerAlgo); // Esto imprimirá "El resultado es: 12"
```

![[Pasted image 20240408165843.png]]