# Mas opciones que tiene `<input>`

## `<select>`
Se utiliza para crear una lista desplegables en formularios web.

Es una forma de proporcionar opciones predefinidas a los usuarios para que seleccionen una sola opcion de entre varias.

Para usarla debemos estar dentro de la etiqueta `select`  se define mediante la etiqueta `<option>`
![[Pasted image 20240329142513.png]]

```html
<br>

<select name="selector" id="Selector">

<option value="">Opcion 1</option>

<option value="">Opcion 2</option>

<option value="">Opcion 3</option>

</select>

<br>
```

---

## `<textarea>`
La eetiqueta `<textarea>` en HTML es utilizada para crear un campo de texto multi-linea en un formulario web.

![[Pasted image 20240329143902.png]]

```html
<br>

<label for="">Ingrese su texto</label>

<textarea name="" id="" cols="30" rows="10"></textarea>

<br>

```

---

## `<fieldset>`
Es utilizada para agrupar elementos relacionados a un formulario web y crea un borde al rededor de ellos

Es muy util cuando tienes varios elementos que comparten un proposito o pertenece a una seccion especifica del formulario 


## `<legend>`
La etiqueta `<legend>` se coloca de `<fieldset>` y proporciona un titulo o descripcion para agrupar los elementos 


```html
<fieldset>

<legend>Formulario 1</legend>

<label for="Nombre">Ingrese Su Nombre :</label>

<input type="text" name="Nombre" id="" placeholder="Nombre" required>

<br>

<label for="Contraseña" >Ingrese Su Contraseña</label>

<input type="password" name="contraseña" id="pass" placeholder="Contraseña">

<br>

<label for="email">Ingrese su Email</label>

<input type="email" name="email" id="email" placeholder="Email">

<br>

<label for="edad">Ingrese su Edad</label>

<input type="number" name="edad" id="edad" placeholder="Edad" min="18" max="90">

<br>

<label for="telefono">Ingrese su telefono</label>

<input type="tel" name="telefono" id="telefono" placeholder="Telefono" maxlength="10">

<br>

<label for="url">Ingrese el URL</label>

<input type="url" name="url" id="url" placeholder="https://www.udemy.com/">

<br>

</fieldset>

<br>

<fieldset>

<h3>Opciones Disponibles</h3>

<legend>Formulario 2</legend>

<label for="Checkbox">Opcion 1</label>

<input type="checkbox" name="opcion1" id="opcion1" value="opcion1" checked>

<br>

<label for="Checkbox">Opcion 2</label>

<input type="checkbox" name="opcion2" id="opcion1" value="opcion1">

<br>

<label for="Checkbox">Opcion 3</label>

<input type="checkbox" name="opcion3" id="opcion1" value="opcion1">

<br>

<h3>Seleccionar una opcion</h3>

<input type="radio" name="1" id="" checked>

<label for="Opcion1">Opcion 1</label>

<br>

<input type="radio" name="1" id="">

<label for="Opcion2">Opcion 2</label>

<br>

<input type="radio" name="1" id="">

<label for="Opcion3">Opcion 3</label>

<br>

<input type="radio" name="1" id="">

<label for="Opcion4">Opcion 4</label>

<br>

</fieldset>
```

