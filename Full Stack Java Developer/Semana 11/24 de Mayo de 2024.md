![[Pasted image 20240524100507.png]]
![[Pasted image 20240524100544.png]]
![[Pasted image 20240524100736.png]]

Aprender arquitectura monolitica
y despues
metete a microservicios
![[Pasted image 20240524101827.png]]
![[Pasted image 20240524101839.png]]
![[Pasted image 20240524101900.png]]
![[Pasted image 20240524102227.png]]
![[Pasted image 20240524102255.png]]
https://www.geeksforgeeks.org/introduction-to-large-objects-lobs/  

https://www.geeksforgeeks.org/blob-full-form/  
  
https://hibernate.org/

![[Pasted image 20240524102317.png]]

![[Pasted image 20240524102357.png]]

https://hibernate.org/  
https://www.ibm.com/docs/es/was-liberty/nd?topic=overview-java-persistence-api-jpa

![[Pasted image 20240524102555.png]]
![[Pasted image 20240524102737.png]]



---
![[Pasted image 20240524104626.png]]
![[Pasted image 20240524104618.png]]

---
## Signup.java
Mappeo de nuestra base de datos

![[Pasted image 20240524115455.png]]

```java
package com.pandevs.userPandevs.model;

  

import java.util.Objects;

  

import jakarta.persistence.Column;

import jakarta.persistence.Entity;

import jakarta.persistence.GeneratedValue;

import jakarta.persistence.GenerationType;

import jakarta.persistence.Id;

import jakarta.persistence.Table;

  

/*

JPA. Para aplicar JPA en nuestro modelo, debemos agregar algunos metodos nuevos (podemos generarlos automaticamente) y tenbemos que agregar anotaciones

Metodos para JPA

1.- Contructor Vacio. JPA necesita un constructor vacio para contruir cualquier objeto sin tomar en cuenta sus atributos

2. hasCode() . Nos va a permitir comparar para evitar duplidicidad en los objetos

3.- equals() **** objetos.

Anotaciones (@)

@Entity para indicar que esta clase es una entidad OMR que se ma a moderar como un obnjeto relacional (va a pasar ser una tabla en mi base de datos)

@Table(name = "tablename", schema = "db") puede recibir parametros o propiedades

@Id . Indicar una llave primaria (PK) .

@GenerateValue() . Indica la manera en la que se genera el atributo en las tablas.

@Column . Nos permite configurar el atributo de Java con las propiedades que debe tener en la columna de la tabla de la DB

*/

@Entity

@Table(name="user")

public class Signup {

S

@Id

@GeneratedValue(strategy = GenerationType.IDENTITY)

@Column(name = "id")

private Long id;

@Column(name = "username", length = 60, nullable = false, unique = true)

private String username;

@Column(name = "email", length = 100, nullable = false, unique = true)

private String email;

@Column(name = "password", length = 250, nullable = false, unique = false)

private String password;

// Contructor Vacio para JPA

public Signup() {

}

  

// Constructor

public Signup(Long id, String username, String email, String password) {

super();

this.id = id;

this.username = username;

this.email = email;

this.password = password;

}

// Getteres and setters

public Long getId() {

return id;

}

  

public void setId(Long id) {

this.id = id;

}

  

public String getUsername() {

return username;

}

  

public void setUsername(String username) {

this.username = username;

}

  

public String getEmail() {

return email;

}

  

public void setEmail(String email) {

this.email = email;

}

  

public String getPassword() {

return password;

}

  

public void setPassword(String password) {

this.password = password;

}

// To String

@Override

public String toString() {

return "Signup [id=" + id + ", username=" + username + ", email=" + email + ", password=" + password + "]";

}

  

//hashcode()

@Override

public int hashCode() {

return Objects.hash(email, id, password, username);

}

  

//equals()

@Override

public boolean equals(Object obj) {

if (this == obj)

return true;

if (obj == null)

return false;

if (getClass() != obj.getClass())

return false;

Signup other = (Signup) obj;

return Objects.equals(email, other.email) && Objects.equals(id, other.id)

&& Objects.equals(password, other.password) && Objects.equals(username, other.username);

}

}
```



---
## Primera Opcion
![[Pasted image 20240524115917.png]]
![[Pasted image 20240524120214.png]]
![[Pasted image 20240524123215.png]]
```yml
server:

port: 8081

  

spring:

application:

name: userPandevs

datasource:

url: jdbc:mysql://localhost:3306/pandevs

username: root

password: $Papaso00

jpa:

hibernate:

ddl-auto: create
```


---
## Creamos una base de datos llamada pandevs
![[Pasted image 20240524123339.png]]
![[Pasted image 20240524123351.png]]


---
## Salida
![[Pasted image 20240524123245.png]]
![[Pasted image 20240524123255.png]]

---
Y si se crea la tabla con los atributos y elementos incluidos automaticamente
![[Pasted image 20240524123423.png]]
![[Pasted image 20240524124346.png]]

---

## Actualizamos de Create a Update
![[Pasted image 20240524141459.png]]

---
![[Pasted image 20240524141540.png]]


---
