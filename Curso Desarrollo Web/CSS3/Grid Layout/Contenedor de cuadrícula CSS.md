## Contenedor de cuadrícula

Para hacer que un elemento HTML se comporte como un contenedor de cuadrícula, debe establecer la propiedad en o .`display` `grid``inline-grid`

Los contenedores de cuadrícula constan de elementos de cuadrícula, colocados dentro de columnas y filas.

## La propiedad grid-template-columns

La propiedad define el número de columnas en el diseño de cuadrícula y puede definir el ancho de cada columna.`grid-template-columns`

El valor es una lista separada por espacios, donde cada valor define el ancho de la columna respectiva.

Si desea que el diseño de cuadrícula contenga 4 columnas, especifique el ancho de las 4 columnas o "auto" si todas las columnas deben tener el mismo ancho.

```css
.grid-container {  display: grid;  
  grid-template-columns: auto auto auto auto;}
```

---
# Tamaño de Filas y Columnas
La propiedad también se puede utilizar para especificar el tamaño (ancho) de las columnas.`grid-template-columns`

```css
.grid-container {
  display: grid;
  grid-template-columns: 80px 200px auto 30px;
  gap: 10px;
  background-color: #2196F3;
  padding: 10px;
}

```
![[Pasted image 20240410211046.png]]

La propiedad define la altura de cada fila.`grid-template-rows`
```css
.grid-container {  display: grid;  
  grid-template-rows: 80px 200px;}
```
![[Pasted image 20240410211136.png]]

---

## La propiedad Justify-Content

Se pueden utiilizar todas las opciones que ofrece la propiedad `justify-content` en los Grid que creamos
Puedes ir a verlo en mi notas 

[[FlexBox en CSS#La propiedad justify-content]]


---
## La propiedad Align-content

Se pueden utiilizar todas las opciones que ofrece la propiedad `aling-content` en los Grid que creamos
Puedes ir a verlo en mi notas 

[[FlexBox en CSS#La propiedad align-content]]
