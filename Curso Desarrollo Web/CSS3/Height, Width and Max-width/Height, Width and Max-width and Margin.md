# Altura, anchura y anchura máxima de CSS

El CSS y las propiedades se utilizan para establecer el altura y anchura de un elemento.`height y width`

La propiedad CSS se utiliza para establecer el ancho máximo de un elemento.`max-width`

## Valores de alto y ancho CSS

Las propiedades y puede tener los siguientes valores:`height``width`

- `auto` - Este es el valor predeterminado. El navegador Calcula la altura y la anchura
- `length` - Define la altura/anchura en px, cm, etc.
- `%` - Define la altura/anchura en porcentaje de El bloque contenedor
- `initial` - Establece la altura/anchura en su Valor predeterminado
- `inherit` - La altura/anchura será heredado de su valor primario

## Ajuste de max-width

La propiedad se utiliza para establecer el ancho máximo de un elemento.`max-width`

Se puede especificar en _valores de longitud_, como px, cm, etc., o en porcentaje (%) de la que contiene, o se establece en none (esto es predeterminado. Significa que no hay un ancho máximo).`max-width`

El problema con lo anterior ocurre cuando la ventana del navegador es más pequeña que el ancho de el elemento (500px). A continuación, el navegador añade una barra de desplazamiento horizontal a la página.`<div>`

En su lugar, en esta situación, mejorará el manejo de las ventanas pequeñas por parte del navegador.`max-width`


## Uso de width, max-width y margin: auto;

Como se mencionó en el capítulo anterior; Un elemento de nivel de bloque siempre ocupa todo el ancho disponible (se extiende hacia la izquierda y hacia la derecha tanto como puede).

Establecer el `width`de un elemento a nivel de bloque evitará que se estire hasta los bordes de su contenedor. A continuación, puede establecer el parámetro márgenes a auto, para centrar horizontalmente el elemento dentro de su contenedor. El ocupará el ancho especificado y el espacio restante se dividirá equitativamente entre los dos márgenes:
![[Pasted image 20240405231000.png]]

>**Nota:** El problema con`<div>`  ocurre cuando la ventana del navegador está más pequeño que el ancho de el elemento. A continuación, el navegador añade una barra de desplazamiento horizontal a la página.


Usar `max-width` en su lugar, en esta situación, mejorará el Manejo de ventanas pequeñas por parte del navegador. Esto es importante a la hora de hacer que un sitio sea utilizable En dispositivos pequeños

```html
<!DOCTYPE html>
<html>
<head>
<style>
div.ex1 {
  width: 500px;
  margin: auto;
  border: 3px solid #73AD21;
}

div.ex2 {
  max-width: 500px;
  margin: auto;
  border: 3px solid #73AD21;
}
</style>
</head>
<body>

<h2>CSS Max-width</h2>

<div class="ex1">This div element has width: 500px;</div>
<br>

<div class="ex2">This div element has max-width: 500px;</div>

<p><strong>Tip:</strong> Drag the browser window to smaller than 500px wide, to see the difference between 
the two divs!</p>

</body>
</html>

```

![[Pasted image 20240405231316.png]]