![[Pasted image 20240406213952.png]]

## La propiedad z-index

Cuando los elementos se colocan, pueden superponerse a otros elementos.

La propiedad especifica `z-index` es el orden de pila de un elemento (qué elemento debe colocarse delante o detrás de los demás).

Un elemento puede tener un orden de pila positivo o negativo:

```html
<h1>Z-Index</h1>

<p>Quis sit aliqua veniam cupidatat est eiusmod culpa nisi officia.</p>

<div class="container">

<div class="black-box">Black box (z-index: 1)

<div class="gray-box">Gray box (z-index: 3)</div>

<div class="green-box">Green box (z-index: 2)</div></div>

</div>
```

![[Pasted image 20240406220540.png]]

```css
.container {

position: relative;

}

div.black-box{

position: relative;

z-index: 1;

border: 1px solid black;

text-align: left;

height: 100px;

margin: 30px;

}

div.gray-box{

position: absolute;

z-index: 3;

background-color: gray;

height: 90px;

width: 500px;

bottom: -15px;

  

}

div.green-box{

position: absolute;

z-index: 2;

background-color: green;

height: 70px;

width: 300px;

top: -15px;

right: 0;

  

}
```


---
# Imagen con Texto Centrado 

```html 
<h1>Ejercicio Imagen</h1>

<div id="container2">

<img src="https://cdn-icons-png.flaticon.com/256/174/174854.png" alt="" class="imagen">

<div class="centroo">Logo HTML5</div>

</div>
```

```css
div#container2{

position: relative;

border: 2px dotted black;

width: 50%;

max-width: 300px;

margin: 0 auto;

}

img.imagen{

width: 100%;

opacity: 0.5; 

}

div.centroo{

position: absolute;

top: 50%;

margin: auto;

border: 2px solid black;

width: 100%;

text-align: center;

font-size: 20px;

}
```

![[Pasted image 20240406222919.png]]