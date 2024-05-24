## Creacion de nuestra primer API

![[Pasted image 20240523114615.png]]
![[Pasted image 20240523114432.png]]
![[Pasted image 20240523114605.png]]


---
![[Pasted image 20240523120837.png]]

```java
package org.generation.user.model;

  

public class User {

// id, nombre, email, contraseña

private Long id;

private String nombre;

private String email;

private String contraseña;

public User(Long id, String nombre, String email, String contraseña) {

super();

this.id = id;

this.nombre = nombre;

this.email = email;

this.contraseña = contraseña;

}

  

public Long getId() {

return id;

}

  

public void setId(Long id) {

this.id = id;

}

  

public String getNombre() {

return nombre;

}

  

public void setNombre(String nombre) {

this.nombre = nombre;

}

  

public String getEmail() {

return email;

}

  

public void setEmail(String email) {

this.email = email;

}

  

public String getContraseña() {

return contraseña;

}

  

public void setContraseña(String contraseña) {

this.contraseña = contraseña;

}

  

@Override

public String toString() {

return "User [id=" + id + ", nombre=" + nombre + ", email=" + email + ", contraseña=" + contraseña + "]";

}

}
```

---
![[Pasted image 20240523120858.png]]
![[Pasted image 20240523135511.png]]

```java
package org.generation.user.service;

  

import java.util.ArrayList;

  

import org.generation.user.model.User;

import org.springframework.stereotype.Service;

  

//Para indicar que esta clase tomara la funcion de Servicio, utilizamos la anotacion @Services sobre la clase

  

@Service

  

public class UserService {

// No tenemos todavia Repository, vamos a instanciar un objeto de tipo User pero en forma de ArrayList, para poder simular una DB

public final ArrayList<User> usuarios = new ArrayList<User>();

public UserService() {

usuarios.add(new User(1L, "Mario Sandoval", "mario.sandoval@gmail.com", "mariobros"));

usuarios.add(new User(2L, "Daniel Maldonado", "daniel.cruz@gmail.com", "genmx"));

usuarios.add(new User(3L, "Fernanda Ramos", "fer.ramos@gmail.com", "hellokitty"));

usuarios.add(new User(4L, "Patricio Pina", "pato.pina@gmail.com", "patito"));

}

// Metodos para la logica del negocio. Aqui vive metodos relacionados al mapeo para acceder a la informacion (get)

public ArrayList<User> getUsuario(){

return usuarios;

}

// Mas adelante, aqui mismo, crearemos los otros metodos

// Por ejemplo; getByEmail, getByID, post , put, delete, putPassword, getAll

}
```

---
![[Pasted image 20240523135531.png]]

```java
package org.generation.user.controller;

  

import java.util.ArrayList;

  

import org.generation.user.model.User;

import org.generation.user.service.UserService;

import org.springframework.beans.factory.annotation.Autowired;

import org.springframework.web.bind.annotation.GetMapping;

import org.springframework.web.bind.annotation.RequestMapping;

import org.springframework.web.bind.annotation.RestController;

  

//Tengo que indicarle a SpringBoot que esta clase sera mi controlador, y que se mapeara los metodosdesde una API creada

// Indicando el endpoint el/los enpoint

  

  

// @RestController: me permite indicar qu es un controlador de tipo REST Api (trabaja con metodos HTTP)

// @RequestMapping: Vamos a contruir la ruta para acceder a nuestra API, indicando el endpoint especifico

// Vamos a instanciar un objeto de Service para poder acceder a los metodos de la logica del negocio

  

@RestController

@RequestMapping("/api/v1") //localhost:8080/api/v1

public class UserController {

// Instancia del objeto Service

private final UserService userService;

// Tengo que hacer una inyeccion de dependencias en un contructor de la clase con la anotacion @Autowired

@Autowired

public UserController(UserService userService) {

this.userService = userService;

}

// Metodo de mapeo especifico. Voy a crear un mapeo de tipo get, para ello utilizare la anotacion @GetMapping sobre el metodo

@GetMapping("/users") //localhost:8080/api/v1/users

public ArrayList<User> getAll(){

return userService.getUsuario();

}

}
```

---
![[Pasted image 20240523135601.png]]


Resumen y Analogía
Modelo (User.java): Es como la ficha de registro de un usuario en la biblioteca.
Servicio (UserService.java): Es como el bibliotecario que sabe cómo gestionar las fichas de los usuarios.
Controlador (UserController.java): Es como el mostrador de la biblioteca donde los usuarios pueden pedir información.
Aplicación Principal (UserApplication.java): Es como el interruptor que enciende toda la biblioteca digital.
Cuando ejecutas la aplicación (UserApplication.java), Spring Boot configura y ejecuta la aplicación web. Los usuarios pueden entonces acceder a localhost:8080/api/v1/users para obtener la lista de usuarios, gracias al controlador (UserController.java) que utiliza el servicio (UserService.java) para obtener los datos del modelo (User.java).

---
# PostMan
![[Pasted image 20240523140428.png]]


---
## Errores
![[Pasted image 20240523140625.png]]
![[Pasted image 20240523140643.png]]
![[Pasted image 20240523140658.png]]
![[Pasted image 20240523140706.png]]
