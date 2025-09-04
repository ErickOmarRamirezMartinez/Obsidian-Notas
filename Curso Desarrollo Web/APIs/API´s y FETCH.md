[Regex Cheat Sheet (rexegg.com)](https://www.rexegg.com/regex-quickstart.html)

![[Pasted image 20240416153320.png]]
![[Pasted image 20240416153601.png]]
![[Pasted image 20240416153721.png]]![[Pasted image 20240416153915.png]]
![[Pasted image 20240416161551.png]]
![[Pasted image 20240416163456.png]]
![[Pasted image 20240416163838.png]]
![[Pasted image 20240416164051.png]]

![[Pasted image 20240416164233.png]]
![[Pasted image 20240416164239.png]]
![[Pasted image 20240416164341.png]]
![[Pasted image 20240416164549.png]]

### Sincronía

En la parte sincrónica de tu código, las funciones se ejecutan en el orden en que se llaman. Esto significa que JavaScript espera a que una función complete su ejecución antes de comenzar la siguiente. Aquí está el desglose:

```JavaScript
function primerFuncion(){ 
	console.log("2"); 
} 

function segundoFuncion(){ 
	console.log("1"); console.log("3"); primerFuncion(); 
}

segundoFuncion();
```

- `segundoFuncion()` se llama primero y dentro de ella, se ejecutan dos `console.log` ("1" y "3") antes de llamar a `primerFuncion()`.
- `primerFuncion()` simplemente imprime "2".

El orden de impresión será 1, 3, 2, siguiendo estrictamente el orden de las llamadas.

### Asincronía

La asincronía permite que JavaScript ejecute operaciones en segundo plano, sin bloquear la ejecución principal del programa. Esto se demuestra mediante el uso de `setTimeout`, que retrasa la ejecución de una función por un número especificado de milisegundos. Aquí te explico el código asincrónico:

```JavaScript
const firstFunction = () => { 
setTimeout(() => { 
console.log("2"); 

}, 2500); // Se ejecuta después de 2.5 segundos 
} 

const secondFunction = () => { 
	setTimeout(() => { 
		console.log("1"); }, 
	5000); // Se ejecuta después de 5 segundos 
	console.log("3"); 
	firstFunction(); 
} 

secondFunction();
```

- `secondFunction()` se invoca primero. Dentro de ella, `setTimeout` retrasa la impresión de "1" hasta después de 5 segundos.
- Sin embargo, antes de eso, imprime "3" directamente, porque `console.log("3")` no está dentro de un `setTimeout`.
- Luego llama a `firstFunction()`, que programa "2" para imprimirse después de 2.5 segundos.

El orden de impresión en este caso será "3", "2", "1". Esto muestra cómo la asincronía puede alterar el orden secuencial de ejecución de las operaciones:

1. "3" se imprime inmediatamente cuando se ejecuta `secondFunction()`.
2. "2" se imprime después de 2.5 segundos porque `firstFunction()` se llama inmediatamente después de imprimir "3", pero su contenido se retrasa.
3. "1" se imprime después de 5 segundos, a pesar de estar en la función que se llamó primero, debido a su mayor retraso en `setTimeout`.

---
# Trabajando con promesas mediante FetchAPI

### Uso de Fetch API con Promesas

1. **Inicio de la Solicitud Fetch:**
    
    - `const url = 'https://jsonplaceholder.typicode.com/users';`
    - Aquí, `fetch(url)` inicia una solicitud GET a la URL proporcionada, que es un recurso que devuelve datos de usuarios en formato JSON. `fetch()` devuelve una promesa que se resuelve en una respuesta de la red, ya sea exitosa o no.
2. **Procesamiento de la Respuesta:**
    
    - `.then(response => response.json())`
    - Este primer `.then()` recibe el objeto `Response` proporcionado por `fetch` y usa el método `.json()` para leer el cuerpo de la respuesta y convertirlo en un objeto JSON. Este método también devuelve una promesa que se resuelve con el resultado de la parseada del texto JSON.
3. **Uso de los Datos JSON:**
    
    - `.then(response => {...})`
    - Aquí manejas la data JSON ya parseada. `response` es ahora un array de objetos, cada uno representando un usuario.
    - `console.log(response);` imprime la lista completa de usuarios.
    - `console.log(response[0]);` muestra los datos del primer usuario (con índice 0).
    - `console.log(response[5].name);` accede directamente al nombre del sexto usuario en la lista (índice 5) y lo imprime.
4. **Manejo de Errores:**
    
    - `.catch(error => console.log("No funciono mi chavo", error));`
    - El método `.catch()` es crucial para manejar errores que pueden ocurrir durante la solicitud fetch o en las promesas anteriores del chain. Aquí, imprime un mensaje personalizado seguido del error que proporciona más detalles sobre lo que salió mal.

```JavaScript
const url = `https://jsonplaceholder.typicode.com/users`;

fetch(url)

    //La funcion de tipo callback se va a ejecutar siempre que la promesa se resuelva y se convierte en tipo String

    .then(response => response.json())

  

    .then(response => {

        console.log(response);

        //Traer el usuario con id 1

        console.log(response[0]);

  

        //Traer el namee del usuario con id 5

        console.log(response[5].name);

    })

  

    //Si se rechaza me muestra este mensaje de error

    .catch(error => console.log("No funciono mi chavo",error));
```

---
# Manipulación dele DOM para mostrar en el navegador

## Metodo GET
### Estructura del Código y Explicación

1. **Selección de Elementos del DOM:**
    
    - `const botonInfo = document.querySelector('#button--info');` y `const contenedorInfo = document.querySelector('#div--info');`
    - Estas líneas seleccionan elementos del DOM que se usarán más adelante para disparar eventos y para mostrar la información.
2. **Inicialización de la Variable para Almacenar Datos:**
    
    - `let post = null;`
    - Aquí se declara una variable que eventualmente almacenará los datos de un usuario obtenidos de la API.
3. **Función para Mostrar los Datos:**
    
    - `const mostrarDatos = (post) => {...}`
    - Esta función crea nuevos nodos en el DOM para cada dato relevante (`name`, `username`, `email`, `phone`) y los inserta en el contenedor especificado.
    - Se utilizan métodos como `document.createElement` y `innerText` para crear y configurar los elementos del DOM.
4. **Consumo de la API con Fetch y Evento:**
    
    - `botonInfo.addEventListener("click", () => {...});`
    - Este bloque de código agrega un evento de clic al botón, lo que inicia una solicitud Fetch cuando se presiona el botón.
    - La función `fetch('https://jsonplaceholder.typicode.com/users/8')` inicia una solicitud GET a la URL, que devuelve los datos del usuario con el id 8.
    - `.then(response => response.json())` convierte la respuesta en formato JSON.
    - En el segundo `.then`, se actualiza la variable `post` con los datos del usuario y se llama a `mostrarDatos` para actualizar el DOM con esta nueva información.
    - `.catch(error => console.log("No funciono mi chavo",error));` captura y maneja errores que puedan surgir durante la solicitud o el procesamiento de datos.

### Explicación Detallada del Manejo de Datos y Errores

- **Datos Dinámicos en el DOM:** La función `mostrarDatos` manipula el DOM en tiempo real, permitiendo que la página web se actualice sin necesidad de recargar. Esto es crucial para crear aplicaciones web interactivas y responsivas.
- **Manejo de Errores:** Utilizar `.catch` para manejar errores es una práctica esencial, ya que permite gestionar fallos en la red o problemas con el servidor de manera que la experiencia del usuario no se vea significativamente afectada.


```JavaScript
//Metodo GET

//1. Guardar los elementos en constantes

const botonInfo = document.querySelector('#button--info');

  

const contenedorInfo = document.querySelector('#div--info');

  

//2. Crear una variable de tipo NULL para guardar la info que vamos a traer de la API

let post = null;

  

//3.Crear una funcion que tome la variable post y me permita manipular el DOM. Vamos a crear nodos y vamos a insertarlos en el ParentNode.

//De mi objeto en la API voy a traer las llaves 'name, phone, email, username'

  

const mostrarDatos = (post) => {

    //Crear nodos

    const name = document.createElement("h2");

    const username = document.createElement("h3");

    const email = document.createElement("p");

    const phone = document.createElement("p");

  

    //Meterles Info (InnerHTML de las key del objeeto)

    name.innerText = post.name;

    username.innerText = post.username;

    email.innerText = post.email;

    phone.innerText = post.phone;

  

    //Mostrarlos en navegador al insertarlos en su ParentNode

    contenedorInfo.appendChild(name);

    contenedorInfo.appendChild(username);

    contenedorInfo.appendChild(email);

    contenedorInfo.appendChild(phone);

};

  

//4. Consumir API con fetch y evento (Metodo GET)

botonInfo.addEventListener("click", () => {

    fetch('https://jsonplaceholder.typicode.com/users/8')

    //La funcion de tipo callback se va a ejecutar siempre que la promesa se resuelva y se convierte en tipo String

    .then(response => response.json())

    //Traer el usuario con id 1

    .then(response => {

        //Guardo los datos obtenidos de la promesa en mi variable null

        post = response;

        mostrarDatos(post);

    })

    //Si se rechaza me muestra este mensaje de error

    .catch(error => console.log("No funciono mi chavo",error));

});
```

---
# Metodo POST con fetch API
### Estructura del Código y Explicación

1. **URL de la API:**
    
    - `const urlPost = 'https://jsonplaceholder.typicode.com/posts';`
    - Esta es la URL del endpoint al que se enviarán los datos. En este caso, es un endpoint de prueba proporcionado por JSONPlaceholder.
2. **Configuración de la Solicitud Fetch:**
    
    - `fetch(urlPost, { ... })`
    - Aquí, `fetch` se utiliza para realizar una solicitud POST. La función recibe dos argumentos: la URL y un objeto de configuración.
3. **Objeto de Configuración:**
    
    - `method: "POST"`: Define el tipo de método HTTP de la solicitud, en este caso, POST.
    - `headers: { 'Content-Type': 'application/json; charset=UTF-8' }`: Establece los headers necesarios para la solicitud. Aquí, se indica que el contenido enviado está en formato JSON.
    - `body: JSON.stringify({ ... })`: El cuerpo de la solicitud, que es el contenido que deseas enviar. `JSON.stringify` convierte un objeto JavaScript en una cadena JSON.
4. **Datos Enviados en el Body:**
    
    - Se crea un objeto con los datos `userID`, `id`, `title`, y `body`. Nota que `id` se menciona como autoincrementable, lo que generalmente significa que el servidor puede ignorarlo o sobrescribirlo, dependiendo de la configuración del backend.
5. **Procesamiento de la Respuesta:**
    
    - `.then(response => response.json())`: Convierte la respuesta recibida del servidor en formato JSON.
    - `.then(response => { console.log(response); })`: Imprime la respuesta convertida a la consola. Esto es útil para verificación y depuración.
6. **Manejo de Errores:**
    
    - `.catch(error => console.log("No funciono mi chavo", error));`: Captura y maneja cualquier error que ocurra durante la solicitud o el procesamiento de la respuesta.

### Consideraciones y Mejores Prácticas

- **Validación de Respuesta:** Es importante verificar que la respuesta del servidor es la esperada (p.ej., revisando el código de estado de la respuesta).
- **Manejo de Errores:** Deberías manejar errores específicos, como errores de red o errores HTTP (p.ej., que la respuesta tenga un código de estado 4xx o 5xx).
- **Seguridad y Privacidad:** Asegúrate de que los datos enviados no contengan información sensible sin el debido cifrado o medidas de protección, especialmente cuando no controlas el backend.
```JavaScript
//----------------------Metodo POST con fetch API---------------------------
const urlPost = 'https://jsonplaceholder.typicode.com/posts';

fetch(urlPost, {

    //Indicamos que esta promesa es de tipo POST

    method: "POST",

    //Definir Headers

    headers: {

        'Content-Type': 'application/json; charset=UTF-8'

    },

    //Definir Body que debe coincidir con mi API, para ello le paso un metodo stringify que me permite transformar el objeto en formato JSON

    body: JSON.stringify({

        userID: 1986,

        id: 25365,// Es AutoIncrementable, entonces no se visualiza

        title: "Un nuevo elemento en la API",

        body: "Estoy enviando un nuevo objeto de tipo JSON a la API de Jsonplaceeholder utilizando el metodo POST"

    })
})

.then(response => response.json())

  

.then(response => {

    console.log(response);

})
 
.catch(error => console.log("No funciono mi chavo",error));
```

---
# Programacion Asincrona

## En Async tenemos funciones de tipo async-await
### Estructura del Código y Explicación

1. **Definición de la Función Asíncrona:**
    
    - `const getUser = async () => { ... };`
    - Aquí se define una función asincrónica llamada `getUser`. La palabra clave `async` antes de la función la transforma en una función que devuelve una promesa.
2. **Manejo de Promesas con `await`:**
    
    - Dentro de la función, se utiliza `await` para pausar la ejecución de la función hasta que la promesa se resuelva o rechace. Esto hace que el código asincrónico se lea de manera más sincrónica, o lineal.
3. **Realización de la Solicitud Fetch:**
    
    - `const response = await fetch("https://jsonplaceholder.typicode.com/users/8");`
    - Se realiza una solicitud `fetch` a un recurso de la API y se espera por la respuesta. La función `fetch` devuelve una promesa, la cual es manejada con `await`.
4. **Conversión de la Respuesta a JSON:**
    
    - `const data = await response.json();`
    - Una vez que se recibe la respuesta, se utiliza `await` nuevamente para esperar a que el contenido de la respuesta sea convertido de un stream JSON a un objeto JavaScript.
5. **Impresión de Datos:**
    
    - `console.log(data);`
    - Después de obtener y procesar la data, se imprime en la consola. Esto es útil para verificar que la data recibida es la esperada.
6. **Manejo de Errores con Bloques `try-catch`:**
    
    - `try { ... } catch (error) { ... }`
    - El bloque `try-catch` permite manejar excepciones de manera efectiva. Cualquier error que ocurra durante la ejecución de las promesas en el bloque `try` será capturado por el bloque `catch`, donde se puede manejar el error, en este caso, imprimiendo un mensaje de error en la consola.

```JavaScript
const getUser = async () => {

    try{

        /* Para agregar un delay en mi promesa

        await new Promise(resolve => setTimeout(resolve,3000))

        */

        //Promesa

        const response = await fetch("https://jsonplaceholder.typicode.com/users/8");

        const data = await response.json();

        console.log(data);

    }

    catch(error){

        console.log("Error en la peticion",error);

    }

};

getUser();
```