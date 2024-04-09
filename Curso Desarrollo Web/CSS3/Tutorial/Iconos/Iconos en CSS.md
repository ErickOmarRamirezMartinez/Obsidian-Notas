# Iconos de Bootstrap

Para usar los glifos de Bootstrap, agregue la siguiente línea dentro de la sección de su página HTML:`<head>`

### CDN

Incluya la hoja de estilo de las fuentes de los iconos, en su sitio web o a través de CSS, de jsDelivr y comience en segundos. [Consulte los documentos de fuentes de iconos](https://icons.getbootstrap.com/#icon-font) para ver ejemplos.`<head>``@import`
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
```
```css
@import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css");
```

```html
<!DOCTYPE html>
<html>
<head>
<title>Bootstrap Icons</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
</head>
<body class="container">

<h1>Bootstrap icon library</h1>

<p>Some Bootstrap icons:</p>
<i class="glyphicon glyphicon-cloud"></i>
<i class="glyphicon glyphicon-remove"></i>
<i class="glyphicon glyphicon-user"></i>
<i class="glyphicon glyphicon-envelope"></i>
<i class="glyphicon glyphicon-thumbs-up"></i>
<br><br>

<p>Styled Bootstrap icons (size and color):</p>
<i class="glyphicon glyphicon-cloud" style="font-size:24px;"></i>
<i class="glyphicon glyphicon-cloud" style="font-size:36px;"></i>
<i class="glyphicon glyphicon-cloud" style="font-size:48px;color:red;"></i>
<i class="glyphicon glyphicon-cloud" style="font-size:60px;color:lightblue;"></i>

</body>
</html>


```

![[Pasted image 20240405213600.png]]

---

# Iconos de Google

Para usar los íconos de Google, agregue la siguiente línea dentro de la sección de su página HTML:`<head>`

`<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">`

**Nota:** ¡No se requiere descarga ni instalación!

```html
<h1>Google icon library</h1>

<p>Some Google icons:</p>
<i class="material-icons">cloud</i>
<i class="material-icons">favorite</i>
<i class="material-icons">attachment</i>
<i class="material-icons">computer</i>
<i class="material-icons">traffic</i>
<br><br>

<p>Styled Google icons (size and color):</p>
<i class="material-icons" style="font-size:24px;">cloud</i>
<i class="material-icons" style="font-size:36px;">cloud</i>
<i class="material-icons" style="font-size:48px;color:red;">cloud</i>
<i class="material-icons" style="font-size:60px;color:lightblue;">cloud</i>
```

![[Pasted image 20240405214054.png]]



## Ejemplo:

```html
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Document</title>

<link rel="stylesheet" href="style.css">

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">

<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">

</head>

<body>

<h1>Iconos con Bootstrap</h1>

<div>

<p>

<i class="bi-0-circle"></i>

<i class="bootstrap-icons"></i>

Alarma

</p>

</div>

  

<h1>Iconos con Google</h1>

<i class="material-icons">cloud</i>

</body>

</html>
```
![[Pasted image 20240405214608.png]]
