La propiedad CSS `float` especifica cómo debe flotar un elemento.
La propiedad CSS `clear`  especifica qué elementos pueden flotar junto al elemento borrado y en qué lado.

## La propiedad float

La propiedad `float` se utiliza para Posicionamiento y formato del contenido, por ejemplo, dejar que una imagen flote a la izquierda del texto en un contenedor.

El `float` puede tener uno de los siguientes valores:

- `left` - El elemento flota a la izquierda de su contenedor
- `right` - El elemento flota a la derecha de su contenedor
- `none` - El elemento no flota (se mostrará justo donde aparece en el texto). Este es el valor predeterminado
- `inherit` - El elemento hereda el valor float de su padre

En su uso más simple, la propiedad se puede usar para ajustar texto alrededor de imágenes.`float`

## Example - float: right;
En el ejemplo siguiente se especifica que una imagen debe flotar a la **derecha** de un texto:
![[Pasted image 20240406235257.png]]

```css
img {  float: right;}
```

## Example - float: left;
En el ejemplo siguiente se especifica que una imagen debe flotar a la **izquierda** en un texto:

![[Pasted image 20240406235407.png]]


---

## Clear - La propiedad clara

Cuando usamos la propiedad `float`, y queremos El siguiente elemento a continuación (no a la derecha ni a la izquierda), tendremos que usar la propiedad `clear`.

La propiedad `clear`especifica lo que debería suceder con el elemento que está al lado de un elemento flotante.
El `clear` puede tener uno de los siguientes valores:

- `none` - El elemento no se empuja hacia abajo elementos flotantes a la izquierda o a la derecha. Este es el valor predeterminado
- `left` - El elemento se empuja hacia abajo a la izquierda Elementos flotantes
- `right` - El elemento se empuja hacia abajo Elementos flotantes a la derecha
- `both` - El elemento se empuja debajo de ambos Elementos flotantes izquierdo y derecho
- `inherit` - El elemento hereda el valor clear de su padre

```css
div.container4{

width: 30%;

height: 100px;

overflow: auto;

}

div.container4.flotado{

float: left;

}

div.container4.flotado.cont1{

border: 2px dashed green;

}

div.container4.cont2{

border: 2px dashed blue;

float: right;

}

div.container4.cont3{

border: 2px dashed yellow;

clear: both;

margin: 0 auto;

}
```
![[Pasted image 20240406235821.png]]
