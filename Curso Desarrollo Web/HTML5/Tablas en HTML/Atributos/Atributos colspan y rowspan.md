![[Pasted image 20240328115449.png]]

## **Colspan**
El atributo `colspan` se utiliza para indicar cuantas columnas debe ocupar una celda de una tabla 
Se puede agregar a la celda `<td>` o `<th>` que deseamos expandir horizontalmente
La celda se fusionara con las celdas adyacentes hacia la derecha. Su valor es un numero entero que representa cuantas columnas debe abarcar

## **Rowspan**
El atributo `rowspan` se utiliza para indicar cuantas filas debe ocupar una celda en una tabla. 
Se puede agregar a la celda `<td>` o `<th>` que deseamos expandir verticalmente
La celda se funcionara con la celda adyacente hacia abajo. Su valor es un numero entero que representa cuantas filas debe abarcar


[Table Tag Generetor](https://tabletag.net/)

---

## Ejercicio Simple del Uso de Tablas
![[ Pasted image 20240328123640.png ]]]
```html
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Document</title>

<link rel="stylesheet" href="estilos.css">

</head>

<body>

<h1>Ejercicio de Calculadora</h1>

  

<table>

<tr>

<th colspan="4" style="border: solid aqua; background-color: darkseagreen;">Pantalla</th>

</tr>

<tr>

<td>7</td>

<td>8</td>

<td>9</td>

<td>+</td>

</tr>

<tr>

<td>4</td>

<td>5</td>

<td>6</td>

<td>-</td>

</tr>

<tr>

<td>1</td>

<td>2</td>

<td>3</td>

<td>*</td>

</tr>

<tr>

<td>0</td>

<td>.</td>

<td>C</td>

<td>/</td>

</tr>

<tr>

<td colspan="4" style="text-align: center;">=</td>

</tr>

</table>

</body>

</html>
```

```css
table{

border: solid red;

padding: 5px;

border-radius: 10px;

}

td{

border: solid;

border-color: aqua;

font-weight: bold;

padding: 5px;

padding-bottom: 10px;

}
```