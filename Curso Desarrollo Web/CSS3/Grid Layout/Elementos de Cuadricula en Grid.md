## La propiedad grid-area

La propiedad se puede utilizar como una propiedad abreviada para las propiedades , y las propiedades.`grid-area``grid-row-start``grid-column-start``grid-row-end``grid-column-end`

```html
<div class="grid-container">

<div class="item1">1</div>

<div class="item2">2</div>

<div class="item3">3</div>

<div class="item4">4</div>

<div class="item5">5</div>

<div class="item6">6</div>

<div class="item7">7</div>

<div class="item8">8</div>

<div class="item9">9</div>

<div class="item10">10</div>

<div class="item11">11</div>

<div class="item12">12</div>

<div class="item13">13</div>

<div class="item14">14</div>

<div class="item15">15</div>

</div>
```

```css
.item3{

grid-area: 1 / 2 / 5 / 6;

}
```

![[Pasted image 20240410215639.png]]


---
## Nomenclatura de elementos de cuadrícula

La propiedad también se puede utilizar para asignar nombres a elementos de cuadrícula.`grid-area`

La propiedad puede hacer referencia a los elementos de cuadrícula con nombre del contenedor de la rejilla.`grid-template-areas`


## Ejemplo de una Maquetacion general de una pagina web

```html
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Document</title>

<link rel="stylesheet" href="stylex2.css">

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
.grid-container{

display: grid;

gap: 20px;

  

width: 100vw;

height: 100vh;

  
  

background-color: aquamarine;

padding: 10px;

border: 1px solid black;

margin: 0 auto;

  
  

grid-template-areas:

'encabezado encabezado encabezado encabezado '

'menu principal derecha derecha'

'menu principal derecha derecha'

'menu principal derecha derecha'

'menu footer footer footer ';

  

}

.grid-container > div {

background-color: rgba(255, 255, 255, 0.8);

text-align: center;

padding: 20px 0;

font-size: 30px;

}

.item1{grid-area: encabezado;}

.item2{grid-area: menu;}

.item3{grid-area: principal;}

.item4{grid-area: derecha;}

.item5{grid-area: footer;}
```

![[Pasted image 20240410222440.png]]