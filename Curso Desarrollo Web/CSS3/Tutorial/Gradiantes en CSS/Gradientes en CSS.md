# Degradados CSS
![[Pasted image 20240408220007.png]]
Los degradados CSS le permiten mostrar transiciones suaves entre dos o más colores especificados.

CSS define tres tipos de degradados:

- **Degradados lineales (va hacia abajo/arriba/izquierda/derecha/diagonalmente)**
- **Degradados radiales (definidos por su centro)**
- **Degradados cónicos (girados alrededor de un punto central)**

---
## Gradientes lineales CSS

Para crear un degradado lineal debe definir Al menos dos paradas de color. Las paradas de color son los colores que desea representar transiciones suaves entre. También puede establecer un punto de partida y una dirección (o un ángulo) a lo largo de con el efecto degradado.

### Sintaxis

`background-image: linear-gradient(_direction_, _color-stop1_, _color-stop2, ..._);`

**Dirección: de arriba a abajo (este es el valor predeterminado)**

En el ejemplo siguiente se muestra un degradado lineal que comienza en la parte superior. Comienza en rojo, pasando a amarillo:

```css
#grad {  background-image: linear-gradient(red, yellow);}
```

![[Pasted image 20240408223554.png]]

**Dirección: de izquierda a derecha**

En el ejemplo siguiente se muestra un degradado lineal que comienza desde la izquierda. Comienza en rojo, pasando a amarillo:

```css
body{

background: linear-gradient(to right, red, blue);

}
```

![[Pasted image 20240408223856.png]]

**Dirección - Diagonal**
Puede crear un degradado en diagonal especificando las posiciones inicial horizontal y vertical.

```css
body{

background: linear-gradient(to top, red, blue);

}
```
![[Pasted image 20240408224106.png]]

---

## Uso de ángulos

Si desea tener más control sobre la dirección del degradado, Puede definir un ángulo, en lugar de las direcciones predefinidas (hacia abajo, hacia arriba, a la derecha, a la izquierda, a abajo a la derecha, etc.). Un valor de 0 grados equivale a "Para arriba". Un valor de 90 grados equivale a "a la derecha". Un valor de 180 grados equivale a "tocar fondo".

```css
#grad1 {

height: 100px;

background-color: red; /* For browsers that do not support gradients */

background-image: linear-gradient(0deg, red, yellow);

}

#grad2 {

height: 100px;

background-color: red; /* For browsers that do not support gradients */

background-image: linear-gradient(90deg, red, yellow);

}

#grad3 {

height: 100px;

background-color: red; /* For browsers that do not support gradients */

background-image: linear-gradient(180deg, red, yellow);

}

#grad4 {

height: 100px;

background-color: red; /* For browsers that do not support gradients */

background-image: linear-gradient(-90deg, red, yellow);

}
```

---

## Gradientes radiales CSS

Un gradiente radial se define por su centro.

Para crear un degradado radial, también debe definir al menos dos paradas de color.

### Sintaxis

background-image: radial-gradient(_shape size_ at _position, start-color, ..., last-color_);

De forma predeterminada, la forma es la elipse, el tamaño es la esquina más lejana y la posición es el centro.

![[Pasted image 20240408224952.png]]
