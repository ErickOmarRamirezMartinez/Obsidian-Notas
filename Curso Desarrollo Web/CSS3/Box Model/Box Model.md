## El modelo de caja CSS

En CSS, el término "box model" se utiliza cuando se habla de diseño y maquetación.

El modelo de caja CSS es esencialmente una caja que envuelve cada elemento HTML. Consta de: contenido, relleno, bordes y márgenes. La siguiente imagen ilustra el modelo de caja:
![[Pasted image 20240404195022.png]]

Explicación de las diferentes partes:

- **Content**: el contenido del cuadro, donde aparecen el texto y las imágenes.
- **Padding:** despeja un área alrededor del contenido. El acolchado es transparente
- **Border**: un borde que rodea el relleno y el contenido
- **Margin**: despeja un área fuera del borde. El margen es transparente


>**Importante:** Al establecer las propiedades width y height de un con CSS, solo tienes que establecer el ancho y el alto del **área de contenido**. Para Calcula el ancho y alto total de un elemento, también debes incluir el relleno (padding) y los bordes (border).

## Heigth y Width (Altura y Anchura)
## Ejemplo
Cuanto de width y heigth tendra este div?

```css
div {  width: 320px;  
  height: 50px;  
  padding: 10px;  
  border: 5px solid gray;  
  margin: 0;}
```

Aquí está el cálculo:  

320px (ancho del área de contenido)  
+20px (relleno izquierdo + relleno derecho)  
+10px (borde izquierdo + borde derecho)  
**= 350px (ancho total)**  
  
50px (altura del área de contenido)  
+20px (relleno superior + relleno inferior)  
+10px (borde superior + borde inferior)  
**= 80px (altura total)**

El ancho total de un elemento debe calcularse de la siguiente manera:

Ancho total del elemento = ancho + relleno izquierdo + relleno derecho + borde izquierdo + borde derecho

La altura total de un elemento debe calcularse de la siguiente manera:

Altura total del elemento = altura + relleno superior + relleno inferior + borde superior + borde inferior

![[Pasted image 20240404202258.png]]

---

# CSS Outline

Un contorno es una línea dibujada fuera del borde del elemento.
Un contorno es una línea que se dibuja alrededor de los elementos, FUERA de los bordes, para hacer que el elemento "se destaque".

![[Pasted image 20240404205351.png]]

CSS tiene las siguientes propiedades de esquema:

- `outline-style`
- `outline-color`
- `outline-width`
- `outline-offset`
- `outline`

>**Nota:** ¡El contorno difiere de [los bordes](https://www.w3schools.com/css/css_border.asp)! A diferencia del borde, el contorno es dibujado fuera del borde del elemento y puede superponerse a otro contenido. Además, el esquema es NO forma parte de las dimensiones del elemento; la anchura y la altura totales del elemento no se ve afectado por la anchura del contorno.

## CSS Outline Style

La propiedad especifica el estilo del contorno, y puede tener uno de los siguientes valores:`outline-style`

- `dotted` - Define un contorno punteado
- `dashed` - Define un contorno discontinuo
- `solid` - Define un contorno sólido
- `double` - Define un doble contorno
- `groove` - Define un contorno ranurado en 3D
- `ridge` - Define un contorno estriado en 3D
- `inset` - Define un contorno de inserción 3D
- `outset` - Define un contorno inicial 3D
- `none` - No define ningún contorno
- `hidden` - Define un contorno oculto

```css
p.dotted {outline-style: dotted;}  
p.dashed {outline-style: dashed;}  
p.solid {outline-style: solid;}  
p.double {outline-style: double;}  
p.groove {outline-style: groove;}  
p.ridge {outline-style: ridge;}  
p.inset {outline-style: inset;}  
p.outset {outline-style: outset;}
```

![[Pasted image 20240404205838.png]]

## Propiedad abreviada

La propiedad es una propiedad abreviada de Establecer las siguientes propiedades de esquema individuales:`outline`

- `outline-width`
- `outline-style` (obligatorio)
- `outline-color`

La propiedad se especifica como uno, dos o tres valores de la lista anterior. El orden de los valores no materia.`outline`

En el ejemplo siguiente se muestran algunos contornos especificados con la propiedad abreviada:`outline`

```css
p.ex1 {outline: dashed;}  
p.ex2 {outline: dotted red;}  
p.ex3 {outline: 5px solid yellow;}  
p.ex4 {outline: thick ridge pink;}
```

## Desplazamiento de contorno CSS

La propiedad añade espacio entre un contorno y el borde/borde de un elemento. El espacio entre un y su contorno es transparente.`outline-offset`

El siguiente ejemplo especifica un contorno de 15px fuera del borde del borde:

![[Pasted image 20240404210654.png]]

```css
p {  margin: 30px;  
  border: 1px solid black;  
  outline: 1px solid red;  
  outline-offset: 15px;}
```


---
# CSS Box Sizing

## Con la propiedad CSS box-sizing

La propiedad nos permite incluir el relleno y el borde en la anchura y la altura totales de un elemento.`box-sizing`

Si se establece en un elemento, el relleno y el borde son Incluido en el ancho y alto:`box-sizing: border-box;`
```css
.div1 {  width: 300px;  
  height: 100px;  
  border: 1px solid blue;  
  box-sizing: border-box;}  
  
.div2 {  width: 300px;  
  height: 100px;  
  padding: 50px;  
  border: 1px solid red;  
  box-sizing: border-box;}

```

![[Pasted image 20240404211748.png]]

Dado que el resultado de usar el método es mucho mejor, muchos desarrolladores quieren que todos los elementos en su páginas para trabajar de esta manera.`box-sizing: border-box;`

El siguiente código garantiza que todos los elementos tengan un tamaño más intuitivo. Muchos navegadores ya utilizan para muchos elementos de forma (pero no todos, por lo que Las entradas y las áreas de texto se ven diferentes en el ancho: 100% ;). `box-sizing: border-box;`

**Simplificación de cálculos de dimensiones**: Al aplicar `box-sizing: border-box;`, el ancho y alto de un elemento incluyen el padding y el borde, pero no el margen. Esto significa que, si estableces un elemento para que tenga un ancho de 100px y luego le añades un padding de 20px y un borde de 5px, el elemento seguirá teniendo un ancho total de 100px. Sin `box-sizing: border-box;`, el ancho final sería 150px (100px de ancho + 20px de padding a cada lado + 5px de borde a cada lado), lo que puede hacer que los cálculos de dimensiones sean más complejos y menos predecibles.

==***Aplicar esto a todos los elementos es seguro y sabio:***==

```css
* {  
box-sizing: border-box;
}
```
![[Pasted image 20240404212136.png]]


# Ejemplo:
 ``` html
<style>

.div1 {

width: 200px;

height: 200px;

padding: 20px;

border: 5px solid black;

margin: 10px;

background-color: lightblue;

}

.div2 {

width: 200px;

height: 200px;

padding: 20px;

border: 5px solid red;

margin: 10px;

box-sizing: border-box;

background-color: lightgreen;

}

</style>

</head>

<body>

<h1>Introduccion a Box Model</h1>

  

<div>Mi Contenido</div>

  

<hr>

  

<div class="div1">Sin border-box</div>

  

<div class="div2">Con border-box</div>
```

![[Pasted image 20240404213503.png]]

![[Pasted image 20240404213528.png]]

---

# Como centrar un elemento inline en CSS

```css
margin: 0 auto;
```

![[Pasted image 20240404214611.png]]

---
# Margin Collapse
## Colapso de márgenes

Los márgenes superior e inferior de los elementos a veces se contraen en un solo margen que es igual al mayor de los dos márgenes.

¡Esto no sucede en los márgenes izquierdo y derecho! ¡Solo márgenes superior e inferior!

Observa el siguiente ejemplo:

```css
h1 {  margin: 0 0 50px 0;}  
  
h2 {  margin: 20px 0 0 0;}
```

En el ejemplo anterior, el elemento `<h1>` tiene un margen inferior de 50px y El `<h2>` tiene un margen superior establecido en 20px.

El sentido común parecería sugerir que el margen vertical entre el `<h1>` y el `<h2>` sería un total de 70px (50px + 20px). Pero debido al colapso de los márgenes, El margen real termina siendo de 50px.

![[Pasted image 20240406232344.png]]