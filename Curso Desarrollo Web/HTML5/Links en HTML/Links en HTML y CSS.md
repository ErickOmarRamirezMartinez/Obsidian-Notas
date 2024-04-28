# Manejo de Link en HTML
## Bookmark 

>**Los bookmarks permiten a los usuario saltar de una seccion especifica a otroa dentro de una pagina web sin la necesidad de dezplazarse**

Ejemplo:

```html
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Document</title>

<link rel="stylesheet" href="estilos.css">

</head>

<body>

<h1 id="seccion1">Esto es una seccion uno</h1>

<p>Culpa eiusmod culpa amet nostrud ipsum esse id adipisicing. Commodo proident cupidatat nostrud in et amet tempor consectetur minim pariatur ut commodo tempor. Fugiat non duis minim culpa non exercitation. Fugiat nostrud officia quis et nisi nostrud minim ex ea est labore.</p>

<p>Culpa eiusmod culpa amet nostrud ipsum esse id adipisicing. Commodo proident cupidatat nostrud in et amet tempor consectetur minim pariatur ut commodo tempor. Fugiat non duis minim culpa non exercitation. Fugiat nostrud officia quis et nisi nostrud minim ex ea est labore.</p>

<p>Culpa eiusmod culpa amet nostrud ipsum esse id adipisicing. Commodo proident cupidatat nostrud in et amet tempor consectetur minim pariatur ut commodo tempor. Fugiat non duis minim culpa non exercitation. Fugiat nostrud officia quis et nisi nostrud minim ex ea est labore.</p>

<h1 id="seccion2">Esto es una seccion dos</h1>

<p>Culpa eiusmod culpa amet nostrud ipsum esse id adipisicing. Commodo proident cupidatat nostrud in et amet tempor consectetur minim pariatur ut commodo tempor. Fugiat non duis minim culpa non exercitation. Fugiat nostrud officia quis et nisi nostrud minim ex ea est labore.</p>

<p>Culpa eiusmod culpa amet nostrud ipsum esse id adipisicing. Commodo proident cupidatat nostrud in et amet tempor consectetur minim pariatur ut commodo tempor. Fugiat non duis minim culpa non exercitation. Fugiat nostrud officia quis et nisi nostrud minim ex ea est labore.</p>

<p>Culpa eiusmod culpa amet nostrud ipsum esse id adipisicing. Commodo proident cupidatat nostrud in et amet tempor consectetur minim pariatur ut commodo tempor. Fugiat non duis minim culpa non exercitation. Fugiat nostrud officia quis et nisi nostrud minim ex ea est labore.</p>

<p><a href="#seccion1">Ir a la seccion 1</a></p>

<p><a href="#seccion2">Ir a la seccion 2</a></p>

  

</body>

</html>
```

---

## Estados y Colores de los Links
![[Pasted image 20240327231907.png]]

- ### `a:link` Estado normal
  Es el estado predeterminado de un enlace antes de que el usuario interactivo con el
- ### `a:visited` Estado visitado 
  Se aplica a un enlace después de que el usuario ha hecho clic en el y ha visitado la pagina vinculada 
- ### `a:active` Estado Activo
  Es el estado del enlace mientras el usuario esta haciendo clic en el o manteniendo presionado el botón del ratón
- ### `a:hover` Estado Hover 
  Se aplica cuando el usuario coloca el curso sobre el enlace, pero antes de hacer clic en el
- ### `a:focus` Estado Focus
  Se aplica cuando el enlace recibe el enfoque, generalmente después de hacer clic en el o al navegar mediante el teclado 
  > Se nota cuando le das tabulador en la pagina 
- ### `a:disabled` Estado Deshabilitado
  Es el estado de un enlace cuando se le aplica la propiedad para deshabilitar la interacción con el 

```html
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Document</title>

<link rel="stylesheet" href="estilos.css">

<link rel="stylesheet" href="index2.html">

</head>

<body>

<p><a href="index2.html">Ir a Index 2</a></p>

</body>

</html>
```

```css
/*Estado General*/

a:link{

color: red;

}

/*Estado Visitado*/

a:visited{

color: cadetblue;

}

  

/*Estado Active*/

a:active{

color: chartreuse;

}

  

/*Estado Hoover*/

a:hover{

color: crimson;

}

  

/*Estado Focus*/

a:focus{

color: darkblue;

}

  

a:disabled{

pointer-events: none;

color: gray;

}
```

---

## Links con Botones en HTML y CSS
Crear un boton con clase y modificado con CSS 

```html
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Document</title>

<link rel="stylesheet" href="estilos.css">

<link rel="stylesheet" href="index2.html">

</head>

<body>

<a href="index2.html" class="boton-link">Ir a Index 2</a>

</body>

</html>
```

```css
.boton-link{

padding: 10px 20px;

background-color: blueviolet;

color: black;

border: solid 5px;

border-radius: 5px;

font-size: 60px;

}
```