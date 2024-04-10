# CSS Flex Items

## Elementos secundarios (elementos)

Los elementos secundarios directos de un contenedor flexible se convierten automáticamente en elementos flexibles (flexibles).

Las propiedades del elemento flexible son:

- [`order`](https://www.w3schools.com/css/css3_flexbox_items.asp#order)
  La propiedad _order_ puede cambiar el orden de los elementos flexibles:
  ```css
  <div class="flex-container">  
  <div style="order: 3">1</div>  
  <div style="order: 2">2</div>  
  <div style="order: 4">3</div>  
  <div style="order: 1">4</div>  
</div>
```
![[Pasted image 20240409221816.png]]
- [`flex-grow`](https://www.w3schools.com/css/css3_flexbox_items.asp#flex-grow)
  La propiedad especifica cuánto crecerá un elemento flexible en relación con el resto de los elementos flexibles.`flex-grow`
  ```css
  <div class="flex-container">  
  <div style="flex-grow: 1">1</div>  
  <div style="flex-grow: 1">2</div>  
  <div style="flex-grow: 8">3</div>  
</div>
  ```
  ![[Pasted image 20240409221921.png]]
- [`flex-shrink`](https://www.w3schools.com/css/css3_flexbox_items.asp#flex-shrink)
  La propiedad especifica cuánto se reducirá un elemento flexible en relación con el resto de los elementos flexibles.`flex-shrink`
  ```css
  <div class="flex-container">  
  <div>1</div>  
  <div>2</div>  
  <div style="flex-shrink: 0">3</div>  
  <div>4</div>  
  <div>5</div>  
  <div>6</div>  
  <div>7</div>  
  <div>8</div>  
  <div>9</div>  
  <div>10</div>  
</div>
```
![[Pasted image 20240409222014.png]]
- [`flex-basis`](https://www.w3schools.com/css/css3_flexbox_items.asp#flex-basis)
  La propiedad especifica la longitud inicial de un elemento flexible.`flex-basis`
  ```css
  <div class="flex-container">  
  <div>1</div>  
  <div>2</div>  
  <div style="flex-basis: 200px">3</div>  
  <div>4</div>  
</div>
  ```
  ![[Pasted image 20240409222109.png]]
- [`flex`](https://www.w3schools.com/css/css3_flexbox_items.asp#flex)
  La propiedad es una propiedad abreviada de las propiedades , , y .`flex` `flex-grow``flex-shrink``flex-basis`
  ```css
 <div class="flex-container">  
  <div>1</div>  
  <div>2</div>  
  <div style="flex: 0 0 200px">3</div>  
  <div>4</div>  
</div>
  ```

- [`align-self`](https://www.w3schools.com/css/css3_flexbox_items.asp#align-self)
  La propiedad especifica el parámetro alineación del elemento seleccionado dentro del contenedor flexible.`align-self`
  La propiedad anula la alineación predeterminada establecida por el propiedad del contenedor.`align-self` `align-items`
  ```css
  <div class="flex-container">  
  <div>1</div>  
  <div>2</div>  
  <div style="align-self: center">3</div>  
  <div>4</div>  
  </div>
```

![[Pasted image 20240409222151.png]]