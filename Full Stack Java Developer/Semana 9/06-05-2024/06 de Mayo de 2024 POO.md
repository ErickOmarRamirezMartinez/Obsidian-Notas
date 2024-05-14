![[Pasted image 20240506100415.png]]![[Pasted image 20240506100506.png]]![[Pasted image 20240506100625.png]]
![[Pasted image 20240506101021.png]]}
![[Pasted image 20240506101053.png]]

>Documentacion
>[https://docs.oracle.com/javase/tutorial/java/concepts/class.html](https://docs.oracle.com/javase/tutorial/java/concepts/class.html "https://docs.oracle.com/javase/tutorial/java/concepts/class.html")


![[Pasted image 20240506101307.png]]


>[https://docs.oracle.com/javase/tutorial/java/concepts/object.html](https://docs.oracle.com/javase/tutorial/java/concepts/object.html "https://docs.oracle.com/javase/tutorial/java/concepts/object.html")


![[Pasted image 20240506101346.png]]
![[Pasted image 20240506101602.png]]
![[Pasted image 20240506101842.png]]
![[Pasted image 20240506102101.png]]
Por ejemplo, si tienes una clase llamada `Persona`, que define atributos como `nombre`, `edad`, y métodos como `hablar()` o `caminar()`, instanciar un objeto de esa clase sería crear una persona específica. En muchos lenguajes de programación, esto se hace usando la palabra clave `new` seguida del nombre de la clase y paréntesis. Aquí tienes un ejemplo básico en Java:


`Persona daniel = new Persona();`

En este código:

- `Persona` es el tipo de objeto que estás creando.
- `daniel` es el nombre del objeto (la instancia).
- `new Persona()` es la acción de crear el objeto. Aquí, `new` es una instrucción que le dice al programa que reserve memoria para un nuevo objeto `Persona`.

Una vez que has creado una instancia, puedes utilizar los métodos definidos en la clase para ese objeto y acceder o modificar sus atributos. Por ejemplo, si quieres que Daniel hable, podrías usar:

`daniel.hablar();`

![[Pasted image 20240506102208.png]]
![[Pasted image 20240506102521.png]]
![[Pasted image 20240506102548.png]]
![[Pasted image 20240506102556.png]]
![[Pasted image 20240506102630.png]]


---
# Pasos para Creacion Objeto
## 1.Declarar atributos

```Java
package org.generation.employee;

  

public class Employee {

//1.Declarar atributos

String nombre;

String apellido;

int edad;

double salario;

String puesto;
```

## 2. Metodo Constructor
```Java
//2. Metodo Constructor, no retorna nada, recibe parametros y argumentos que corresponden a los atributos y estos se guardan con la palabra reservada this.

public Employee(String nombre, String apellido, int edad, double salario, String puesto){

this.nombre = nombre;

this.apellido = apellido;

this.edad = edad;

this.salario = salario;

this.puesto = puesto;

}
```

>//Atajo para crear constructos.

```SH
//Click derecho en la clase

//Source

//Generate Constructor using Field
```

## 3. Metodo para acceder y modificar el objeto
```Java
public String getNombre() {

return nombre;

}

  

  

public void setNombre(String nombre) {

this.nombre = nombre;

}

  

  

public String getApellido() {

return apellido;

}

  

  

public void setApellido(String apellido) {

this.apellido = apellido;

}

  

  

public int getEdad() {

return edad;

}

  

  

public void setEdad(int edad) {

this.edad = edad;

}

  

  

public double getSalario() {

return salario;

}

  

  

public void setSalario(double salario) {

this.salario = salario;

}

  

  

public String getPuesto() {

return puesto;

}

  

  

public void setPuesto(String puesto) {

this.puesto = puesto;

}
```

## 4. Metodo para leer el objeto: toString con anotacion Override


```Java
@Override

public String toString() {

return "Employee "

+ "[nombre=" + nombre

+ ", apellido=" + apellido

+ ", edad=" + edad

+ ", salario=" + salario

+ ", puesto=" + puesto + "]";

}
```

# Como Instanciar un objeto

```Java
Employee daniel = new Employee ("Daniel", "Maldonado", 37, 2000d, "Instructor");

Employee erick = new Employee ("Erick", "Ramirez", 22, 10999d, "Tester QA");

Employee javier = new Employee ("Javier", "Cadena", 37, 6122.33d, "Data Analyst");

Employee lizeth= new Employee ("Lizeth", "Lopez", 25, 25837.12d, "DevOps");

System.out.println(daniel);

System.out.println(erick);

System.out.println(javier);

System.out.println(lizeth);
```

## Utilizando metodos de los objetos
```Java
erick.trabajar();

javier.informacion();

lizeth.calcularSalario();
```


## Utilizando su informacion y modificandola
```Java
//Utilizar informacion de los objetos (getters)

System.out.println(daniel.getNombre() + " "+ daniel.getApellido()+ " "+ "Trabaja como : "+ daniel.getPuesto());

System.out.println(javier.getNombre() + " "+ javier.getApellido() + " Tiene un Salario base de :"+javier.getSalario()+" Pero se le incrementaron $2000, quedando su salario en "+(javier.getSalario()+2000));

//Modificar informacion de los objetos (setters)

javier.calcularSalario(); //Aparece el mismo salario

double nuevoSalario = javier.getSalario()+2000;

javier.setSalario(nuevoSalario);

javier.calcularSalario();
```




---
![[Pasted image 20240506125644.png]]

## Ejercicio de Ejemplo

### Input User
```Java
package org.generation.letras;

import java.util.Scanner;

public class Letras {

/*

* Crear un programa que le solicite al usuario una cadena de texto y determine cuántas vocales, consonantes, números y simbolos tiene dicha entrada.

* Utiliza la tabla ASCII para desarrollarlo.

* Utiliza POO

* Refactorización y reutilización de código

* Datos primitivos, operadores.

* */

//En letras vamos a crear métodos que servirán para interactuar con el usuario

Scanner scanner = new Scanner(System.in);

//Método para retornar el scanner y poder usarlo las veces que quiera

public String leerEntrada() {

return scanner.nextLine();

}

//Método para dar contexto al usuario

public void mostrarMensaje(String mensaje) {

System.out.println(mensaje);

}

}
```

## Objeto
``` Java
package org.generation.letras;

  

public class Contador {

//Aqui vive la logica de mi programa:

//Determinar si es vocal, consonante , etc...

//-----Grupo 1 -> Metodos booleanos para determinar a que tipo de caracter corresponde

//-----Grupo 2 -> Metodos int que nos permiten contar dichos caracteres

//Grupo 1

public boolean esVocal(char caracter) {

return (caracter == 'a' || caracter == 'A' || caracter == 'e' || caracter == 'E' || caracter == 'i' || caracter == 'I' ||caracter == 'o' || caracter == 'O' ||caracter == 'u' || caracter == 'U');

}

public boolean esConsonante(char caracter){

//Casteo para poder utilizar tabla ASCII

short codigoASCII = (short) caracter;

return (((codigoASCII >= 65 && codigoASCII <=90)||codigoASCII>=97 && codigoASCII<=122) && !esVocal(caracter));

}

public boolean esNumero(char caracter) {

//Casteo para poder utilizar tabla ASCII

short codigoASCII = (short) caracter;

return ((codigoASCII >= 48 && codigoASCII <=57));

}

public boolean esSimbolo(char caracter) {

return !(esVocal(caracter) || esConsonante(caracter) || esNumero(caracter));

}

//Grupo 2

public int contarVocales(String texto) {

int vocales = 0;

for (char caracter : texto.toCharArray()) {

if (esVocal(caracter)) {

vocales++;

}

}

return vocales;

}

public int contarConsonantes(String texto) {

int consonantes = 0;

for (char caracter : texto.toCharArray()) {

if (esConsonante(caracter)) {

consonantes++;

}

}

return consonantes;

}

public int contarNumeros(String texto) {

int numero = 0;

for (char caracter : texto.toCharArray()) {

if (esNumero(caracter)) {

numero++;

}

}

return numero;

}

public int contarSimbolos(String texto) {

int simbolo = 0;

for (char caracter : texto.toCharArray()) {

if (esSimbolo(caracter)) {

simbolo++;

}

}

return simbolo;

}

}
```

## Instanciar el objeto
```Java
package org.generation.letras;

  

public class LetrasMain {

public static void main(String[] args) {

//Instancias Objetos

Letras letras = new Letras();

letras.mostrarMensaje("Escribe un texto para conocer el numero de vocales, consonantes, numero y simbolos que posee");

String texto = letras.leerEntrada();

Contador contador = new Contador();

int totalVocales = contador.contarVocales(texto);

System.out.println("Hay " + totalVocales + " vocales");

int totalConsonantes = contador.contarConsonantes(texto);

System.out.println("Hay "+ totalConsonantes + "consonantes");

int totalNumero = contador.contarNumeros(texto);

System.out.println("Hay "+ totalNumero + " numeros");

  

int totalSimbolos = contador.contarSimbolos(texto);

System.out.println("Hay "+ totalSimbolos + " simbolos");

}

}
```