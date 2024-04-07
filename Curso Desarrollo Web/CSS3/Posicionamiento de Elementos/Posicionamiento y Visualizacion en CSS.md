# Como centrar elementos tipo DIV con CSS
`margin: 0 auto;`

Podemos centrar un elemento div con margin auto 

> Siempre hay que tener cuidado con el tamaño de nuestro anchura (width)

Para ello siempre podemos utilizar el `width: 50%;`
O tambien  `max-width: 340px;`

Ejemplo:

* Con `width: 50%;`
  ![[Pasted image 20240406195826.png]]
* Con `max-width: 340px;`
  ![[Pasted image 20240406195903.png]]
---

# Posición - propiedad Position

La  propiedad especifica `position` es el tipo de método de posicionamiento utilizado para un elemento (static, relative, fixed, absolute or sticky).
## La posición Propiedad

La propiedad especifica `position` el tipo de método de posicionamiento utilizado para un elemento.

Hay cinco valores de posición diferentes:
- `static`
- `relative`
- `fixed`
- `absolute`
- `sticky`

## position: static;

==Los elementos posicionados estáticamente no se ven afectados por las propiedades top, bottom, left, and right.==
 >Los elementos HTML se colocan estáticos de forma predeterminada.

Como se puede ver en el codigo, aun aplicando top, y left, no es afectado

```css
h1{

text-align: center;

color: crimson;

}

div{

max-width: 340px;

  

top: 100px;

left: 50px;

border: 3px solid firebrick;

margin: 0 auto;

  

}
```

![[Pasted image 20240406201812.png]]

## posición: relative;

Un elemento con `position: relative;` se coloca en relación con su posición normal.

Si se establecen las propiedades superior, derecha, inferior e izquierda de un elemento con una posición relativa, se producirá para ser ajustado lejos de su posición normal. El resto del contenido no se ajustará para que quepa en ningún hueco dejado por el elemento.
 ```css
 h1{

text-align: center;

color: crimson;

}

div{

position: relative;

max-width: 340px;

  

top: 50px;

left: 50px;

  

border: 3px solid firebrick;

margin: 0 auto;

  

}
```
![[Pasted image 20240406202944.png]]

## position: fixed;

Un elemento con `position: fixed;` se coloca en relación con la ventana gráfica, lo que significa que siempre permanece en el mismo lugar incluso si se desplaza la página. La parte superior, Las propiedades right, bottom e left se utilizan para colocar el elemento.

>Un elemento fijo no deja un hueco en la página donde normalmente se habría ubicado.

![[Pasted image 20240406204044.png]]

> Si aumentamos el padding-bottom de un elemento
> Podemos notar que el elementos position:fixed estara fijo en nuestra pantalla siempre que bajemos y usemos scroll

## position: absolute;

Un elemento con `position: absolute;` se coloca en relación con el antecesor posicionado más cercano (en lugar de colocarse en relación con la ventana gráfica, como fijo).
Sin embargo; Si un elemento posicionado en absoluto no tiene antecesores posicionados, Utiliza el cuerpo del documento y se mueve junto con el desplazamiento de la página.

>**Nota:** Los elementos posicionados en posición absoluta se eliminan del flujo normal y pueden superponerse elementos.

```css
div.absolute{

position: absolute;

top: 0;

right: 0;

border: 3px solid firebrick;

}

div.relative{

position: relative;

height: 100px;

width: 400px;

margin: 0 auto;

border: 3px solid firebrick;

}
```

```html
<h1>Posicionamiento</h1>

<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quia repellat voluptates optio excepturi distinctio voluptate, consequuntur quisquam temporibus voluptatum maxime aliquam possimus omnis laborum nisi inventore dicta dignissimos magnam dolores. </p>

<div class="relative">Elemento tipo Relative

<div class="absolute">Elemento tipo Absolute</div></div>

<p>Sit mollit sint duis minim laborum sunt reprehenderit nostrud non occaecat.</p>

<p style="padding-bottom: 2000px;">Nostrud dolore tempor ut fugiat aute ut commodo.</p>
```

![[Pasted image 20240406211301.png]]

## position: sticky;
Un elemento con `position: sticky;` se coloca en función de la posición de desplazamiento del usuario.

Un elemento adhesivo alterna entre`relative` y `fixed` , dependiendo de la posición de desplazamiento. Se coloca en relación hasta que se alcanza una posición de desplazamiento determinada en la ventana gráfica, luego se "pega" en su lugar (como position:fixed).

>**Nota:** Internet Explorer no admite el posicionamiento permanente. Safari requiere un -webkit- (vea el ejemplo a continuación). También debe especificar al menos uno de los , o para Posicionamiento pegajoso para trabajar.`top``right``bottom``left`

En este ejemplo, el elemento adhesivo se adhiere a la parte superior de la página `(top: 0)`, cuando se alcanza su posición de desplazamiento.

```css
div.sticky{

position: sticky;

top: 0;

border: 3px solid firebrick;

}
```

![[Pasted image 20240406213022.png]]

