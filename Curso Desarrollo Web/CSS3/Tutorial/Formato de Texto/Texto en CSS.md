## Color del texto

La propiedad se utiliza para establecer el color del texto. El color se especifica mediante:`color`

- un nombre de color, como "rojo"
- un valor HEX, como "#ff0000"
- un valor RGB - como "rgb(255,0,0)"

Mira [los valores de color CSS](https://www.w3schools.com/cssref/css_colors_legal.asp) para obtener una lista completa de los posibles valores de color.

El color de texto predeterminado para una página se define en el selector de cuerpo.

## Color del texto y color de fondo

En este ejemplo, definimos tanto la propiedad como la propiedad:`background-color``color`

```css
body {  background-color: lightgrey;  
  color: blue;}  
  
h1 {  background-color: black;  
  color: white;}  
  
div {  background-color: blue;  
  color: white;}
```

## Alineación y dirección del texto

En este capítulo aprenderá sobre las siguientes propiedades:

- `text-align`
- `text-align-last`
- `direction`
- `unicode-bidi`
- `vertical-align`
## Text Alignment
La propiedad se utiliza para establecer la alineación horizontal de un texto.`text-align`

Un texto puede estar alineado a la izquierda o a la derecha, centrado o justificado.

En el ejemplo siguiente se muestra el texto alineado al centro y alineado a la izquierda y a la derecha (La alineación a la izquierda es la predeterminada si la dirección del texto es de izquierda a derecha y a la derecha La alineación es predeterminada si la dirección del texto es de derecha a izquierda):
```css
h1 {  text-align: center;}  
  
h2 {  text-align: left;}  
  
h3 {  text-align: right;}
```

Cuando la propiedad se establece en "justify", cada línea es estirado de modo que cada línea tenga el mismo ancho, y los márgenes izquierdo y derecho sean Recto (como en revistas y periódicos):`text-align`

## Text Align Last
La propiedad especifica cómo alinear la última línea de un texto.`text-align-last`

![[Curso Desarrollo Web/CSS3/Tutorial/Formato de Texto/extras/Pasted image 20240404224316.png]]

---

# Decoración de texto CSS

En este capítulo aprenderá sobre las siguientes propiedades:

- `text-decoration-line`
- `text-decoration-color`
- `text-decoration-style`
- `text-decoration-thickness`
- `text-decoration`

## Añadir una línea de decoración al texto

La propiedad se utiliza para agregar Una línea de decoración a texto.`text-decoration-line`

**Propina:** Puede combinar más de un valor, como sobrelínea y subrayado para mostrar líneas tanto por encima como por debajo de un texto.

```css
h1 {  text-decoration-line: overline;}  
  
h2 {  text-decoration-line: line-through;}  
  
h3 {  text-decoration-line: underline;}  
  
p {  text-decoration-line: overline underline;}
```
![[Curso Desarrollo Web/CSS3/Tutorial/Formato de Texto/extras/Pasted image 20240404231440.png]]
>**Nota:** No se recomienda subrayar el texto que no es un enlace, ya que esto a menudo confunde al lector.

## La propiedad abreviada
La propiedad es una taquigrafía Propiedad para:`text-decoration`

- `text-decoration-line` (obligatorio)
- `text-decoration-color` (Opcional)
- `text-decoration-style` (Opcional)
- `text-decoration-thickness` (Opcional)
```css
h1 {  text-decoration: underline;}  
  
h2 {  text-decoration: underline red;}  
  
h3 {  text-decoration: underline red double;}  
  
p {  text-decoration: underline red double 5px;}
```

![[Curso Desarrollo Web/CSS3/Tutorial/Formato de Texto/extras/Pasted image 20240404231409.png]]
##  *Un pequeño consejo*

Todos los enlaces en HTML están subrayados de forma predeterminada. A veces Compruebe que los enlaces se diseñan sin subrayado. El se utiliza para eliminar el subrayado de los enlaces, Así:`text-decoration: none;`

```css
a {  text-decoration: none;}
```


---

## Transformación de texto

La propiedad se utiliza para especificar letras mayúsculas y minúsculas en un texto.`text-transform`

Se puede usar para convertir todo en letras mayúsculas o minúsculas, o Escribe en mayúscula la primera letra de cada palabra:

```css
p.uppercase {  text-transform: uppercase;}  
  
p.lowercase {  text-transform: lowercase;}  
  
p.capitalize {  text-transform: capitalize;}
```

![[Curso Desarrollo Web/CSS3/Tutorial/Formato de Texto/extras/Pasted image 20240404231314.png]]
---

## Espaciado de texto

En este capítulo aprenderá sobre las siguientes propiedades:

- `text-indent`
- `letter-spacing`
- `line-height`
- `word-spacing`
- `white-space`

## Sangría de texto

La propiedad se utiliza para especificar la sangría de la primera línea de un texto:`text-indent`
```css
p {  text-indent: 50px;}
```

![[Curso Desarrollo Web/CSS3/Tutorial/Formato de Texto/extras/Pasted image 20240404225823.png]]
## Espaciado entre letras

La propiedad se utiliza para especificar el espacio entre los caracteres de un texto.`letter-spacing`

En el ejemplo siguiente se muestra cómo aumentar o disminuir el espacio entre caracteres:

```css
h1 {  letter-spacing: 5px;}  
  
h2 {  letter-spacing: -2px;}
```

![[Curso Desarrollo Web/CSS3/Tutorial/Formato de Texto/extras/Pasted image 20240404225840.png]]

## Altura de la línea

La propiedad se utiliza para especificar el espacio entre líneas:`line-height`

```css
p.small {  line-height: 0.8;}  
  
p.big {  line-height: 1.8;}
```
![[Curso Desarrollo Web/CSS3/Tutorial/Formato de Texto/extras/Pasted image 20240404225923.png]]

## Espaciado entre palabras

La propiedad se utiliza para especificar el espacio entre las palabras de un texto.`word-spacing`

En el ejemplo siguiente se muestra cómo aumentar o disminuir el espacio entre palabras:

```css
p.one {  word-spacing: 10px;}  
  
p.two {  word-spacing: -2px;}
```

![[Curso Desarrollo Web/CSS3/Tutorial/Formato de Texto/extras/Pasted image 20240404230043.png]]

---

# Sombra de texto CSS

## Sombra de texto

La propiedad agrega sombra al texto.`text-shadow`

En su uso más simple, solo se especifica la sombra horizontal (2px) y la sombra vertical (2px):

```css
h1 {  text-shadow: 2px 2px 5px red;}
```
![[Curso Desarrollo Web/CSS3/Tutorial/Formato de Texto/extras/Pasted image 20240404230812.png]]
