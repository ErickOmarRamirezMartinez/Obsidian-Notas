Ya que el aprendiz tiene el formulario HTML y CSS listo utilizando componentes de Bootstrap, el siguiente paso es agregar la funcionalidad de JavaScript para hacer que el formulario sea interactivo y capaz de manejar la adición de productos. Aquí te dejo una guía detallada sobre cómo proceder:
![[Pasted image 20240504122029.png]]

### Paso 1: Configurar el Manejo de Eventos en JavaScript

1. **Agregar un Event Listener al Botón**:
    
    - Asegúrate de que el botón "Agregar Producto" tenga un `id` para facilitar su selección con JavaScript.
    - Agrega un event listener al botón para manejar el evento `click`. Cuando el usuario haga clic en el botón, se deberá ejecutar una función que procese la información del formulario.
    
    `document.getElementById('addProductBtn').addEventListener('click', addProduct);`
    

### Paso 2: Crear la Función para Agregar Productos

2. **Implementar la Función `addProduct`**:
    
    - Dentro de esta función, captura los valores ingresados en los campos del formulario.
    - Verifica que todos los campos estén llenos antes de proceder (validación básica).

```javascript
function addProduct() {    
var productName = document.getElementById('productName').value;     
var productDescription =document.getElementById('productDescription').value; var productPrice = document.getElementById('productPrice').value;     
var productImageUrl = document.getElementById('productImageUrl').value;      
if (productName && productDescription && productPrice && productImageUrl) {  
// Procede a guardar el producto         
saveProduct(productName, productDescription, productPrice, productImageUrl);}
else {         
alert('Por favor, completa todos los campos.');     } }
```

### Paso 3: Guardar el Producto en Local Storage

3. **Implementar `saveProduct` para Almacenar Datos**:
    
    - Esta función debe tomar los valores del formulario y crear un objeto de producto.
    - Convierte el objeto de producto a una cadena JSON y guárdalo en Local Storage.
    
```javascript
function saveProduct(name, description, price, imageUrl) {     
var product = {         
id: Date.now(), 
// Un identificador único para el producto         
name: name,         
description: description,         
price: price,         
imageUrl: imageUrl     };     
var products = JSON.parse(localStorage.getItem('products')) || [];     products.push(product);     
localStorage.setItem('products', JSON.stringify(products));     alert('Producto agregado con éxito!'); }
```

### Paso 4: Limpieza Post-Agregación

4. **Limpiar el Formulario Después de la Agregación**:
    
    - Una vez que el producto se haya agregado correctamente, limpia los campos del formulario para que estén listos para el próximo ingreso.
    
```JavaScript
document.getElementById('productName').value = ''; document.getElementById('productDescription').value = ''; document.getElementById('productPrice').value = ''; document.getElementById('productImageUrl').value = '';
```
----
### Paso 1: Definir la Estructura del Producto

**Tema técnico**: Manipulación de objetos JavaScript

- **Acción**: Define un objeto JavaScript para almacenar los detalles del producto. Utiliza propiedades como `id`, `name`, `description`, `price`, y `imageUrl`.

### Paso 2: Añadir Productos al DOM

**Tema técnico**: Manipulación del DOM

- **Acción**: Crea tarjetas de producto dinámicamente utilizando `innerHTML` para insertar HTML en el DOM, integrando los datos del producto directamente en el markup.


```javascript
function addProductCard(product) {     const cardContainer = document.getElementById('productCards');     const cardHTML = `         <div class="col-md-4 product-card" id="product-${product.id}">             <img src="${product.imageUrl}" class="card-img-top" alt="${product.name}">             <div class="card-body">                 <h5 class="card-title">${product.name}</h5>                 <p class="card-text">${product.description}</p>                 <p class="card-text"><strong>Precio:</strong> $${product.price}</p>                 <button onclick="deleteProduct(${product.id})" class="btn btn-danger">Eliminar</button>                 <button onclick="showEditModal(${product.id})" class="btn btn-secondary">Editar</button>             </div>         </div>`;     cardContainer.innerHTML += cardHTML; }
```

### Paso 3: Eliminar Productos

**Tema técnico**: Uso de Local Storage y manipulación del DOM

- **Acción**: Implementa la eliminación de productos del Local Storage y del DOM usando `filter` y `remove`.

```javascript
function deleteProduct(productId) {     let products = JSON.parse(localStorage.getItem('products'));     products = products.filter(product => product.id !== productId);     localStorage.setItem('products', JSON.stringify(products));     document.getElementById(`product-${productId}`).remove(); }
```

### Paso 4: Mostrar y Editar Productos

**Tema técnico**: Manipulación del DOM, Eventos de JavaScript, Uso de Modales (Bootstrap)

- **Acción**: Muestra un modal de Bootstrap con un formulario prellenado para la edición de productos, manipulando el DOM para insertar los datos

```JavaScript
function showEditModal(productId) {

            let products = JSON.parse(localStorage.getItem('products'));

            let foundProduct = products.find(product => product.id === productId);

            if (foundProduct) {

                document.getElementById('editProductId').value = foundProduct.id;

                document.getElementById('editProductName').value = foundProduct.name;

                document.getElementById('editProductDescription').value = foundProduct.description;

                document.getElementById('editProductPrice').value = foundProduct.price;

                document.getElementById('editProductImageURL').value = foundProduct.imageUrl;

                var editModal = new bootstrap.Modal(document.getElementById('editProductModal'));

                editModal.show();

            }

        }
```

### Paso 5: Guardar Productos Editados

**Tema técnico**: Manipulación del DOM, Local Storage, Programación Asíncrona

- **Acción**: Guarda los cambios realizados al producto en Local Storage y actualiza la visualización en la interfaz de usuario.

```JavaScript
function saveEditedProduct() {     const productId = parseInt(document.getElementById('editProductId').value);     const productName = document.getElementById('editProductName').value;     const productDescription = document.getElementById('editProductDescription').value;     const productPrice = document.getElementById('editProductPrice').value;     const productImageURL = document.getElementById('editProductImageURL').value;      let products = JSON.parse(localStorage.getItem('products'));     let productIndex = products.findIndex(product => product.id === productId);     if (productIndex !== -1) {         products[productIndex] = {             id: productId,             name: productName,             description: productDescription,             price: productPrice,             imageUrl: productImageURL         };         localStorage.setItem('products', JSON.stringify(products));         document.getElementById(`product-${productId}`).remove();         addProductCard(products[productIndex]);          var editModal = bootstrap.Modal.getInstance(document.getElementById('editProductModal'));         editModal.hide();     } }
```


- **Explicación**: Esta función busca el producto en el arreglo almacenado en Local Storage por ID, lo actualiza con los nuevos valores obtenidos del formulario del modal, y lo guarda de nuevo en Local Storage. Luego actualiza la visualización del producto en la página web sin necesidad de recargar, y finalmente cierra el modal.

### Paso 6: Eliminar Productos

**Tema técnico**: Manipulación del DOM, Local Storage

- **Acción**: Elimina un producto tanto del Local Storage como del DOM.

```Javascript
function deleteProduct(productId) {     let products = JSON.parse(localStorage.getItem('products'));     products = products.filter(product => product.id !== productId);     localStorage.setItem('products', JSON.stringify(products));     document.getElementById(
```