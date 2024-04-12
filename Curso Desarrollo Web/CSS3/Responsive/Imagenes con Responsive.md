## Uso de la propiedad max-width
Si la propiedad se establece en un porcentaje y la propiedad se establece en "auto", la imagen será Responsivo y escalable hacia arriba y hacia abajo:`width``height`

Si la propiedad se establece en 100%, la imagen se reducirá verticalmente si es necesario, pero nunca se ampliará para que sea más grande que su Tamaño original:`max-width`

```html
<div class="col-6 col-s-9">

<h1>75% porciento</h1>

<p>Chania is the capital of the Chania region on the island of Crete. The city can be divided in two parts, the old town and the modern city.</p>

<img src="https://i.pinimg.com/736x/87/c4/5f/87c45f28647106d9d8f41ba8b7375d9f.jpg" width="460" height="345">

</div>
```

```css
img{

max-width: 100%;

height: auto;

}
```

![[Pasted image 20240411230917.png]]
![[Pasted image 20240411230935.png]]
![[Pasted image 20240411230956.png]]

---
## Propiedades de ` background-size:`
Las imágenes de fondo también pueden responder al cambio de tamaño y escalado.


1. Si la propiedad está configurada como `contain`, el fondo La imagen se escalará e intentará ajustarse al área de contenido. Sin embargo, la imagen mantendrá su relación de aspecto (la relación proporcional entre la anchura y la altura de la imagen):
```css
div {  width: 100%;  
  height: 400px;  
  background-image: url('img_flowers.jpg');  
  background-repeat: no-repeat;  
  background-size: contain;  
  border: 1px solid red;}
```
![[Pasted image 20240411233023.png]]

2. Si la propiedad se establece en `100% 100%`, la imagen de fondo se estirará para cubrir toda el área de contenido:
```css
div {  width: 100%;  
  height: 400px;  
  background-image: url('img_flowers.jpg');  
  background-size: 100% 100%;  
  border: 1px solid red;}
```
![[Pasted image 20240411233104.png]]

3. Si la propiedad está configurada en `cover`, la imagen de fondo se escalará para cubrir toda el área de contenido. Tenga en cuenta que el valor "cover" mantiene el aspecto y una parte de la imagen de fondo puede ser Recortado:
```css
div {  width: 100%;  
  height: 400px;  
  background-image: url('img_flowers.jpg');  
  background-size: cover;  
  border: 1px solid red;}

```


---
## Hacer aparecer y desaparecer una imagen 

```css
/* For width smaller than 400px: */  
body {  background-image: url('img_smallflower.jpg');}  
  
/* For width 400px and larger: */  
@media only screen and (min-width: 400px) {  
body {    
background-image: url('img_flowers.jpg');  
}
}
```
![[Pasted image 20240411233404.png]]
![[Pasted image 20240411233417.png]]

---
## El elemento HTML `<picture>`

El elemento HTML le da a web Más flexibilidad para los desarrolladores a la hora de especificar los recursos de imagen.`<picture>`

El uso más común del elemento será para imágenes utilizadas en diseños responsivos. En lugar de tener uno imagen que se escala hacia arriba o hacia abajo en función de la anchura de la ventanilla, se pueden estar diseñado para llenar mejor la ventana gráfica del navegador.`<picture>`

El elemento funciona de forma similar a los elementos and. Configura diferentes orígenes, y el primer origen que se ajuste a la propiedad preferences es la que se está utilizando:`<picture>``<video>``<audio>`

```html
<div class="col-12">

<picture>

<source srcset="./imagen1.jpg" media="(max-width: 400px)">

<source srcset="./imagen2.jpeg">

<img src="imagen1.jpg" alt="Mariposa" >

</picture>

</div>
```
![[Pasted image 20240411234445.png]]
![[Pasted image 20240411234509.png]]


