## ¿Qué son las pseudoclases?

Una pseudoclase se utiliza para definir un estado especial de un elemento.

Por ejemplo, se puede utilizar para:

- Aplicar estilo a un elemento cuando un usuario pasa el ratón por encima de él
- Diseña los enlaces visitados y no visitados de manera diferente
- Aplicar estilo a un elemento cuando se le da el focus

## Sintaxis

La sintaxis de las pseudoclases:

```css
selector:pseudo-class {  property: value;}
```


Ejemplos:
```html
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Document</title>

<link rel="stylesheet" href="style.css">

</head>

<body>

<h1>Pseudo Clases y Psudo Elementos </h1>

  

<div class="contenedor oculto">

Pasa por encima

  

<p>Se muestra el parrafo</p>

  

</div>

<div class="contenedor primero">

<p>Primer Parrafo</p>

<p>Segundo Parrafo</p>

</div>

  

<div>

Coloca el cursos sobre mi para mostrar el elemento < p >

<p class="here">Tadaa estoy Aqui</p>

</div>

  

<input type="text" name="" id="">

</body>

</html>
```


```css
h1{

text-align: center;

color: crimson;

}

div.contenedor{

height: 20%;

width: 80%;

margin: 20px auto;

border: 2px solid black;

text-align: center;

}

div.contenedor:hover{

background-color: darkgoldenrod;

color: white;

}

div.contenedor.oculto p{

display: none;

}

div.contenedor.oculto:hover p{

display: block;

background-color: aquamarine;

color: black;

padding: 15px;

}

div.contenedor.primero p:first-child{

font-variant: small-caps;

}

  

p.here{

display: none;

background-color: yellow;

padding: 20px;

}

div:hover p{

display: block;

}

input[type = "text"]{

margin: 20px 0;

  

}

input[type = "text"]:focus{

background-color: yellow;

width: 250px;

}
```

![[Pasted image 20240407230600.png]]

![[Pasted image 20240407230628.png]]

## All CSS Pseudo Classes

- **:active**: Selecciona el enlace activo.
- **:checked**: Selecciona todos los elementos `<input>` que estén marcados.
- **:disabled**: Selecciona todos los elementos `<input>` que estén deshabilitados.
- **:empty**: Selecciona todos los elementos `<p>` que no tengan hijos.
- **:enabled**: Selecciona todos los elementos `<input>` que estén habilitados.
- **:first-child**: Selecciona todos los elementos `<p>` que sean el primer hijo de su padre.
- **:first-of-type**: Selecciona todos los elementos `<p>` que sean el primer elemento `<p>` de su padre.
- **:focus**: Selecciona el elemento `<input>` que tenga el foco.
- **:hover**: Selecciona los enlaces cuando el mouse pasa sobre ellos.
- **:in-range**: Selecciona los elementos `<input>` con un valor dentro de un rango especificado.
- **:invalid**: Selecciona todos los elementos `<input>` con un valor inválido.
- **:lang(language)**: Selecciona todos los elementos `<p>` con un valor de atributo lang que comience con "it".
- **:last-child**: Selecciona todos los elementos `<p>` que sean el último hijo de su padre.
- **:last-of-type**: Selecciona todos los elementos `<p>` que sean el último elemento `<p>` de su padre.
- **:link**: Selecciona todos los enlaces no visitados.
- **:not(selector)**: Selecciona todos los elementos que no sean elementos `<p>`.
- **:nth-child(n)**: Selecciona todos los elementos `<p>` que sean el segundo hijo de su padre.
- **:nth-last-child(n)**: Selecciona todos los elementos `<p>` que sean el segundo hijo de su padre, contando desde el último hijo.
- **:nth-last-of-type(n)**: Selecciona todos los elementos `<p>` que sean el segundo elemento `<p>` de su padre, contando desde el último hijo.
- **:nth-of-type(n)**: Selecciona todos los elementos `<p>` que sean el segundo elemento `<p>` de su padre.
- **:only-of-type**: Selecciona todos los elementos `<p>` que sean el único elemento `<p>` de su padre.
- **:only-child**: Selecciona todos los elementos `<p>` que sean el único hijo de su padre.
- **:optional**: Selecciona los elementos `<input>` sin atributo "required".
- **:out-of-range**: Selecciona los elementos `<input>` con un valor fuera de un rango especificado.
- **:read-only**: Selecciona los elementos `<input>` con un atributo "readonly" especificado.
- **:read-write**: Selecciona los elementos `<input>` sin atributo "readonly".
- **:required**: Selecciona los elementos `<input>` con un atributo "required" especificado.
- **:root**: Selecciona el elemento raíz del documento.
- **:target**: Selecciona el elemento #news actual activo (haz clic en una URL que contenga ese nombre de ancla).
- **:valid**: Selecciona todos los elementos `<input>` con un valor válido.
- **:visited**: Selecciona todos los enlaces visitados.