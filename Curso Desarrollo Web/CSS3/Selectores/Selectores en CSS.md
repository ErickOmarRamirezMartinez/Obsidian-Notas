> Un combinador es algo que explica la relación entre los selectores.

Un selector CSS puede contener más de un selector simple. Entre lo simple selectores, podemos incluir un combinador.

Hay cuatro combinadores diferentes en CSS:

- Selector de descendientes (espacio)
- Selector de niños (>)
- Selector de hermanos adyacentes (+)
- Selector general de hermanos (~)

## Selector de descendientes

El selector de descendientes coincide con todos los elementos que son descendientes de un elemento.

En el ejemplo siguiente se seleccionan todos los elementos `<p>` dentro de los elementos `<div>`:
![[Pasted image 20240407214047.png]]

```css
div p {  background-color: yellow;}
```

![[Pasted image 20240407223703.png]]
## Selector de niños(child) (>)

El selector secundario selecciona todos los elementos que son los elementos secundarios de un elemento especificado.

En el ejemplo siguiente se seleccionan todos los elementos `<p>` que son Hijos de una `<div>` elemento:



```html 
<div class="contenedor hijo">

Selectores Hijos (child)

<p>Primer renglon</p>

<p>Segundo renglon</p>

<section>

<p>Tercer renglon</p>

<p>Cuarto renglon</p>

</section>

<p>Quinto renglon</p>

</div>
```

```css
div.contenedor.hijo > p{

background-color: #fdffb6;

}
```

![[Pasted image 20240407223641.png]]
## Selector de hermanos adyacentes (+)

El selector del mismo nivel adyacente se utiliza para seleccionar un elemento que está directamente después de otro elemento específico.

Los elementos del mismo nivel deben tener el mismo elemento primario y "adyacente" significa "inmediatamente después".
```css
div.contenedor.hermanoM + p{

background-color: #fdffb6;

}
```

![[Pasted image 20240407221137.png]]
## Selector general de hermanos (~)

El selector general de elementos del mismo nivel selecciona todos los elementos que son los siguientes del mismo nivel de un elemento especificado.
```css
div.contenedor.hermanoM ~ p{

background-color: #fdffb6;

}
```

![[Pasted image 20240407221401.png]]

