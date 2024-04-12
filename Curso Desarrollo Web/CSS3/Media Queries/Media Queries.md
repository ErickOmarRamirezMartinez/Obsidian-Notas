## ¿Qué es una media querie?
Las medias queries es una técnica CSS introducida en CSS3.

Utiliza la regla para incluir un bloque de propiedades CSS solo si un cierta condición es verdadera.`@media`

## Adición de un punto de interrupción

Anteriormente en este tutorial hicimos una página web con filas y columnas, y respondía, pero no se veía bien en una pantalla pequeña.

Las consultas de medios pueden ayudar con eso. Podemos agregar un punto de interrupción donde Ciertas partes del diseño se comportarán de manera diferente en cada lado del punto de ruptura.
  
![](https://www.w3schools.com/css/rwd_desktop.png)  
Escritorio

![](https://www.w3schools.com/css/rwd_phone.png)  
Teléfono

## Ejemplo:
Cuando la pantalla (ventana del navegador) tiene menos de 768 px, cada columna debe tener un ancho del 100%:
[[Selectores de atributos CSS#Selector [attribute*="value"]]]]

```css
@media only screen and (max-width: 768px) {
  /* For mobile phones: */
  [class*="col-"] {
    width: 100%;
  }
}
```
![[Pasted image 20240411215407.png]]

---
## Diseñe siempre primero para dispositivos móviles (Mobile First)

Mobile First significa diseñar para dispositivos móviles antes de diseñar para computadoras de escritorio o cualquier otra opción. otro dispositivo (esto hará que la página se muestre más rápido en dispositivos más pequeños).

Esto significa que debemos hacer algunos cambios en nuestro CSS.

En lugar de cambiar los estilos cuando el ancho se hace _más pequeño_ que 768px, deberíamos cambiar el diseño cuando el ancho sea _mayor_ que 768px. Esto hará que nuestro diseño sea Mobile First:

---
## Otro punto de quiebre

Puede agregar tantos puntos de interrupción como desee.

También insertaremos un punto de interrupción entre tabletas y teléfonos móviles.

![](https://www.w3schools.com/css/rwd_desktop.png)  
Escritorio

![](https://www.w3schools.com/css/rwd_tablet.png)  
Tableta

![](https://www.w3schools.com/css/rwd_phone.png)  
Teléfono

  

Para ello, añadimos una consulta de medios más (a 600 px) y un conjunto de nuevas clases para dispositivos de más de 600 píxeles (pero menor que 768px):

> Tenga en cuenta que los dos conjuntos de clases son casi idénticos, el único La diferencia es el nombre ( y ):`col-``col-s-`

```css
/* For mobile phones: */  
[class*="col-"] {  width: 100%;}  
  
@media only screen and (min-width: 600px) {  /* For tablets: */  
  .col-s-1 {width: 8.33%;}  
  .col-s-2 {width: 16.66%;}  
  .col-s-3 {width: 25%;}  
  .col-s-4 {width: 33.33%;}  
  .col-s-5 {width: 41.66%;}  
  .col-s-6 {width: 50%;}  
  .col-s-7 {width: 58.33%;}  
  .col-s-8 {width: 66.66%;}  
  .col-s-9 {width: 75%;}  
  .col-s-10 {width: 83.33%;}  
  .col-s-11 {width: 91.66%;}  
  .col-s-12 {width: 100%;}}  
  
@media only screen and (min-width: 768px) {  /* For desktop: */  
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
  .col-12 {width: 100%;}}

```

La primera sección abarcará 3 columnas, la segunda abarcará 9 y la tercera sección se mostrará debajo de las dos primeras secciones, y abarcará 12 columnas:
```html 
<div class="row">  
  <div class="col-3 col-s-3">...</div>  
  <div class="col-6 col-s-9">...</div>  
  <div class="col-3 col-s-12">...</div>  
</div>
```

![[Pasted image 20240411222423.png]]
![[Pasted image 20240411222502.png]]
![[Pasted image 20240411222522.png]]

---
# Puntos de interrupción típicos de dispositivos

Hay toneladas de pantallas y dispositivos con diferentes alturas y anchos, por lo que es difícil crear un punto de interrupción exacto para cada dispositivo. Para simplificar las cosas, podrías apuntar a Cinco grupos:

```css
/* 
Dispositivos extra pequeños (teléfonos, 600 px y menos) */  
@media only screen and (max-width: 600px) {...}  
  
/* 
Dispositivos pequeños (tabletas verticales y teléfonos grandes, 600 px y más) */  
@media only screen and (min-width: 600px) {...}  
  
/* 
Dispositivos medianos (tabletas horizontales, 768 px y superiores)*/  
@media only screen and (min-width: 768px) {...}  
  
/*   
Dispositivos grandes (portátiles/de escritorio, 992 px y más) */  
@media only screen and (min-width: 992px) {...}  
  
/*
Dispositivos extragrandes (portátiles y de sobremesa grandes, de 1200 px y más) 
*/  
@media only screen and (min-width: 1200px) {...}

```

Para poder ver los diferentes tamaños
```html
<p class="example">Resize the browser window to see how the background color of this paragraph changes on different screen sizes.</p>
```

```css
.example {
  padding: 20px;
  color: white;
}
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .example {background: red;}
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {
  .example {background: green;}
}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  .example {background: blue;}
} 

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  .example {background: orange;}
} 

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  .example {background: pink;}
}
```

---
## Orientacion: Portrait / Landscape

Los media queries también se pueden utilizar para cambiar el diseño de una página en función de la orientación del navegador.

Puede tener un conjunto de propiedades CSS que solo cuando la ventana del navegador es más ancha que su altura, lo que se denomina "Landscape" orientación:
> En otras palabras, cuando el dispositivo este en vertical, activara el media queri

```css
body {
  background-color: lightgreen;
}

@media only screen and (orientation: landscape) {
  body {
    background-color: lightblue;
  }
}

```

![[Pasted image 20240411224325.png]]
![[Pasted image 20240411224340.png]]

---
## Ocultar elementos con consultas de medios

Otro uso común de las consultas de medios es ocultar elementos en diferentes tamaños de pantalla:
 ```css
 div.example {
  background-color: yellow;
  padding: 20px;
}

@media screen and (max-width: 600px) {
  div.example {
    display: none;
  }
}
```
![[Pasted image 20240411225139.png]]
![[Pasted image 20240411225152.png]]

---
## Cambiar el tamaño de la fuente con las consultas de medios

También puede usar consultas de medios para cambiar el tamaño de fuente de un elemento en Diferentes tamaños de pantalla:

```css
/* If the screen size is 601px or more, set the font-size of <div> to 80px */  
@media only screen and (min-width: 601px) {  div.example {    font-size: 80px;  }}  
  
/* If the screen size is 600px or less, set the font-size of <div> to 30px */  
@media only screen and (max-width: 600px) {  div.example {    font-size: 30px;  }}
```
![[Pasted image 20240411225510.png]]
![[Pasted image 20240411225530.png]]
