# `<dl>` 
Las listas con definición se utilizan para mostrar conjuntos con sus definiciones


## `<dt>` term
Aquí se va el titulo de la descripcion

## `<dd>` data
Aquí se pone la descripción del termino

```html
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Document</title>

<style>

ol li::before{

content: "Serie: ";

}

dt{

}

</style>

</head>

<body>

<ul>

<li>Elemento A</li>

<li>Elemento B</li>

<li>Elemento C</li>

</ul>

  

<ol>

<li>Elemento A</li>

<li>Elemento B</li>

<li>Elemento C</li>

<ul>

<li>No</li>

</ul>

</ol>

  

<dl>

<dt>Termino 1</dt>

<dd>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Debitis excepturi veniam tempore, asperiores assumenda illo officiis nihil eius dolore unde tenetur placeat quod reiciendis doloremque odio, inventore quidem quaerat dolorem.</dd>

<dt>Termino 2</dt>

<dd>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab quo animi ipsum aut consectetur incidunt saepe maxime, accusantium dignissimos illum. Esse dolor eum sed excepturi reprehenderit quo, dignissimos corporis culpa?</dd>

  

<dt>Termino 3</dt>

<dd>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Doloremque dolorum, perferendis maxime inventore numquam sapiente vero ipsum aliquam, impedit, totam quis dolores architecto eum quia. Rerum maiores iusto architecto officia.</dd>

</dl>

</body>

</html>
```