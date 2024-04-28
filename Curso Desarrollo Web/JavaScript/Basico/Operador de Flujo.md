# Interpolacion de Cadenas

## Backticks
${}  Llamara a las variables
 ```javascript
 //backticks ``

let nombre = "Erick Omar";

let apellido = "Ramirez Martinez";

let mensaje = "Hola, soy " + nombre + " " +  apellido + " estoy en CH39";

//Con backtips

let mensajeB = `Holi , soy ${nombre} ${apellido} de la CH 39`;

  

console.log(mensaje);

console.log(mensajeB);
```

---

![[Pasted image 20240409102210.png]]
![[Pasted image 20240409102300.png]]

![[Pasted image 20240409102555.png]]![[Pasted image 20240409102707.png]]![[Pasted image 20240409102847.png]]![[Pasted image 20240409103330.png]]
```javascript
//Declaracion IF

  

let edad = 18;

  

if (edad >= 18) {

    console.log("Es mayor de edad");

} else {

    console.log("Es menor de edad");

}

  

if (edad != null) {

    console.log("El usuario iingreso su edad");

}else{

    console.log("Solicita la edad del usuario");

}
```

## Operador ternario
```JavaScript
//Operador ternario

// Es una forma concisa de escribir una sentencia condicional (if-else). Se utiliza los caracteres de ?: ára evaluar una condicion como true o false

// (condicion) ? true : false;

  

const num2 = 577;

  

console.log(num2 % 2 == 0 ? "El numero es par" : "El numero es impar");
```

## Else If
![[Pasted image 20240409115017.png]]

```JavaScript
//Else If

//Determinar si una persona es un bebe, un niño, un adolecente o un adulto con base en su edad.

  

let edad2 = 18;

  

if (edad2 >= 18) {

    if (edad2 < 60) {

        console.log("Es un adulto");

    } else {

        console.log("Es un adulto mayor");

    }

} else if(edad2 >=12) {

    console.log("Es un adolecente");

} else if (edad2 >=3){

    console.log("Es un niño");

} else{

    console.log("Es un bebe");

}
```

![[Pasted image 20240409122410.png]]

## * = Asignacion 

## * == Comparacion

## * === Comparacion estricta
Compara un valor y tipo de datos


``` JavaScript
  

// Determinar si un dia de la semana corresponde a dia laboral o fin de semana (sabado y domingo)

const diasemana = (finSemana) =>{

    let diasLibres = finSemana === "Sabado" || finSemana === "Domingo";

  

    if (diasLibres) {

        return "Es fin de semana";

    } else{

        return "Dias Laborables :C";

    }

};

let dia = "Martes"

console.log(diasemana(dia));
```



# Switch
Permite evaluar una exprecion y haceer coincidir el valor de la expresion con diferentes casos (case)
Se apoya como break y continue para frenar o continuar entre los diferentes casos
![[Pasted image 20240409124210.png]]
```JavaScript
//Switch

let diasemanas = "Domingo";

switch (diasemanas) {

    case "Lunes":

        console.log("Es un lunes");

        break;

    case "Martes":

        console.log("Es un martes");

        break;

    case "Miercoles":

        console.log("Es un miercoles");

        break;

    case "Jueves":

        console.log("Es un jueves");

        break;

    case "Viernes":

        console.log("Es un viernes");

        break;

    case "Sabado":

        console.log("Es un sabado");

        break;

    case "Domingo":

        console.log("Es un domingo");

        break;

    default:

        console.log("No es un dia de la semana");

        break;

}
```

![[Pasted image 20240409124459.png]]
![[Pasted image 20240409124846.png]]

```JavaScript
//Reto 1

function Impresion(mensaje) {

    console.log(`El numero es ${mensaje}`);

}

let numero = (numeroPI) =>{

    return numeroPI%2 ==0  ? "es par" : "es Impar";

}

Impresion(numero(4));

  
  

//Reto 2

//Utilizando esas dos variables, calcular la edad de una persona y decir si es mayor o no de edad

  

function Impresion2(mensaje) {

    console.log(`La fecha de Nacimiento es ${mensaje}`);

}

  

let operacion = (Naci) => {

    const today = new Date();

    let edad3 = today.getFullYear() - Naci;

  

    if (edad3 >= 18) {

        return `${Naci} tu edad es ${edad3} y Es mayor de edad`;

    } else {

        return `${Naci} tu edad es ${edad3} y Es menor de edad`;

    }

}

Impresion2(operacion(2002));
```