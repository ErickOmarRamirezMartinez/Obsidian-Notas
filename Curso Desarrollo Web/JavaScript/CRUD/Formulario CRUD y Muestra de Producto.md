# Temas Tecnicos

Temas técnicos y conceptos de JavaScript y desarrollo web que hemos utilizado:

1. **Manipulación del DOM**: Usamos JavaScript para acceder y modificar elementos del Document Object Model (DOM). Esto incluye obtener valores de los campos de formulario, crear nuevos elementos HTML dinámicamente, y modificar el contenido existente de la página web. Ejemplos específicos incluyen:
    
    - Uso de `document.getElementById()` para acceder a elementos.
    - Uso de `innerHTML` para añadir contenido HTML dinámicamente a la página.
    - Manipulación de clases y atributos de elementos para controlar el modal.
2. **Eventos y Manejo de Eventos**: JavaScript se utiliza para manejar eventos del usuario, como clics de botones, a través de manejadores de eventos. Esto permite que la aplicación reaccione a acciones del usuario, como abrir un modal, guardar datos, o eliminar productos.
    
    - Uso de `onclick` para asignar funciones a ejecutar cuando los botones son clicados.
3. **Local Storage**: Utilizamos Local Storage para almacenar y recuperar datos persistentes del navegador. Esto permite que los datos de los productos persistan entre sesiones de navegación y después de recargar la página.
    
    - Uso de `localStorage.setItem()` y `localStorage.getItem()` para guardar y recuperar datos en formato JSON.
4. **JSON (JavaScript Object Notation)**: Usamos JSON para estructurar los datos de los productos como una forma de transmitir datos entre el cliente y el almacenamiento local. JSON es ampliamente utilizado en aplicaciones web para el manejo de datos debido a su fácil integración con JavaScript.
    
    - Uso de `JSON.stringify()` para convertir objetos JavaScript a una cadena JSON.
    - Uso de `JSON.parse()` para convertir una cadena JSON de vuelta a un objeto JavaScript.
5. **Programación Asíncrona**: Aunque en los ejemplos proporcionados no utilizamos operaciones asíncronas como fetch API para comunicaciones de red, el manejo de Local Storage y la manipulación del DOM están preparados para integrarse con tales operaciones si se desea expandir la funcionalidad (por ejemplo, cargar productos desde un servidor).
    
6. **Bootstrap y sus componentes interactivos**: Integración de Bootstrap para el estilizado y componentes interactivos como modales. Esto demuestra cómo JavaScript puede interactuar con frameworks de CSS para mejorar la interfaz de usuario.
    
    - Inicialización y control de un modal de Bootstrap mediante JavaScript.
7. **Validación de Formularios**: Aseguramos que los campos del formulario deben ser llenados antes de permitir la adición de un producto, demostrando técnicas básicas de validación del lado del cliente.
    
8. **Funciones y Scope**: Creación y uso de funciones para organizar el código, mantenerlo modular, y manejar diferentes funcionalidades como agregar, editar y eliminar. Además, gestionamos el alcance de las variables y funciones para mantener la estructura del código limpia y eficiente.
    
9. **Uso de template strings (template literals)**: Facilitan la inserción de variables y expresiones en cadenas HTML, haciéndolas más legibles y fáciles de manejar.
    

Estos conceptos no solo son fundamentales para el desarrollo con JavaScript sino que también son esenciales para la creación de aplicaciones web modernas y dinámicas.

---
### 1. Manipulación del DOM

En el desarrollo del formulario y las tarjetas de productos, utilizamos la manipulación del DOM para interactuar con los elementos HTML de la página directamente desde JavaScript. Aquí hay ejemplos concretos:

- **Acceso a Elementos**: Utilizamos `document.getElementById()` para obtener los valores de los campos del formulario, lo que nos permitió capturar lo que el usuario introdujo.
    
    `const productName = document.getElementById('productName').value;`
    
- **Modificación de Elementos**: Al crear las tarjetas de los productos y al mostrar el modal de edición, modificamos el HTML de la página dinámicamente usando `innerHTML`.
    
    `cardContainer.innerHTML += cardHTML;`
    
- **Creación de Elementos**: Al guardar un nuevo producto o editar uno existente, creamos nuevos elementos HTML para las tarjetas que representan visualmente estos productos en la página.
    
    
    ``const cardHTML = `   <div class="col-md-4 product-card" id="product-${product.id}">     ...   </div>`;``
    

Estas operaciones son fundamentales para que la página web sea interactiva y reaccione en tiempo real a las acciones del usuario, como agregar, editar, y eliminar productos.


---
### 2. Eventos y Manejo de Eventos

La gestión de eventos es clave para interactuar con el usuario mediante la página web. Implementamos manejadores de eventos para responder a acciones como clics en botones:

- **Botón de Agregar Producto**: Asignamos la función `addProduct()` al evento `onclick` del botón de agregar, lo que permite capturar y procesar los datos del formulario al hacer clic.

    
    `<button type="button" class="btn btn-primary" onclick="addProduct()">Agregar Producto</button>`
    
- **Botones de Editar y Eliminar**: Cada tarjeta de producto tiene botones para editar y eliminar, cada uno con su propio manejador de eventos que invoca funciones específicas cuando se hacen clic en ellos.
    
    
    `<button onclick="deleteProduct(${product.id})" class="btn btn-danger">Eliminar</button> <button onclick="showEditModal(${product.id})" class="btn btn-secondary">Editar</button>`
    

Estos manejadores de eventos permiten que la aplicación web responda dinámicamente a las interacciones del usuario, ejecutando código específico que modifica el estado de la aplicación y la vista del usuario.

---
### 3. Local Storage

Usamos Local Storage para guardar los datos de los productos de manera persistente en el navegador del usuario. Esto permite que los datos se conserven incluso después de cerrar el navegador o recargar la página.

- **Guardar Datos**: Al agregar o editar un producto, guardamos o actualizamos la lista de productos en Local Storage.

    
    `localStorage.setItem('products', JSON.stringify(products));`
    
- **Recuperar Datos**: Al cargar la página, recuperamos la lista de productos de Local Storage para mostrarlos.
    
    
    `const products = JSON.parse(localStorage.getItem('products')) || [];`
    

Local Storage es crucial para crear una experiencia de usuario consistente, manteniendo los datos accesibles a lo largo de las sesiones de navegación sin necesidad de una base de datos externa o backend.

---
### 4. JSON (JavaScript Object Notation)

JSON es utilizado para estructurar los datos que guardamos en Local Storage, facilitando su manejo como objetos en JavaScript.

- **Serialización**: Convertimos el objeto de datos del producto en una cadena JSON para su almacenamiento.
    
    `JSON.stringify(products);`
    
- **Deserialización**: Convertimos la cadena JSON recuperada de Local Storage de nuevo en un objeto JavaScript para su manipulación.
    
    `JSON.parse(localStorage.getItem('products'));`
    

La utilización de JSON permite un manejo eficiente y estandarizado de los datos dentro de aplicaciones web, facilitando su almacenamiento, recuperación y transmisión.

---
### 5. Bootstrap y sus componentes interactivos

Incorporamos Bootstrap para mejorar la interfaz de usuario mediante estilos predefinidos y componentes interactivos como modales.

- **Modales**: Usamos un modal de Bootstrap para el formulario de edición de productos, proporcionando una interfaz de usuario limpia y consistente.
    
    `<div class="modal fade" id="editProductModal" tabindex="-1" aria-labelledby="editProductModalLabel" aria-hidden="true">   ... </div>`
    
- **Inicialización de Modal**: Inicializamos y mostramos el modal de Bootstrap con JavaScript.
    
    `var editModal = new bootstrap.Modal(document.getElementById('editProductModal')); editModal.show();`
    

Bootstrap facilita la creación de interfaces de usuario atractivas y responsivas con menos esfuerzo y más coherencia en el diseño.

---
### 5. Programación Asíncrona

Aunque en nuestro código no se implementaron llamadas de red asíncronas, el patrón y las prácticas están preparados para soportar tales extensiones. Sin embargo, es importante recalcar que **LocalStorage**, por su naturaleza síncrona, no requiere este tipo de programación. Pero si fueras a implementar un fetch para recuperar datos de un servidor, el código se vería algo así:


`async function fetchProducts() {     try {         const response = await fetch('https://api.example.com/products');         const products = await response.json();         products.forEach(product => addProductCard(product));     } catch (error) {         console.error('Error fetching products:', error);     } }`

Este ejemplo de cómo podrías integrar la programación asíncrona en un contexto real no está implementado directamente en nuestro código, pero representa una extensión natural de las prácticas que hemos establecido.


---
### 6. Validación de Formularios

En el formulario de HTML, hemos usado validaciones simples de HTML5 para asegurarnos de que todos los campos necesarios sean ingresados antes de permitir la adición de un producto:


`<input type="text" class="form-control" id="productName" required> <textarea class="form-control" id="productDescription" rows="3" required></textarea> <input type="number" class="form-control" id="productPrice" required> <input type="url" class="form-control" id="productImageURL" required>`

Cada campo utiliza el atributo `required`, y los campos de precio e URL tienen tipos específicos que también validan el formato de entrada. Estas son las validaciones básicas que proporciona HTML5 sin necesidad de JavaScript adicional.


---
### 7. Funciones y Scope

Nuestras funciones están diseñadas para realizar tareas específicas, ayudando a mantener el código organizado y facilitando la reutilización y el mantenimiento:

- **Funciones de Manejo de Productos**: Cada operación con productos (agregar, editar, eliminar) se encapsula en su propia función.

``function addProduct() {     ...     localStorage.setItem('products', JSON.stringify(products));     addProductCard(productData); }  function deleteProduct(productId) {     ...     localStorage.setItem('products', JSON.stringify(products));     document.getElementById(`product-${productId}`).remove(); }  function editProduct(productId) {     ...     showEditModal(productId); }``

Cada función tiene acceso solo a las variables que necesita para operar, y las variables globales como el acceso al LocalStorage son manejadas de manera global solo cuando es necesario.

---
### 8. Uso de Template Strings (Template Literals)

Utilizamos template strings para construir dinámicamente los HTML de las tarjetas y el modal. Esto permite insertar variables directamente dentro del HTML, haciendo el código más legible y fácil de mantener:

- **Tarjetas de Productos**:


``const cardHTML = `     <div class="col-md-4 product-card" id="product-${product.id}">         <img src="${product.imageUrl}" class="card-img-top" alt="${product.name}">         <div class="card-body">             <h5 class="card-title">${product.name}</h5>             <p class="card-text">${product.description}</p>             <p class="card-text"><strong>Precio:</strong> $${product.price}</p>             <button onclick="deleteProduct(${product.id})" class="btn btn-danger">Eliminar</button>             <button onclick="showEditModal(${product.id})" class="btn btn-secondary">Editar</button>         </div>     </div>`;``

- **Modal para Edición**:


`document.getElementById('editProductName').value = foundProduct.name; document.getElementById('editProductDescription').value = foundProduct.description; ...`

Estos template literals son especialmente útiles cuando necesitas combinar JavaScript y HTML de una manera que es fácil de leer y escribir, especialmente cuando se manejan datos dinámicos como los nombres, descripciones, y precios de los productos.