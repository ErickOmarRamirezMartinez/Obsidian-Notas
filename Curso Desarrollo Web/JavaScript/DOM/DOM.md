![[Pasted image 20240415114127.png]]
![[Pasted image 20240415114240.png]]

![[Pasted image 20240415114315.png]]
![[Pasted image 20240415114332.png]]![[Pasted image 20240415114536.png]]

[Caninclude](https://caninclude.glitch.me/)

![[Pasted image 20240415115009.png]]
![[Pasted image 20240415115218.png]]
![[Pasted image 20240415115327.png]]


---
## Elemento Defer en Javascript

```Javascript
<script src="./src/app/app.js" defer></script>
```
Este atributo booleano está configurado para indicarle a un navegador que el script debe ejecutarse después de que se haya analizado el documento, pero antes de activar DOMContentLoaded.

Los scripts con el atributo defer evitarán que el evento DOMContentLoaded se active hasta que el script se haya cargado y terminado de evaluar.

---

![[Pasted image 20240415161403.png]]
![[Pasted image 20240415161410.png]]

---

# Manipulación del DOM con JavaScript:
Podemos acceder y modificar elementos del HTML utilizando métodos específicos. 
Métodos comunes para seleccionar elementos: 

*  `document.getElementById("id")` : Selecciona un único elemento por su ID. 
*  `document.getElementsByClassName("class")`: Selecciona todos los elementos que tienen la clase especificada. 
* `document.getElementsByTagName("tag")` : Selecciona todos los elementos con el nombre de etiqueta especificado. 

```javaScript
// Usando getElementById para obtener elementos individuales por su ID.

const tituloH1 = document.getElementById("title1");  // Selecciona el elemento con ID 'title1'.

const tituloH2 = document.getElementById("title2");  // Selecciona el elemento con ID 'title2'.

  

// Mostrar en la consola los elementos seleccionados.

console.log(tituloH1);           // Muestra el objeto del elemento HTML para 'title1'.

console.log(tituloH1.innerText); // Muestra el texto contenido en el elemento 'title1'.

console.log(tituloH2.innerText); // Muestra el texto contenido en el elemento 'title2'.

  

// Usando getElementsByClassName para obtener todos los elementos que comparten una clase.

const titulos = document.getElementsByClassName("title"); // Selecciona todos los elementos con la clase 'title'.

console.log(titulos);         // Muestra el HTMLCollection de los elementos con clase 'title'.

console.log(titulos.length);  // Muestra el número de elementos con la clase 'title'.

console.log(typeof titulos);  // Muestra el tipo de objeto 'titulos', que es 'object'.
```

## Usando `getElementsByTagName` para obtener todos los elementos con la etiqueta especificada.

```JavaScript
const tituloH3 = document.getElementsByTagName("h3"); 
console.log(tituloH3); // Muestra una colección HTML de todos los elementos <h3> encontrados.
```

## Métodos para seleccionar elementos usando selectores CSS: 

*  `document.querySelector("selector")`: Retorna el primer elemento que coincida con el selector CSS especificado. 
* `document.querySelectorAll("selector")`: Retorna todos los elementos que coincidan con el selector CSS especificado.

### Usando `querySelector` para obtener el primer elemento que coincide con el selector.
```JavaScript
const titulo4 = document.querySelector("#title4"); // Selecciona el primer elemento con el ID 'title4'.
console.log(titulo4); // Muestra el elemento en la consola.

const primerTitulo = document.querySelector(".title"); // Selecciona el primer elemento con la clase 'title'. 
console.log(primerTitulo); // Muestra el primer elemento con la clase 'title'. // Usando querySelectorAll para obtener todos los elementos que coincidan con el selector. 

const tituloQuery = document.querySelectorAll(".title"); // Selecciona todos los elementos con la clase 'title'. 
console.log(tituloQuery); // Muestra un NodeList de todos los elementos con clase 'title'.
```


###  Manipulación de estilos del DOM desde JavaScript para el elemento con ID 'title1'.

```JavaScript
tituloH1.style.textAlign = "center"; 
// Centra el texto del elemento. 

tituloH1.style.color = "#E1523D"; 
// Cambia el color del texto a rojo.
```

### Manipulación del texto y estilo de un elemento.

```JavaScript
tituloH2.innerText = "Sesion de Manipulacion del DOM - CH39"; 
// Cambia el texto del elemento 'title2'. 

tituloH2.style.color = "#C2BB00"; 
// Cambia el color del texto a amarillo.
```

---

# Crear y agregar elementos en el DOM: 
Este proceso se divide en dos partes principales: Crear el nodo y agregar el nodo. 

### Crear Nodos:  
- `document.createElement("tipoElemento")`: Crea un elemento HTML nuevo especificado por la etiqueta. 
*  `document.createTextNode("texto")`: Crea un nodo de texto que puede ser añadido a un elemento HTML. 

 ### Agregar Nodos: 
 * `parentNode.appendChild(node)`: Añade un nodo como el último hijo del nodo padre. 
 * `parentNode.append(node, node2, ...)`: Añade uno o más nodos o textos al final del nodo padre. 
 *  `parentNode.insertBefore(newNode, referenceNode)`: Inserta un nodo antes del nodo de referencia en el DOM. 
 *  `parentNode.insertAdjacentElement(position, node)`: Inserta un elemento en la posición especificada relativa al nodo padre.

## Crear elementos del DOM.

```JavaScript
const tituloH4 = document.createElement("h4"); 
// Crea un elemento <h4>.

const imgNode = document.createElement("img"); 
// Crea un elemento <img>.
```

```JavaScript
// 1. Obtener el nodo padre donde se agregarán los elementos creados. 
const imgParent = document.getElementById("img-container"); 

// 2. Crear el texto que vivirá en el nodo títuloH4. 
const textTitulo4 = document.createTextNode("Imagen agregada desde el DOM"); 

// 3. Insertar el texto en el nodo títuloH4. 
tituloH4.appendChild(textTitulo4); 

// 4. Insertar el nodo títuloH4 en el nodo padre. 
imgParent.appendChild(tituloH4); 
imgParent.style.color = "#A1C7E0"; 

// Cambiar el color del texto del nodo padre. 

// 5. Configurar atributos de la imagen. 
imgNode.src = "path/to/image.png"; 

// Ruta de la imagen (ajustar según sea necesario). 
imgNode.alt = "Imagen de ejemplo"; 

// Texto alternativo para la imagen. 
imgNode.width = "360"; // Ancho de la imagen en píxeles. 

// 6. Agregar la imagen al nodo padre. 
imgParent.appendChild(imgNode);
```