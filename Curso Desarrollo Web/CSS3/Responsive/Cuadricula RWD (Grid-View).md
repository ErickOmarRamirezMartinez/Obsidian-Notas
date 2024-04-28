# Diseño Web Responsivo - Introducción

El diseño web responsivo hace que su página web se vea bien en todos los dispositivos.

El diseño web responsivo utiliza solo HTML y CSS.

El diseño web responsivo no es un programa ni un JavaScript.

## Diseñando para la mejor experiencia para todos los usuarios

Las páginas web se pueden ver utilizando muchos dispositivos diferentes: computadoras de escritorio, tabletas y teléfonos. Su página web debe verse bien y ser fácil de usar, independientemente del dispositivo.

Las páginas web no deben dejar de lado la información para adaptarse a dispositivos más pequeños, sino adaptar su contenido para adaptarse a cualquier dispositivo:

  

![](https://www.w3schools.com/css/rwd_desktop.png)  
Escritorio

![](https://www.w3schools.com/css/rwd_tablet.png)  
Tableta

![](https://www.w3schools.com/css/rwd_phone.png)  
Teléfono

Se llama diseño web responsivo cuando usa CSS y HTML para cambiar el tamaño, ocultar, reducir, ampliar o mover el contenido para que se vea bien en cualquier pantalla.

--- 
## ¿Qué es The Viewport?

La ventanilla es el área visible del usuario de una página web.

La ventana gráfica varía según el dispositivo y será más pequeña en un teléfono móvil que en la pantalla de una computadora.

Antes de las tabletas y los teléfonos móviles, las páginas web se diseñaban solo para pantallas de computadora, y era común que páginas web para tener un diseño estático y un tamaño fijo.

Luego, cuando empezamos a navegar por internet usando tabletas y teléfonos móviles, Las páginas web de tamaño eran demasiado grandes para caber en la ventanilla. Para solucionar esto, los navegadores de esos dispositivos redujeron la escala de toda la página web para que se ajustara a la pantalla.

¡Esto no fue perfecto! Pero una solución rápida.

## Configuración de la ventanilla

HTML5 introdujo un método para permitir que los diseñadores web tomaran el control de la ventana gráfica, a través de la etiqueta.`<meta>`

Debe incluir el siguiente elemento de ventanilla en todas sus páginas web:`<meta>`


>Si usas un diseño adaptable, debes indicarle al navegador que no realice ese escalamiento. Puedes hacerlo con un elemento `meta` en el `head` de la página web:


```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
* La parte establece el ancho de la página para seguir el ancho de la pantalla del dispositivo (que variará según el dispositivo).`width=device-width`

* La pieza establece el nivel de zoom inicial cuando el navegador carga la página por primera vez.`initial-scale=1.0`

Esto le da al navegador instrucciones sobre cómo para controlar las dimensiones y la escala de la página.

## Ajustar el tamaño del contenido a la ventanilla

Los usuarios están acostumbrados a desplazarse por los sitios web verticalmente tanto en computadoras de escritorio como en dispositivos móviles dispositivos, ¡pero no horizontalmente!

Por lo tanto, si el usuario se ve obligado a desplazarse horizontalmente, o alejarse, para ver el Toda la página web da como resultado una mala experiencia de usuario.

Algunas reglas adicionales a seguir:

===**1. NO utilice elementos grandes de ancho fijo,**== por ejemplo, si una imagen se muestra con un ancho más ancho que la ventana gráfica, puede causar el ventanilla para desplazarse horizontalmente. Recuerde ajustar este contenido para que quepa dentro de El ancho de la ventanilla.

==**2. NO permita que el contenido dependa de un ancho de ventana gráfica en particular para render well**==: dado que las dimensiones y el ancho de la pantalla en píxeles CSS varían Ampliamente entre dispositivos, el contenido no debe depender de un ancho de ventana gráfica en particular para renderizar bien.

==**3. Utilice consultas de medios CSS para aplicar diferentes estilos para pequeñas y pantallas grandes**==: configuración de grandes anchos CSS absolutos para los elementos de la página hará que el elemento sea demasiado ancho para la ventanilla en un dispositivo más pequeño. En su lugar, considere la posibilidad de usar valores de ancho relativo, como width: 100%. Además, sea Cuidado con el uso de grandes valores de posicionamiento absolutos. Puede hacer que el elemento quedan fuera de la ventanilla en dispositivos pequeños.

---
## ¿Qué es una vista de cuadrícula?

Muchas páginas web se basan en una vista de cuadrícula, lo que significa que la página está dividida en columnas:

El uso de una vista de cuadrícula es muy útil a la hora de diseñar páginas web. Facilita la colocación de elementos en la página.

![[Pasted image 20240411202911.png]]
## Creación de una vista de cuadrícula adaptable

Comencemos a construir una vista de cuadrícula receptiva.

1. En primer lugar, asegúrese de que todos los elementos HTML tengan la propiedad establecida en . Esto asegura que el relleno y el borde estén incluidos en el ancho y alto totales de los elementos.`box-sizing``border-box`

```css
* {  box-sizing: border-box;}
```

Sin embargo, queremos usar una vista de cuadrícula receptiva con 12 columnas, para tener más Control sobre la página web.

Primero debemos calcular el porcentaje para una columna: 100% / 12 columnas = 8.33%.

2. A continuación, Hacer una clase para cada una de las 12 columnas, y un número Definir el número de columnas que debe abarcar la sección:`class="col-"`

```css
.col-1 {width: 8.33%;}  
.col-2 {width: 16.66%;}  
.col-3 {width: 25%;}  
.col-4 {width: 33.33%;}  
.col-5 {width: 41.66%;}  
.col-6 {width: 50%;}  
.col-7 {width: 58.33%;}  
.col-8 {width: 66.66%;}  
.col-9 {width: 75%;}  
.col-10 {width: 83.33%;}  
.col-11 {width: 91.66%;}  
.col-12 {width: 100%;}
```


3. Todas estas columnas deben estar flotando a la izquierda y tener un relleno de 15px:
```css
[class*="col-"] {  float: left;  
  padding: 15px;  
  border: 1px solid red;}
```

4. Cada fila debe estar envuelta en un archivo . El número de columnas Dentro de una fila siempre debe sumar 12:`<div>`

 ```html
<div class="row">  
  <div class="col-3">...</div> <!-- 25% -->  
  <div class="col-9">...</div> <!-- 75% -->  
</div>
```

y por ultimo

5. Las columnas dentro de una fila están todas flotando hacia la izquierda y, por lo tanto, sacados del flujo de la página, y otros elementos se colocarán como si las columnas no existieran. Para evitarlo, haremos lo siguiente: Agregue un estilo que despeje el flujo:
```css
.row::after {  content: "";  
  clear: both;  
  display: table;}
```


### Ejemplo: 

```html 
<div class="col-12 header">

<h1>Chania</h1>

</div>

<div class="row">

<div class="col-3 menu">

<ul>

<li>The Flight</li>

<li>The City</li>

<li>The Island</li>

<li>The Food</li>

</ul>

</div>

<div class="col-9">

<h1>The City</h1>

<p>Chania is the capital of the Chania region on the island of Crete. The city can be divided in two parts, the old town and the modern city.</p>

<p>Resize the browser window to see how the content respond to the resizing.</p>

</div>
  
<div class="col-4">

<h2>Noticias</h2>

<p>Ex incididunt Lorem reprehenderit labore esse.</p>

<p>Eiusmod ea qui occaecat cupidatat labore magna proident officia sint magna eiusmod elit tempor aute. Elit reprehenderit non enim excepteur reprehenderit do. Amet tempor voluptate excepteur officia et fugiat mollit mollit. Ad laborum dolor aute velit fugiat sunt mollit anim culpa aliquip consequat. Fugiat est officia adipisicing culpa deserunt anim nulla eiusmod sint dolor pariatur et. Irure tempor deserunt exercitation consequat laborum aliquip aliquip velit qui. Velit culpa irure voluptate incididunt nulla anim.</p>

</div>

  

<div class="col-4">

<h2>Noticias</h2>

<p>Ex incididunt Lorem reprehenderit labore esse.</p>

<p>Eiusmod ea qui occaecat cupidatat labore magna proident officia sint magna eiusmod elit tempor aute. Elit reprehenderit non enim excepteur reprehenderit do. Amet tempor voluptate excepteur officia et fugiat mollit mollit. Ad laborum dolor aute velit fugiat sunt mollit anim culpa aliquip consequat. Fugiat est officia adipisicing culpa deserunt anim nulla eiusmod sint dolor pariatur et. Irure tempor deserunt exercitation consequat laborum aliquip aliquip velit qui. Velit culpa irure voluptate incididunt nulla anim.</p>

</div>

  

<div class="col-4">

<h2>Noticias</h2>

<p>Ex incididunt Lorem reprehenderit labore esse.</p>

<p>Eiusmod ea qui occaecat cupidatat labore magna proident officia sint magna eiusmod elit tempor aute. Elit reprehenderit non enim excepteur reprehenderit do. Amet tempor voluptate excepteur officia et fugiat mollit mollit. Ad laborum dolor aute velit fugiat sunt mollit anim culpa aliquip consequat. Fugiat est officia adipisicing culpa deserunt anim nulla eiusmod sint dolor pariatur et. Irure tempor deserunt exercitation consequat laborum aliquip aliquip velit qui. Velit culpa irure voluptate incididunt nulla anim.</p>

</div>

  

</div>

```

```css
* {

box-sizing: border-box;

}

.row::after {

content: "";

clear: both;

display: table;

}

[class*="col-"] {

float: left;

padding: 15px;

}

.col-1 {width: 8.33%;}

.col-2 {width: 16.66%;}

  

.col-3 {width: 25%;}

.col-4 {width: 33.33%;}

.col-5 {width: 41.66%;}

.col-6 {width: 50%;}

.col-7 {width: 58.33%;}

.col-8 {width: 66.66%;}

  

.col-9 {width: 75%;}

  
  

.col-10 {width: 83.33%;}

.col-11 {width: 91.66%;}

.col-12 {width: 100%;}

html {

font-family: "Lucida Sans", sans-serif;

}

.header {

background-color: #9933cc;

color: #ffffff;

}

.menu ul {

list-style-type: none;

margin: 0;

padding: 0;

}

.menu li {

padding: 8px;

margin-bottom: 7px;

background-color: #33b5e5;

color: #ffffff;

box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);

}

.menu li:hover {

background-color: #0099cc;

}
```

![[Pasted image 20240411210437.png]]

