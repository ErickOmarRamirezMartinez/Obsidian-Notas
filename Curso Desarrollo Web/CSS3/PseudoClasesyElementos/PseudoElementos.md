## ¿Qué son los pseudoelementos?

Un pseudoelemento CSS se utiliza para aplicar estilo a partes específicas de un elemento.

Por ejemplo, se puede utilizar para:

- Aplicar estilo a la primera letra, o línea, de un elemento
- Insertar contenido antes o después del contenido de un elemento
## Sintaxis

La sintaxis de los pseudoelementos:

```css
selector::pseudo-element {  property: value;}
```


```css
p::first-letter {

color: #ff0000;

font-size: xx-large;

}

p::first-line {

color: #0000ff;

font-variant: small-caps;

}

::selection {

color: red;

background: yellow;

}
```

![[Pasted image 20240407231636.png]]

## All CSS Pseudo Elements
- **::after**: Inserta contenido después de cada elemento `<p>`.
- **::before**: Inserta contenido antes de cada elemento `<p>`.
- **::first-letter**: Selecciona la primera letra de cada elemento `<p>`.
- **::first-line**: Selecciona la primera línea de cada elemento `<p>`.
- **::marker**: Selecciona los marcadores de los elementos de lista.
- **::selection**: Selecciona la porción de un elemento que es seleccionada por un usuario.