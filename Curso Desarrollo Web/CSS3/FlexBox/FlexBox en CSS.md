# Flexbox CSS
## CSS Flexbox Layout Module
Antes del módulo de diseño de Flexbox, había cuatro modos de diseño:

- Block, para secciones de una página web
- Inline, para texto
- Tabla, para datos de tabla bidimensionales
- Positioned, para la posición explícita de un elemento

El Módulo de Diseño de Caja Flexible, facilita el diseño Estructura de diseño flexible y receptiva sin usar **Float** o **Positioning**.

## Ejemplo:
Un diseño flexible debe tener un elemento primario con la propiedad _display_ establecida en _flex_.

Los elementos secundarios directos del contenedor flexible se convierten automáticamente en elementos flexibles.

```css
div.contenedor{

display:flex;

background-color: aqua;

}

div.contenedor > p{

background-color: aquamarine;

margin: 20px auto;

padding: 30px;

}

```
![[Pasted image 20240409205302.png]]

---
# Flex Container

Las propiedades del contenedor flexible son:

- [`flex-direction`](https://www.w3schools.com/css/css3_flexbox_container.asp#flex-direction)
- [`flex-wrap`](https://www.w3schools.com/css/css3_flexbox_container.asp#flex-wrap)
- [`flex-flow`](https://www.w3schools.com/css/css3_flexbox_container.asp#flex-flow)
- [`justify-content`](https://www.w3schools.com/css/css3_flexbox_container.asp#justify-content)
- [`align-items`](https://www.w3schools.com/css/css3_flexbox_container.asp#align-items)
- [`align-content`](https://www.w3schools.com/css/css3_flexbox_container.asp#align-content)

---

# La propiedad flex-direction

La propiedad define en qué dirección se encuentra el contenedor Quiere apilar los elementos flexibles.`flex-direction`

```css
.flex-container {  display: flex;  
  flex-direction: column;}
```

```css
div.contenedor{

display:flex;

background-color: aqua;

flex-direction: column;

}

div.contenedor > p{

background-color: aquamarine;

width: 100px;

height: 50px;

margin: 10px;

line-height: 50px;

text-align: center;

}
```

![[Pasted image 20240409210925.png]]

El valor apila los elementos flexibles verticalmente (pero de abajo hacia arriba):`column-reverse`

```css
div.contenedor{

display:flex;

background-color: aqua;

flex-direction: column-reverse;

}
```
![[Pasted image 20240409211248.png]]

El valor apila los elementos flexibles horizontalmente (de izquierda a derecha):`row`

```css
div.contenedor{

display:flex;

background-color: aqua;

flex-direction: row;

}
```
![[Pasted image 20240409211450.png]]

El valor apila los elementos flexibles horizontalmente (pero de derecha a izquierda):`row-reverse`

```css
div.contenedor{

display:flex;

background-color: aqua;

flex-direction: row-reverse;

}
```

![[Pasted image 20240409211554.png]]

---
## La propiedad flex-wrap

La propiedad especifica si el Los artículos flexibles deben envolverse o no.`flex-wrap`

Los siguientes ejemplos tienen 12 elementos flexibles, para demostrar mejor la propiedad. `flex-wrap`

```css
div.contenedor{

display:flex;

background-color: aqua;

flex-wrap: wrap;

}
``` 

![[Pasted image 20240409212005.png]]

El valor especifica que los elementos flexibles no se ajustarán (este es el valor predeterminado):`nowrap`

![[Pasted image 20240409212147.png]]

El valor especifica que los elementos flexibles se ajustarán Si es necesario, en orden inverso:`wrap-reverse`

```css
div.contenedor{

display:flex;

background-color: aqua;

flex-wrap: wrap-reverse;

}
```

![[Pasted image 20240409212336.png]]


----
## La propiedad flex-flow

La propiedad es una propiedad abreviada para establecer las propiedades y .`flex-flow` `flex-direction``flex-wrap`

```css
.flex-container {  display: flex;  
  flex-flow: row wrap;}
```
![[Pasted image 20240409212655.png]]


---
## La propiedad justify-content

La propiedad se utiliza para Alinee los elementos flexibles:`justify-content`
```css
div.contenedor{

display:flex;

background-color: aqua;

justify-content: center;

}
```

![[Pasted image 20240409212840.png]]

El valor alinea los elementos flexibles al principio del contenedor (este es el valor predeterminado):`flex-start`
```css
div.contenedor{

display:flex;

background-color: aqua;

justify-content: flex-start;

}
```
![[Pasted image 20240409213016.png]]
El valor alinea los elementos flexibles al final del contenedor:`flex-end`

```css
}

div.contenedor{

display:flex;

background-color: aqua;

justify-content: flex-end;

}
```

![[Pasted image 20240409213103.png]]

El valor muestra los elementos flexibles con espacio antes, entre, y después de las líneas:`space-around`
```css
.flex-container {  display: flex;  
  justify-content: space-around;}

```
![[Pasted image 20240409213307.png]]

El valor muestra los elementos flexibles con espacio entre los lineas:`space-between`
```css
.flex-container {  display: flex;  
  justify-content: space-between;}
```

![[Pasted image 20240409213424.png]]

---

## La propiedad align-items

La propiedad se utiliza para alinear Los elementos flexibles.`align-items`

El valor alinea los elementos flexibles en el centro de la contenedor:`center`
```css
div.contenedor{

display:flex;

background-color: aqua;

align-items: center;

height: 300px;

}
```
![[Pasted image 20240409213857.png]]

El valor alinea los elementos flexibles en la parte superior del contenedor:`flex-start`
El valor alinea los elementos flexibles en la parte inferior del contenedor:`flex-end`
```css
.flex-container {  display: flex;  
  height: 200px;  
  align-items: flex-start;}
 
.flex-container {  display: flex;  
  height: 200px;  
  align-items: flex-end;}
```

![[Pasted image 20240409214038.png]]
![[Pasted image 20240409214054.png]]

El valor estira los elementos flexibles para llenar el contenedor (este es el valor predeterminado):`stretch`

```css
div.contenedor{

display:flex;

background-color: aqua;

align-items: stretch;

height: 300px;

}
```
![[Pasted image 20240409215007.png]]
 ---
## La propiedad align-content

El valor muestra las líneas flexibles con espacio antes, entre ellos y después de ellos:`space-around`
El valor muestra las líneas flexibles con el mismo espacio entre ellas:`space-between`

```css
div.contenedor{

display:flex;

background-color: aqua;

height: 600px;

flex-wrap: wrap;

align-content:space-around ;
```
![[Pasted image 20240409220132.png]]
![[Pasted image 20240409220218.png]]

El valor estira las líneas flexibles para ocupar las restantes espacio (este es el valor predeterminado):`stretch`

```css
div.contenedor{

display:flex;

background-color: aqua;

height: 600px;

flex-wrap: wrap;

align-content:stretch ;

overflow: scroll;

}
```

![[Pasted image 20240409220358.png]]

El valor muestra las líneas flexibles en el centro del contenedor:`center`
```css
div.contenedor{

display:flex;

background-color: aqua;

height: 600px;

flex-wrap: wrap;

align-content: center ;

overflow: scroll;

}
```

![[Pasted image 20240409220435.png]]

El valor muestra las líneas flexibles al principio del contenedor:`flex-start`
El valor muestra las líneas flexibles al final del contenedor: `flex-end`

```css
div.contenedor{

display:flex;

background-color: aqua;

height: 600px;

flex-wrap: wrap;

align-content: flex-start ;

overflow: scroll;

}
```
![[Pasted image 20240409220604.png]]
![[Pasted image 20240409220624.png]]


## Centrado perfecto

En el siguiente ejemplo resolveremos un problema de estilo muy común: perfecto Centrado.
```css
div.contenedor{

display:flex;

background-color: aqua;

height: 600px;

justify-content: center;

align-items: center;

}
```

![[Pasted image 20240409220846.png]]