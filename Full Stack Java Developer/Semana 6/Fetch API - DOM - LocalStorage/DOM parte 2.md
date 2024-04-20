## Objeto que contiene la información del usuario.

```JavaScript
const user = { 
username: "danieldlcm86", 
age: 37, 
email: "daniel@gmail.com", 
films: ["Se7en", "Interstellar", "Back to the Future", "End Game", "Terminator", "La La Land", "Rambo"] };
```

### Función para mostrar la información de un usuario en el DOM.
```JavaScript
// Función para mostrar la información de un usuario en el DOM. 
const crearUsuario = (user) => { 
/ Asignar los valores del objeto user a los elementos del DOM correspondientes. 

document.getElementById("name").textContent = user.username; 
/ Muestra el nombre de usuario. 

document.getElementById("age").textContent = user.age; 
/ Muestra la edad. 

document.getElementById("e-mail").textContent = user.email; 
/ Muestra el correo electrónico. 

// Crear y agregar la lista de películas al nodo correspondiente. 
const listaDesordenada = document.getElementById("films"); user.films.forEach(film => { 

const itemLista = document.createElement("li"); 
/ Crea un nuevo elemento <li> por cada película. 

itemLista.textContent = film; 
/ Asigna el nombre de la película al <li>. 

listaDesordenada.appendChild(itemLista); 
/ Agrega el <li> a la lista desordenada. 

}); 

// Estilos para la lista de películas. 

listaDesordenada.style.listStyleType = "none"; 
/ Remueve los marcadores de lista. 

listaDesordenada.style.padding = "0"; 
/ Elimina el padding. 

listaDesordenada.style.color = "coral"; 
/ Establece el color del texto de la lista. };
};

// Llamar a la función crearUsuario pasándole el objeto user. 
crearUsuario(user);
```