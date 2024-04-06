## Relleno de la tabla

Para controlar el espacio entre el borde y el contenido de una tabla, utilice la propiedad en `<td> y <th>` elementos:`padding`
![[Pasted image 20240405220600.png]]

```css
th, td {  padding: 15px;  
  text-align: left;}
```

## Divisores horizontales

![[Pasted image 20240405220544.png]]
```css
th, td {  border-bottom: 1px solid #ddd;}
```

## Tabla flotante

Utilice el selector de `<tr>` para resaltar las filas de la tabla con el ratón sobre:`:hover`

![[Pasted image 20240405220528.png]]

```css
tr:hover {background-color: coral;}
```


## Mesas rayadas

![[Pasted image 20240405220812.png]]
En el caso de las tablas con rayas de cebra, utilice el selector y agregue a todas las filas pares (o impares) de la tabla:`nth-child()``background-color`

## Color de la tabla

En el ejemplo siguiente se especifica el color de fondo y el color del texto de <º > elementos:
![[Pasted image 20240405220835.png]]

```css
th {  background-color: #04AA6D;  
  color: white;}
```

