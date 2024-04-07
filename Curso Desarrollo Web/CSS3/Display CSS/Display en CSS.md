# Diseño CSS - La propiedad display

## La propiedad display
La propiedad `display` se utiliza para especificar cómo se muestra un elemento en una página web.

Cada elemento HTML tiene un valor de visualización predeterminado, dependiendo del tipo de elemento que sea. El valor de visualización predeterminado para la mayoría de los elementos es`block` o `inline`.

La propiedad `display`  se utiliza para cambiar el comportamiento de visualización predeterminado de los elementos HTML. 

## Elementos a nivel de bloque

Un elemento de nivel de bloque SIEMPRE comienza en una nueva línea y ocupa todo el ancho disponible (se extiende hacia la izquierda y hacia la derecha tanto como puede).

![[Pasted image 20240405223015.png]]
Ejemplos de elementos a nivel de bloque:
```html
- <div>
- <h1> --- <h6>
- <p>
- <form>
- <header>
- <footer>
- <section>
```


## Elementos en línea

Un elemento en línea NO comienza en una nueva línea y solo ocupa el ancho necesario.

Se trata de un elemento `<span>` en línea dentro de un párrafo.

Ejemplos de elementos en línea:
```html
- <span>
- <a>
- <img>
```
## La visualización de los valores de propiedad

La propiedad tiene muchos valores:`display`
![[Pasted image 20240405223645.png | 650]]

## Display: none;

`display: none;` se usa comúnmente con JavaScript para ocultar y mostrar elementos sin eliminarlos y volver a crearlos. Echa un vistazo a nuestro último ejemplo en esta página si desea saber cómo se puede lograr esto.

El elemento se utiliza de forma predeterminada.`<script>``display: none;`

![[Pasted image 20240405225931.png]]
![[Pasted image 20240405225944.png]]
## Ocultar un elemento - display:none o visibility:hidden?
La ocultación de un elemento se puede hacer estableciendo la propiedad `display` en `none`. El elemento se ocultará y la página se mostrará como si el elemento no lo estuviera allí:
```css
h1.hidden {  display: none;}
```

`visibility:hidden;` también oculta un elemento.

Sin embargo, el elemento seguirá ocupando el mismo espacio como antes. El elemento estará oculto, pero seguirá afectando al diseño:

```css
h1.hidden {  visibility: hidden;}
```

