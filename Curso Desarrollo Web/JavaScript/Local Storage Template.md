### Estructura del Código y Explicación

#### Formulario de Registro

1. **Selección del Formulario y Evento de Envío:**
    
    - `const registroFormulario = document.getElementById("registerForm");`
    - Se selecciona el formulario de registro utilizando `getElementById` y se agrega un listener de evento para el envío (`submit`).
2. **Prevención del Envío por Defecto:**
    
    - `event.preventDefault();`
    - Evita que el formulario se envíe de manera predeterminada, lo cual permitiría recargar la página.
3. **Recuperación de Datos del Formulario:**
    
    - Se obtienen los valores de los campos de usuario y contraseña usando `.value`.
    - `const username = document.getElementById("username").value;`
    - `const password = document.getElementById("password").value;`
4. **Almacenamiento en `localStorage`:**
    
    - `localStorage.setItem("username", username);`
    - `localStorage.setItem("password", password);`
    - Los datos se almacenan en `localStorage`, permitiendo su acceso en sesiones futuras.
5. **Feedback y Limpieza del Formulario:**
    
    - `alert("Registro Exitoso!!!");`
    - `this.reset();`
    - Se muestra un mensaje de registro exitoso y se limpia el formulario.


```javascript
const registroFormulario = document.getElementById("registerForm");

const inicioFormulario = document.getElementById("loginForm");


//Manipulando el formulario de Registro

registroFormulario.addEventListener("submit",(event) =>{

    event.preventDefault(); //Evita enviar el formulario

  

    //Guardando los valores de los input

    const username = document.getElementById("username").value;

    const password = document.getElementById("password").value;

  

    //Guardar los valores de los inputs en el alcacenamieento local

    // Syntaxis (localstorage.setItem("nombreItem", variable))

    localStorage.setItem("username", username);

    localStorage.setItem("password", password);


    alert("Registro Exitoso!!!");

    this.reset();// Permite limpiar el formulario despuees de enviar la informacion

});
```

#### Formulario de Inicio de Sesión

1. **Selección del Formulario y Evento de Envío:**
    
    - `const inicioFormulario = document.getElementById("loginForm");`
    - Similar al formulario de registro, se agrega un listener para el evento de envío.
2. **Prevención del Envío por Defecto y Recuperación de Datos:**
    
    - También se previene el envío predeterminado y se recuperan los valores ingresados por el usuario.
3. **Recuperación de Datos de `localStorage`:**
    
    - `const saveusername = localStorage.getItem("username");`
    - `const savepassword = localStorage.getItem("password");`
    - Se obtienen los datos almacenados anteriormente de `localStorage`.
4. **Validación de Credenciales:**
    
    - Se compara si los datos ingresados coinciden con los almacenados.
    - Si coinciden, se muestra un mensaje de bienvenida.
    - Si no coinciden, se informa al usuario y se limpia el formulario.


```JavaScript
//Manipulando el formulario de Inicio de Sesion

inicioFormulario.addEventListener("submit",(event) =>{

    event.preventDefault();

  

    //Guardando los valores de los input

    const loginUsername = document.getElementById("loginUsername").value;

    const loginPassword = document.getElementById("loginPassword").value;

  

    //Obtener los valores de los inputs del almacenamiento local

    //Sintaxis para obtener: localStorage.getItem("nombreItem");

  

    const saveusername = localStorage.getItem("username");

    const savepassword = localStorage.getItem("password");

  

    //Validar si el usernamee y password coinciden con el local storage

  

    if(loginUsername === saveusername && loginPassword === savepassword){

        alert(`Bienvenido ${saveusername}, Inicio de Sesion Exitoso`);

    }

    else{

        alert("Usuario o contraseña incorrectos!!!");

        this.reset();// Permite limpiar el formulario despuees de enviar la informacion");

    }

  

});
```
### Mejores Prácticas y Consideraciones

- **Seguridad:** Aunque `localStorage` es útil para datos no sensibles, no es recomendable usarlo para almacenar contraseñas u otra información sensible debido a su naturaleza fácilmente accesible desde el cliente.
- **Depuración y Pruebas:** Es crucial probar ambos formularios para asegurar que los datos se guardan y recuperan correctamente.
