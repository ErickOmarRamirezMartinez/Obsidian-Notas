## Formas en la que podemos agregar CSS a HTML

![[Pasted image 20240327210440.png]]

```HTML
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Document</title>

<link rel="stylesheet" href="estilos.css">

<!--Esto es un estilo directo-->

<style>

p{

font-size: 50px;

}

</style>

</head>

<body>

<!-- Este es un estilo añadido en linea-->

<p style="color: aqua;">Este es un estilo interno o en linea</p>

  

<p class="mi-class">Este es un estilo interno en el mismo HTML</p>

</body>

</html>


```

```CSS
.mi-class{

background-color: blueviolet;

}
```