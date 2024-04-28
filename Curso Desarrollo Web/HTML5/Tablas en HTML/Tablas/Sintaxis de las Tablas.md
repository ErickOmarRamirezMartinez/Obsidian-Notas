Para crear una tabla en HTML, utilizas la etiqueta `<table>`. Dentro de esta tabla, puedes definir filas con la etiqueta `<tr>` y luego celdas dentro de esas filas usando `<td>` para celdas de datos o `<th>` para celdas de encabezado. Aquí tienes un ejemplo básico de cómo se vería:

```html
<table>
  <tr>
    <th>Encabezado 1</th>
    <th>Encabezado 2</th>
  </tr>
  <tr>
    <td>Dato 1</td>
    <td>Dato 2</td>
  </tr>
  <tr>
    <td>Dato 3</td>
    <td>Dato 4</td>
  </tr>
</table>

```

También puedes añadir atributos a la etiqueta `<table>` y a las celdas para controlar aspectos como el borde, el espaciado entre celdas, y la alineación del texto. Por ejemplo, para añadir un borde a toda la tabla, podrías hacerlo así:
```html
<table border="1">
  <!-- Contenido de la tabla aquí -->
</table>

```

![[Pasted image 20240328114018.png]]

---
# Responsive
## Tabla responsiva

Una tabla adaptable mostrará una barra de desplazamiento horizontal si la pantalla es demasiado small para mostrar el contenido completo:
![[Pasted image 20240405221103.png]]

```html
<div style="overflow-x:auto;">  
  
<table>  
... table content ...  
</table>  
  
</div>
```
