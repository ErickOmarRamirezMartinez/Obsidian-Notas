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

```











---
![[Pasted image 20240506125644.png]]
