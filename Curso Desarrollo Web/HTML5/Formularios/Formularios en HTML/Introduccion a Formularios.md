# **Formularios en HTML** `<form> <input>`

> La etiqueta `<form>` se utiliza para crear un formulario interactivo que permite a los usuarios enviar datos al servidor web

> La etiqueta `<input>` es unos de los elementos ,as versatiles y se utiliza para crear los campos interactivos en los formularios web.


## Atributos de la etiqueta `<form>`

![[Pasted image 20240329145000.png]]


---

## Algunos  `<input>` mas comunes que se utilizan son:

+  `type="text"` 
  Crea un campo de entrada de texto de una sola linea, que permite al usuario escribir texto
+  `type="password"`
  Oculta los caracteres escritos para poder ingresar la contraseña
+  `type="checkbox"`
  Muestra una casilla de verificación que el usuario puede seleccionar 
+  `type="submit"` 
  Crea un botón para enviar el formulario


## **Atributos de la etiqueta `<input>`**

+ ## `type`
  Especifica el tipo de campo de entrada, como:
  `"checkbox" , "radio", "submit", "reseat", "file", "number", "date"`, entre otros

+ ## `name`
  Define el nombre del campo de entrada, Es util para poder identificar el capo que se enviara al servidor

+ ## `value`
  Establece el valor predeterminado del campo. Sirve para darle un valor inicial a un campo de selección

+ ## `placeholder`
  Muestra un texto de ayuda o indicativo dentro del campo de entrada 

+ ## `disabled`
  Si se establece, deshabilita el campo de entrada, lo que el usuario no podrá interactuar ni modificar
  
+ ## `readonly`
  Si se establece, permite que el campo de entrada solo sea de lectura

+ ## `required`
  Indica que el campo de entrada es obligatorio y debe tener un valor antes de ser enviado
  
+ ## `max y min`
  Estos atributos se utilizan en campos numéricos para definir el máximo y mínimo permitido

+ ## `maxlenght`
  Define la cantidad máxima de un carácter puede ingresa

+ ## `multiple`
  Aplicable en campos de tipo `"file"` , permite al usuario seleccione varios archivos para ser enviados

+ ## `autocomplete`
  Habilita o des habilita la función de auto completar del navegador para el campo de entrada

+ ## `pattern`
  Permite definir una expresión regular que el valor del campo de entrada debe cumplir para ser valido 

--- 
## Ejemplos

### `<input Type “text”>`
```html
<form>

<label for="Nombre">Ingrese Su Nombre :</label>

<input type="text" name="Nombre" id="" placeholder="Nombre" required>

<input type="submit" placeholder="Enviar">

</form>
```


### `<input Type “password”>`
```html
<form>

<label for="Nombre">Ingrese Su Nombre :</label>

<input type="text" name="Nombre" id="" placeholder="Nombre" required>

<br>

<label for="Contraseña" >Ingrese Su Contraseña</label>

<input type="password" name="contraseña" id="pass" placeholder="Contraseña">

<br>

<input type="submit" placeholder="Enviar">

</form>
```

### `<input Type “email”>`
```html
<br>

<label for="email">Ingrese su Email</label>

<input type="email" name="email" id="email" placeholder="Email">

<br>
```


### `<input Type “number”>`
```html
<br>

<label for="edad">Ingrese su Edad</label>

<input type="number" name="edad" id="edad" placeholder="Edad" min="18" max="90">

<br>
```


### `<input Type “tel”>`
```html
<br>

<label for="telefono">Ingrese su telefono</label>

<input type="tel" name="telefono" id="telefono" placeholder="Telefono" maxlength="10">

<br>
```

### `<input Type “url”>`
```html
<br>

<label for="url">Ingrese el URL</label>

<input type="url" name="url" id="url" placeholder="https://www.udemy.com/">

<br>
```


### `<input Type “checkbox”>`
```html
<br>

<label for="Checkbox">Opcion 1</label>

<input type="checkbox" name="opcion1" id="opcion1" value="opcion1" checked>

<br>

<label for="Checkbox">Opcion 2</label>

<input type="checkbox" name="opcion1" id="opcion1" value="opcion1" checked>

<br>

<label for="Checkbox">Opcion 3</label>

<input type="checkbox" name="opcion1" id="opcion1" value="opcion1" checked>

<br>
```

### `<input Type “radio”>`
```html
<h2>Seleccionar una opcion</h2>

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
```

### `<input Type “file”>`
```html
<br>

<label for="">Ingrese el archivo</label>

<br>

<input type="file" name="archivo" id="archivo" multiple accept=".jpg">

<br>
```

### `<input Type “date”>`
```html
<label for="fecha">Ingrese la fecha</label>

<input type="date" name="" id="">

<br>
```

### `<input Type “datetime-local”>`
```html
<br>

<label for="fecha">Ingrese la fecha</label>

<input type="date" name="" id="">

<input type="datetime-local" name="" id="">

<br>
```

### `<input Type “time”>`
```html
<br>

<label for="tiempo">Ingrese la hora</label>

<input type="time" name="" id="">

<br>
```

### `<input Type “month”>`
```html
<br>

<label for="meses">Ingrese el mes y año</label>

<input type="month" name="" id="">

<br>
```

### `<input Type “week”>`
```html
<br>

<label for="semana">Ingrese la semana del año</label>

<input type="week" name="" id="">

<br>
```

### `<input Type “color”>`
```html
<br>

<label for="color">Selecciona un color</label>

<input type="color" name="" id=""value="#FFFFFF">

<br>
```

### `<input Type “range”>`
```html
<br>

<label for="rango">Ingrese un rango</label>

<input type="range" name="" id="" min="1" max="50" step="5">

<br>
```

### `<input Type “submit”>`
![[Pasted image 20240328234930.png]]

```html
<br>

<input type="submit" placeholder="Enviar">

<br>
```


### `<input Type “reset”>`

```html
<br>

<input type="reset" value="Reestablecer">

<br>
```

### `<input Type “button”>`
```html
<br>

<input type="button" value="Haz Click">

<br>
```

### `<input Type “hidden”>`
Este es un campo se poner modificar nosotros sin que el usuario lo pueda ver o modificar
```html
<br>

<input type="hidden" name="id_usuario" value="User123">

<br>
```

