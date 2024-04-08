## Centrar elementos de alineación

Para centrar horizontalmente un elemento de bloque (como `<div>`), use `margin: auto;`

Establecer el ancho del elemento evitará que se extienda hacia el bordes de su contenedor.

A continuación, el elemento ocupará el ancho especificado y el espacio restante se dividirá a partes iguales entre los dos márgenes:
![[Pasted image 20240407211120.png]]

## Centrar el texto de alineación

Para centrar el texto dentro de un elemento, use `text-align: center;`
![[Pasted image 20240407211146.png]]

## Centrar una imagen

Para centrar una imagen, establezca los márgenes izquierdo en `auto` y derecho y conviértala en un elemento:`block`
![[Pasted image 20240407211211.png]]

## Alinear a la izquierda y a la derecha - Usar la posición

Un método para alinear elementos es utilizar:`position: absolute;`

![[Pasted image 20240407211319.png]]

## Alinear a la izquierda y a la derecha: uso de float

Otro método para alinear elementos es usar la propiedad:`float`
![[Pasted image 20240407211416.png]]

## El truco de clearfix

>**Nota:** Si un elemento es más alto que el elemento que lo contiene y flota, se desbordará fuera de su contenedor. Puede usar el "truco de clearfix" para solucionar esto (vea el ejemplo a continuación).

![[Pasted image 20240407211528.png]]

## Centrar verticalmente - Uso de Flexbox

También puedes usar flexbox para centrar las cosas. Solo tenga en cuenta que flexbox no es compatible con IE10 y versiones anteriores:
![[Pasted image 20240407211710.png]]

