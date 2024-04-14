# CSS Fonts

## La selección de la fuente es importante

Elegir la fuente correcta tiene un gran impacto en la forma en que los lectores experimentan un sitio web.

La fuente correcta puede crear una identidad fuerte para tu marca.

Es importante usar una fuente que sea fácil de leer. La fuente agrega valor a su texto. También es importante elegir el color y el tamaño del texto correctos para la fuente.

## Familias de fuentes genéricas

En CSS hay cinco familias de fuentes genéricas:
1. **Serif** tienen un pequeño trazo en los bordes de cada letra. Crean una sensación de formalidad y elegancia.
2. **Sans-serif** tienen líneas limpias (sin trazos pequeños adjuntos). Crean un aspecto moderno y minimalista.
3. **Monospace** aquí todas las letras tienen el mismo ancho fijo. Crean un aspecto mecánico.
4. **Cursive** imitan la escritura humana.
5. **Fantasy** son fuentes decorativas/lúdicas.

## Diferencia entre fuentes serif y sans-serif

![Serif vs. Sans-serif](https://www.w3schools.com/css/serif.gif)

>**Nota:** En las pantallas de las computadoras, las fuentes sans-serif se consideran más fáciles de leer que las fuentes serif.

## Algunos ejemplos de fuentes

|Generic Font Family|Examples of Font Names|
|---|---|
|Serif|Times New Roman  <br>Georgia  <br>Garamond|
|Sans-serif|Arial  <br>Verdana  <br>Helvetica|
|Monospace|Courier New  <br>Lucida Console  <br>Monaco|
|Cursive|Brush Script MT  <br>Lucida Handwriting|
|Fantasy|Copperplate  <br>Papyrus|

## La propiedad CSS font-family

En CSS, usamos la propiedad para especificar la fuente de un texto.`font-family`

**Nota**: Si el nombre de la fuente es más de una palabra, debe estar entre comillas, como: "Times New Roman".

```css
.p1 {  font-family: "Times New Roman", Times, serif;}  
  
.p2 {  font-family: Arial, Helvetica, sans-serif;}  
  
.p3 {  font-family: "Lucida Console", "Courier New", monospace;}
```

---

## ¿Qué son las fuentes seguras para la web?

Las fuentes seguras para la Web son fuentes que se instalan universalmente en todos los navegadores y dispositivos.
## Fuentes de reserva

Sin embargo, no existen fuentes 100% completamente seguras para la web. Siempre hay un Posibilidad de que no se encuentre una fuente o no esté instalada correctamente.

Por lo tanto, es muy importante utilizar siempre fuentes alternativas.

Esto significa que debe agregar una lista de "fuentes de copia de seguridad" similares en la propiedad. Si el La primera fuente no funciona, el navegador probará la siguiente, y la siguiente, y así sucesivamente. Termine siempre la lista con un nombre genérico de familia de fuentes.`font-family`

Aquí, hay tres tipos de fuentes: Tahoma, Verdana y sans-serif. La segunda y tercera fuente son copias de seguridad, en caso de que no se encuentre la primera.

```css
p {  
font-family: Tahoma, Verdana, sans-serif;  
}
```

## Las mejores fuentes seguras para la web para HTML y CSS

La siguiente lista son las mejores fuentes seguras para la web para HTML y CSS:

- Arial (sans-serif)
- Verdana (sans-serif)
- Tahoma (sans-serif)
- Trebuchet MS (sans-serif)
- Times New Roman (serif)
- Georgia (serif)
- Garamond (serif)
- Courier New (monoespaciado)
- Brush Script MT (cursiva)

---

# Font Style
## Estilo de fuente

La propiedad se usa principalmente para especificar texto en cursiva.`font-style`

Esta propiedad tiene tres valores:
- normal: el texto se muestra normalmente
- italic (cursiva) - El texto se muestra en cursiva
- oblique(oblicuo) - El texto está "inclinado" (oblicuo es muy similar a la cursiva, pero menos compatible)
```css
p.normal {  font-style: normal;}  
  
p.italic {  font-style: italic;}  
  
p.oblique {  font-style: oblique;}
```

## Font Weight

La propiedad especifica el grosor de una fuente:`font-weight`
```css
p.normal {  font-weight: normal;}  
  
p.thick {  font-weight: bold;}
```
![[Curso Desarrollo Web/CSS3/Tutorial/Fuentes en CSS 1/extras/Pasted image 20240405204449.png]]

---

# CSS Font Size

## Tamaño de fuente

La propiedad establece el tamaño del texto.`font-size`.
Ser capaz de gestionar el tamaño del texto es importante en el diseño web. Sin embargo, usted no debe usar ajustes de tamaño de fuente para hacer que los párrafos parezcan encabezados, o Los encabezados parecen párrafos.

Utilice siempre las etiquetas HTML adecuadas, como `<h1> - <h6>` para los encabezados y `<p>` para Párrafos.

El valor font-size puede ser un tamaño absoluto o relativo.

Tamaño absoluto:

- Establece el texto en un tamaño especificado
- No permite al usuario cambiar el tamaño del texto en todos los navegadores (malo por razones de accesibilidad)
- El tamaño absoluto es útil cuando se conoce el tamaño físico de la salida

Tamaño relativo:

- Establece el tamaño relativo a los elementos circundantes
- Permite al usuario cambiar el tamaño del texto en los navegadores


> **Nota:** Si no especifica un tamaño de fuente, el tamaño predeterminado para el texto normal, como los párrafos, es de 16 px (16 px = 1em).


## Establecer el tamaño de la fuente con píxeles

Establecer el tamaño del texto con píxeles le da control total sobre el tamaño del texto:

```css
h1 {  font-size: 40px;}  
  
h2 {  font-size: 30px;}  
  
p {  font-size: 14px;}
```

## Tamaño de fuente responsivo

El tamaño del texto se puede establecer con una unidad, lo que significa el "ancho de la ventana gráfica".`vw`

De esa manera, el tamaño del texto seguirá el tamaño de la ventana del navegador:

```css
<h1 style="font-size:10vw;">Responsive Text</h1>

<p style="font-size:5vw;">Resize the browser window to see how the text size scales.</p>

<p style="font-size:5vw;">Use the "vw" unit when sizing the text. 10vw will set the size to 10% of the viewport width.</p>

<p>Viewport is the browser window size. 1vw = 1% of viewport width. If the viewport is 50cm wide, 1vw is 0.5cm.</p>
```

![[Curso Desarrollo Web/CSS3/Tutorial/Fuentes en CSS 1/extras/Pasted image 20240405205955.png]]

---

## Fuentes de Google

Si no desea utilizar ninguna de las fuentes estándar en HTML, puede utilizar Google Fonts.

Las fuentes de Google son de uso gratuito y tienen más de 1000 fuentes para elegir.

## Cómo usar Google Fonts

Sólo tienes que añadir un enlace especial a la hoja de estilo en la sección `<head>` y luego consultar la fuente en el CSS.

```css
<head>  
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sofia">
<style>  
body {  font-family: "Sofia", sans-serif;}  
</style>  
</head>
```
![[Curso Desarrollo Web/CSS3/Tutorial/Fuentes en CSS 1/extras/Pasted image 20240405210154.png]]

---

## La propiedad de fuente CSS

Para acortar el código, también es posible especificar todas las propiedades de fuente individuales en una propiedad.

La propiedad es una propiedad abreviada para:`font`

- `font-style`
- `font-variant`
- `font-weight`
- `font-size/line-height`
- `font-family`

**Nota:** Los valores y son obligatorios. Si falta uno de los otros valores, se utiliza su valor predeterminado.`font-size``font-family`

```css
p.a {  font: 20px Arial, sans-serif;}  
  
p.b {  font: italic small-caps bold 12px/30px Georgia, serif;}
```