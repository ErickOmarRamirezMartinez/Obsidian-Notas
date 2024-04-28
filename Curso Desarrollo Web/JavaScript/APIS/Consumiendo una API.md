## Consumir una API

[https://jsonplaceholder.typicode.com/](https://jsonplaceholder.typicode.com/ "https://jsonplaceholder.typicode.com/")


---
## Sincronia
respeta la secuencia

```JavaScript
function primerFuncion(){

    console.log("2");

}

function segundoFuncion(){

    console.log("1");

    console.log("3");

    primerFuncion();

}

segundoFuncion();
```

## Asincronia
Recibimos una funcion y podemos estableceer tiempos dee ejecucion, para eevitar el codigo seecuencial. Este tiempo se establece mediante `setTimeout` quee permite indicar tiempo en milisegundos (1000ms = 1s)

```JavaScript
const firstFunction = () => {

    setTimeout( () => {

        console.log("2");

  

    },2500);

}

  

const secondFunction = () => {

    setTimeout(() => {

        console.log("1");

    },5000);

    console.log("3");

    firstFunction();

}

secondFunction();
```

---
## Trabajando con promesas mediante FetchAPI

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
## Manipulacion dele DOM para mostrar en el navegador

```JavaScript
const botonInfo = document.querySelector('#button--info');

const contenedorInfo = document.querySelector('#div--info');

// Crear una variable de tipo NULL para guardar la info que vamos a traer de la API

let post = null;
```


