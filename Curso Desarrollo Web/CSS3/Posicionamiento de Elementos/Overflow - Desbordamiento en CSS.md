## Desbordamiento de CSS

La propiedad `overflow` especifica si se va a recortar el contenido o para agregar barras de desplazamiento cuando el contenido de un elemento es demasiado grande para caber en el área.
La propiedad `overflow` tiene los siguientes valores:

- `visible` -Predeterminado. El desbordamiento no se recorta. El contenido se representa fuera del cuadro del elemento
- `hidden` - El desbordamiento se recorta y el resto del contenido será invisible
- `scroll` - El desbordamiento se recorta y se agrega una barra de desplazamiento para ver el resto del contenido
- `auto` - Similar a , pero agrega barras de desplazamiento solo cuando es necesario`scroll`

>**Nota:** La propiedad solo funciona para elementos de bloque con una altura especificada.`overflow`

>**Nota:** En OS X Lion (en Mac), las barras de desplazamiento están ocultas de forma predeterminada y solo se muestran cuando se usan (aunque se haya establecido "overflow:scroll").


---
## overflow: visible

De forma predeterminada, el desbordamiento es `visible`, lo que significa que no está recortado y renderiza fuera de la caja del elemento:
```css
div.container3{

border: 5px dashed black;

background-color: aquamarine;

width: 50%;

height: 150px;

margin: auto;

padding: 20px;

  

overflow: visible;

}

```
![[Pasted image 20240406231128.png]]

## overflow: hidden
Con el valor`hidden`, el desbordamiento se recorta y el resto del contenido se oculta:
```css
div.container3{

border: 5px dashed black;

background-color: aquamarine;

width: 50%;

height: 150px;

margin: auto;

padding: 20px;

  

overflow: hidden;

}
```

![[Pasted image 20240406231255.png]]


## overflow: scroll

Al establecer el valor en`scroll` , se recorta el desbordamiento y se agrega una barra de desplazamiento para desplazarse dentro del cuadro. Tenga en cuenta que esto agregará una barra de desplazamiento tanto horizontal como verticalmente (incluso si no la necesita):

![[Pasted image 20240406231404.png]]


## overflow: auto

El valor `auto` es similar a `scroll` , Pero agrega barras de desplazamiento solo cuando es necesario:
![[Pasted image 20240406231522.png]]