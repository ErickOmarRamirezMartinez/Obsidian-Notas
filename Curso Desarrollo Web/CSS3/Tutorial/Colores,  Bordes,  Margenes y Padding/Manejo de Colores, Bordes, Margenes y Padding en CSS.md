![[Pasted image 20240403222412.png]]

# Colores
## Valores de color CSS

En CSS, los colores también se pueden especificar mediante valores RGB, valores HEX, HSL valores, valores RGBA y valores HSLA:

Igual que el nombre del color "Tomate":
![[Pasted image 20240404220306.png]]
Igual que el nombre del color "Tomate", pero 50% transparente:
![[Pasted image 20240404220320.png]]

---

# Manejo de Bordes

![[Pasted image 20240404190304.png]]

```html
<h1>Bordes en CSS</h1>

<p class="punteado">Borde Punteado</p>

<p class="discontinuo">Borde Discontinuo</p>

<p class="solido">Borde Solido</p>

<p class="doble">Borde Doble</p>

<p class="surco">Borde Surco</p>

<p class="cresta">Borde Cresta</p>

<p class="recuadro">Borde Recuadro</p>

<p class="outset">Borde Inverso</p>

<p class="sin_borde">Sin borde</p>

<p class="oculto">Borde Oculto</p>

<p class="mixto">Borde Mixto</p>

```

```css
.punteado{

border-style: dotted;

}

.discontinuo{

border-style:dashed ;

}

.solido{

border: 10px solid red;

}

.doble{

border: 10px double yellowgreen;

}

.surco{

border: 10px groove;

}

.cresta{

border: 10px ridge;

}

  

.recuadro{

border: 10px inset;

}

.outset{

border: 10px outset;

}

.sin_borde{

border: none;

}

.oculto{

border:hidden ;

}

.mixto{

border-style: dotted solid dashed double;

}
```


---

# Ancho de Bordes

## Ancho del borde CSS

La propiedad especifica el ancho de los cuatro bordes.`border-width`

El ancho se puede establecer como un tamaño específico (en px, pt, cm, em, etc.) o usando Uno de los tres valores predefinidos: fino, medio o grueso:

```html
<h1>Bordes en CSS</h1>

<p class="punteado">Borde Punteado</p>

<p class="discontinuo">Borde Discontinuo</p>

<p class="solido">Borde Solido</p>

<p class="doble">Borde Doble</p>

```


```css
.punteado{

border-style: dotted;

border-width: 10px 5px 3px 2px;

}

.discontinuo{

border-style:dashed ;

border-width: thick; /* thin , medium y thick*/

}

.solido{

border: solid red;

border-width: 10px 5px 2px ;

}

.doble{

border: 10px double yellowgreen;

border-width: 10px 5px;

}
```

![[Pasted image 20240404192049.png]]


---
## Color del borde CSS

La propiedad se utiliza para establecer el color de los cuatro bordes.`border-color`

El color se puede establecer mediante:

- Nombre: especifique un nombre de color, como "rojo"
- HEX: especifique un valor HEX, como "#ff0000"
- RGB: especifique un valor RGB, como "rgb(255,0,0)"
- HSL: especifique un valor HSL, como "hsl(0, 100%, 50%)"
- transparente

**Nota:** Si no se establece, hereda el color del elemento.`border-color`

```css
p.one {  border-style: solid;  
  border-color: red;}  
  
p.two {  border-style: solid;  
  border-color: green;}  
  
p.three {  border-style: dotted;  
  border-color: blue;}
```
![[Pasted image 20240404193110.png]]



---
# Márgenes CSS

Las propiedades CSS se utilizan para crear espacio alrededor de los elementos, fuera de las fronteras definidas.`margin`

Con CSS, tienes control total sobre los márgenes. Hay propiedades para establecer el margen de cada lado de un elemento (superior, derecho, inferior e izquierdo).

## Margen - Lados individuales

CSS tiene propiedades para especificar el margen de cada lado de un elemento:

- `margin-top`
- `margin-right`
- `margin-bottom`
- `margin-left`

Todas las propiedades de margen pueden tener los siguientes valores:

- Auto: el navegador calcula el margen
- _length_: especifica un margen en px, pt, cm, etc.
- _%_ - especifica un margen en % de la anchura del elemento que lo contiene
- inherit: especifica que el margen debe heredarse del elemento primario


---
# Padding CSS (Relleno)

Las propiedades CSS se utilizan para generar espacio alrededor el contenido de un elemento, dentro de los bordes definidos.`padding`

Con CSS, tienes control total sobre el relleno. Hay propiedades para establecer el relleno de cada lado de un elemento (superior, derecho, inferior e izquierdo).

## Acolchado - Lados individuales

CSS tiene propiedades para especificar el relleno de cada lado de un elemento:

- `padding-top`
- `padding-right`
- `padding-bottom`
- `padding-left`

Todas las propiedades de relleno pueden tener los siguientes valores:

- _Length_: especifica un relleno en PX, PT, CM, etc.
- _%_ - especifica un relleno en % de la anchura del elemento que lo contiene
- inherit: especifica que el relleno debe heredarse del elemento primario