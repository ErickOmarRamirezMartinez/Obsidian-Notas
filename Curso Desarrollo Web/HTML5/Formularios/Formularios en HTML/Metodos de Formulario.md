# `method="GET"`
Se utiliza para eenviar datos e informacion del formulario a traves de la URL.
Cuando el usuario envia el formulario, el metodo GET, los parametros del formulario se agregan a la URL como una cadena de consulta (query string)

> [!info] Esto hace que los datos sean visibles en la barra de direcciones del navegador y permite que los usuarios compartan facilemnte los enlaces que contienen esos datos 

```html
<form method="get">

<label for="Nombre">Ingrese Su Nombre :</label>

<input type="text" name="Nombre" id="" placeholder="Nombre" required>

<br>

<label for="Contraseña" >Ingrese Su Contraseña</label>

<input type="password" name="contraseña" id="pass" placeholder="Contraseña">

<br>

<br>

<input type="submit" value="Enviar">

</form>
```

![[Pasted image 20240329002147.png]]

---

# `method="POST"`
Se utiliza para enviar los datos del formulario en el cuerpo de la solicitud HTTP

> [!info] A diferencia del metodo GET, los datos no son visibles en el URL. Esto es util cuando se envian datos sensibles o cuando la cantidad de datos es demasiado grande para incluirlo en la URL

Cuando usas el método POST para enviar datos desde un formulario web a un servidor, estos datos no se anexan a la URL como sucede con el método GET. En lugar de eso, los datos se envían a través del cuerpo de la solicitud HTTP. Esto tiene varias implicaciones en términos de seguridad y capacidad de carga de los datos

```html
<form method="post">

<label for="Nombre">Ingrese Su Nombre :</label>

<input type="text" name="Nombre" id="" placeholder="Nombre" required>

<br>

<label for="Contraseña" >Ingrese Su Contraseña</label>

<input type="password" name="contraseña" id="pass" placeholder="Contraseña">

<br>

<br>

<input type="submit" value="Enviar">

</form>
```

---
# `method="PUT y DELETE"`
Solo HTML soportan los metodos GET Y POST
Pero en aplicaciones mas avanzadas, puedes utilizar los metodos PUT y DELETE

==Put y Delete permiten realizar operaciones de actualizacion y eliminacion en recursos especificos del servidor==
> [!info]  Para usar PUT y DELETE normalmente se utiliza JavaScript u otras tecnologias para enviar solicitudes HTTP personalizadas



