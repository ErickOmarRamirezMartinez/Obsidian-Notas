![[Pasted image 20240429115758.png]]

https://docs.oracle.com/en/java/javase/17/docs/api/index.html

![[Pasted image 20240429120856.png]]

## Scanner
Clase que me permite interactuar con un usuario 
Debo definir el tipo de valor a leer

```Java
package org.generation.ControlDeFlujo;

  

import java.util.Scanner;

  

public class ControlDeFlujo {

public static void main(String[] args) {

Scanner scanner = new Scanner (System.in);

//Dar Contexto al Usuario

System.out.println("Ingresa tu nombre");

String nombre = scanner.next();

System.out.println("Ingresa tu Edad");

int edad = scanner.nextInt();

//Usando las dos variables

System.out.println("Hola "+nombre+" Tienes :"+edad+"Años");

//Utilizando un if, le solicite al usuario su nombre y edad.

//Si es Mayor de edad de 18 años se le autoriza, y si es menor se le niega

if(edad < 18) {

System.out.println(nombre + "No puedes comprar alcohol");

}else {

System.out.println(nombre+" Aqui tienes tu chelita");

}

}




scanner.close();
```

> Los scanner que abren
> Tiene que cerrarse 
> `scanner.close();`
### Bloque Switch
```Java
//Bloque Switch

//Solicite al usuario un numero

//De 1 a 7 de cada dia de la semana (1 = Lunes)

// Si no se elige un numerrcto envie un mensaje de advertencia

System.out.println("Ingresa un numero del 1 al 7 para conocer el dia de la semana");

int numeroDia = scanner.nextInt();

switch(numeroDia) {

case 1:

System.out.println("Lunes");

break;

case 2:

System.out.println("Martes");

break;

case 3:

System.out.println("Miercoles");

break;

case 4:

System.out.println("Jueves");

break;

case 5:

System.out.println("Viernes");

break;

case 6:

System.out.println("Sabado");

break;

case 7:

System.out.println("Domingo");

break;

default:

System.out.println("No es un numero valido");

break;

}
```

