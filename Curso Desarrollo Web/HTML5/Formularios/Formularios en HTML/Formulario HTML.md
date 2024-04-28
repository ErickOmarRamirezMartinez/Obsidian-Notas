```html
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Document</title>

</head>

<body>

<h1>Ejemplo de un Simple Formulario</h1>

  

<!--Uso de Input:text y Input:submit-->

<form>

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

<h2>Opciones Disponibles</h2>

<label for="Checkbox">Opcion 1</label>

<input type="checkbox" name="opcion1" id="opcion1" value="opcion1" checked>

<br>

<label for="Checkbox">Opcion 2</label>

<input type="checkbox" name="opcion2" id="opcion1" value="opcion1">

<br>

<label for="Checkbox">Opcion 3</label>

<input type="checkbox" name="opcion3" id="opcion1" value="opcion1">

<br>

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

<h2>Mas Opciones</h2>

<label for="">Ingrese el archivo</label>

<br>

<input type="file" name="archivo" id="archivo" multiple accept=".jpg">

<br>

<label for="fecha">Ingrese la fecha</label>

<input type="date" name="" id="">

<input type="datetime-local" name="" id="">

<br>

<label for="tiempo">Ingrese la hora</label>

<input type="time" name="" id="">

<br>

<label for="meses">Ingrese el mes y año</label>

<input type="month" name="" id="">

<br>

<label for="semana">Ingrese la semana del año</label>

<input type="week" name="" id="">

<br>

<label for="color">Selecciona un color</label>

<input type="color" name="" id=""value="#FFFFFF">

<br>

<label for="rango">Ingrese un rango</label>

<input type="range" name="" id="" min="1" max="50" step="5">

<br>

<input type="submit" value="Enviar">

<br>

<input type="reset" value="Reestablecer">

<br>

<input type="button" value="Haz Click">

<br>

<input type="hidden" name="id_usuario" value="User123">

<br>

<input type="search" name="bus" id="bus" placeholder="Busca Algo">

</form>

</body>

</html>
```