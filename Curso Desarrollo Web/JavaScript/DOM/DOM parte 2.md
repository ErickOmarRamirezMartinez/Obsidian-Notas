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


---
### Modificación de Información Mediante Eventos

La manipulación de la información en el DOM utilizando eventos es una práctica común en JavaScript para hacer las páginas interactivas. En este caso, el código que tienes establece un mecanismo para actualizar la información de un usuario basado en los valores ingresados en los campos de un formulario. Aquí te dejo las notas detalladas sobre cada parte:

1. **Selección de Elementos del DOM:**
    
    - Utilizas `document.getElementById` para obtener referencias a los elementos del DOM que manipularás. Esto incluye inputs del usuario y lugares donde mostrarás los nuevos valores.
2. **Creación de Event Listeners:**
    
    - `buttonActualizar.addEventListener("click", callback)` agrega un listener de evento al botón que espera un clic para ejecutar una función. Es crucial en interfaces de usuario interactivas.
3. **Función de Actualización en el Evento:**
    
    - Dentro de la función de callback del evento de clic, actualizas el `textContent` de los elementos seleccionados con los valores obtenidos de los `input`. Esto modifica directamente el contenido del DOM, mostrando los nuevos valores en la página.

```Javascript
/*

Crear funcion para que, mediante eventos, se modifique la informacion tomando el valor de los inputs

  
  

*/

// Obtiene los elementos de entrada y el botón de la interfaz de usuario

const inputUsername = document.getElementById("username");

const inputEmail = document.getElementById("email");

const buttonActualizar = document.getElementById("button--main");

  
// Elementos del DOM donde se mostrarán los valores actualizados
const nuevoUsername = document.getElementById("name");

const nuevoEmail = document.getElementById("e-mail");

  

// Añade un 'listener' al botón para manejar clics
buttonActualizar.addEventListener("click", () => {

// Actualiza el contenido de texto de los elementos con los valores de los inputs
    nuevoUsername.textContent = inputUsername.value;

    nuevoEmail.textContent = inputEmail.value;

  

});
```


---
### Concepto de Expresiones Regulares

Las expresiones regulares son secuencias de caracteres que forman un patrón de búsqueda, y se utilizan principalmente para la búsqueda de patrones de cadenas de texto. Son muy útiles para la validación de formatos en entradas de datos, como emails, números de teléfono, etc.

### Detalles del Código

1. **Selección de Elementos del DOM:**
    
    - `document.getElementById('email')` obtiene el elemento input para el email.
    - `document.getElementById('button--login')` obtiene el botón de login.
2. **Inicialización de Estado del Botón:**
    
    - `buttonLogin.disabled = true;` inicialmente deshabilita el botón de login hasta que se cumpla la condición de validación.
3. **Creación de la Expresión Regular:**
    
    - `const emailRegex = /^[\w.+\-]+@gmail.com$/;` define una regex para validar que el email ingresado termine en "@gmail.com". La regex asegura que la parte local del email puede incluir letras, números, puntos, guiones y signos de suma.
4. **Evento de Entrada y Validación:**
    
    - `emailInput.addEventListener('input', (event) => {...});` añade un 'listener' al campo de entrada del email para reaccionar a cada cambio (cada vez que el usuario escribe algo).
5. **Función de Validación:**
    
    - Dentro del evento, cada vez que cambia el input:
        - Se captura el valor actual del input con `event.target.value`.
        - Se evalúa este valor con la regex. Si cumple con el patrón (`emailRegex.test(email)`), el botón se habilita. Si no, permanece deshabilitado.

```JavaScript
// Obtención de elementos del DOM
const emailInput = document.getElementById('email');
const buttonLogin = document.getElementById('button--login');


// Deshabilita el botón inicialmente
buttonLogin.disabled = true;


// Definición de la regex para validar emails de Gmail
const emailRegex = /^[\w.+\-]+@gmail.com$/

  
  

//Creear evento para input, el cual va evaluar el patron regex y en caso de cumplir con el, habilita el boton y poodemos movernos a App.html

  

//1.Obtenemos el valor del input utilizaando ee.target.value y lo almcacenamos en una variable

  

//2. Se evalua mediante una condicional

  
// Listener para validar el input de email en tiempo real
emailInput.addEventListener('input', (event) => {

    const email = event.target.value;

  
	// Habilita el botón solo si el email cumple con la regex de Gmail
    if (emailRegex.test(email)) {

        buttonLogin.disabled = false;

    } else {

        buttonLogin.disabled = true;

    }

});
```