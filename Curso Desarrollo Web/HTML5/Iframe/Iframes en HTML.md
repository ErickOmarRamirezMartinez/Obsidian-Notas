# `<iframe>` Inline Frame - Marco de linea
La etiqueta `<iframe>` es un elemento de HTML que se utiliza para incrustar contenido de otra pagina web dentro de una pagina principal

Con `<iframe>` , es posible mostrar contenido externo, como otras paginas web, documentos PDF, videos, mapas y mas

![[Pasted image 20240328213006.png]]


```html
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Document</title>

</head>

<body>

<h1>Uso de los iframes</h1>

<hr>

  

<h2>Uso de los iframe con archivos HTML que esten en la misma carptea</h2>

<iframe src="horario.html" frameborder="100px" height="300px" width="500px"></iframe>

  

<br>

<h2>Uso de los Iframes con paginas WEB</h2>

<iframe width="560" height="315" src="https://www.youtube.com/embed/2gyxXtOpWlA?si=4gS6Tea0I86_jmQt" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

</body>

</html>
```

