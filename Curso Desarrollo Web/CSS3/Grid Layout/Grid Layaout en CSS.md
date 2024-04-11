# Módulo de diseño de cuadrícula CSS
![[Pasted image 20240410195225.png]]

## Grid Elements
Un diseño de cuadrícula consta de un elemento primario, con uno o más elementos secundarios.

```html
<div class="grid-container">  
  <div class="grid-item">1</div>  
  <div class="grid-item">2</div>  
  <div class="grid-item">3</div>  
  <div class="grid-item">4</div>  
  <div class="grid-item">5</div>  
  <div class="grid-item">6</div>  
  <div class="grid-item">7</div>  
  <div class="grid-item">8</div>  
  <div class="grid-item">9</div>  
</div>
```

```css
.grid-container{

display: grid;

grid-template-columns: auto auto auto ;

background-color: aquamarine;

padding: 10px;

border: 1px solid black;

margin: 20px auto;

  

}

.grid-item{

background-color: rgba(255, 255, 255, 0.8);

border: 1px solid black;

padding: 20px;

text-align: center;

}
```

![[Pasted image 20240410200743.png]]


## Display Property
Un elemento HTML se convierte en un contenedor de cuadrícula cuando su propiedad se establece en `display``grid` o `inline-grid`.
```css
.grid-container{

display: inline-grid;

grid-template-columns: auto auto auto ;

background-color: aquamarine;

padding: 10px;

border: 1px solid black;

margin: 20px auto;
}
```

![[Pasted image 20240410200833.png]]

---

## Grid Columns
Las líneas verticales de los elementos de cuadrícula se denominan _columnas_.
![[Pasted image 20240410200937.png]]


## Grid Rows
Las líneas horizontales de los elementos de la cuadrícula se denominan _filas_.
![[Pasted image 20240410201030.png]]

## Grid Gaps
Los espacios entre cada columna/fila se denominan _huecos_.
![[Pasted image 20240410201217.png]]
Puede ajustar el tamaño del hueco mediante una de las siguientes propiedades:

- `column-gap`
  La propiedad establece el espacio entre las columnas
- `row-gap`
  La propiedad establece el espacio entre las filas
- `gap`
  La propiedad es una propiedad abreviada de las propiedades y las siguientes:`gap`: `row-gap``column-gap`
  La propiedad también se puede usar para establecer tanto el espacio entre filas como el Separación de columna en un valor:`gap: 50px;`

```css
.grid-container{

display: inline-grid;

grid-template-columns: auto auto auto ;

gap: 20px 20px;

  
  

background-color: aquamarine;

padding: 10px;

border: 1px solid black;

margin: 20px auto;

  

}

```

![[Pasted image 20240410202253.png]]

---

## Líneas de cuadrícula

Las líneas entre columnas se denominan _líneas de columna_.

Las líneas entre filas se denominan _líneas de fila_.

![[Pasted image 20240410202547.png]]

---
## Ejemplo de una Maquetacion general de una pagina web

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

<div class="grid-container">

<div class="item1">Encabezado</div>

<div class="item2">Menu</div>

<div class="item3">Principal</div>

<div class="item4">Derecha</div>

<div class="item5">Pie de Pagina</div>

</div>

</body>

</html>
```


```css
html, body{

height: 100%;

margin: 0;

overflow: hidden;

}

  

.grid-container{

display: grid;

grid-template-columns: auto auto auto ;

gap: 20px;

  

width: 100vw;

height: 100vh;

  
  

background-color: aquamarine;

padding: 10px;

border: 1px solid black;

margin: 0 auto;

  

}

.grid-container > div {

background-color: rgba(255, 255, 255, 0.8);

text-align: center;

padding: 20px 0;

font-size: 30px;

}

  

.item1 {

grid-column-start: 1;

grid-column-end: 4;

}

.item2{

grid-row-start: 2;

grid-row-end: 5;

}

.item3{

grid-row-start: 2;

grid-row-end: 4;

}

.item4{

grid-row-start: 2;

grid-row-end: 4;

}

.item5{

grid-column-start: 2;

grid-column-end: 4;

grid-row-start: 4;

grid-row-end: 5;

}
```

![[Pasted image 20240410210210.png]]