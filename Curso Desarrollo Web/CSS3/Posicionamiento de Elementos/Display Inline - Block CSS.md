## El Display: inline-block 

En comparación con `display: inline`, el principal diferencia `display: inline-block` es que permite para establecer una anchura y una altura en el elemento.

Además con `display: inline-block` , Se respetan los márgenes/rellenos superior e inferior, pero con `display: inline`  no.

En comparación con `display: block` , el principal diferencia `display: inline-block` es que no no agregue un salto de línea después del elemento, por lo que el elemento puede colocarse junto a otros Elementos.

```html
<h1>Horizontal Navigation Links</h1>

<p>By default, list items are displayed vertically. In this example we use display: inline-block to display them horizontally (side by side).</p>

<p>Note: If you resize the browser window, the links will automatically break when it becomes too crowded.</p>

  

<ul class="nav">

<li><a href="#home">Home</a></li>

<li><a href="#about">About Us</a></li>

<li><a href="#clients">Our Clients</a></li>

<li><a href="#contact">Contact Us</a></li>

</ul>
```

![[Pasted image 20240407204931.png]]

```css
.nav {

background-color: yellow;

list-style-type: none;

text-align: center;

margin: 0;

padding: 0;

}

.nav li {

display: inline-block;

font-size: 20px;

padding: 20px;

border: 1px solid black;

}
```