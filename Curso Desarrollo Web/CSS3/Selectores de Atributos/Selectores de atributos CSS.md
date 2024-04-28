## Aplicar estilo a elementos HTML con atributos específicos

Es posible aplicar estilo a elementos HTML que tienen atributos o valores de atributo específicos.

---
## Selector [attribute] 
El selector se utiliza para seleccionar elementos con un atributo.`[attribute]`

En el ejemplo siguiente se seleccionan todos los elementos `<a>` con un atributo de destino:

```html
<a href="https://www.w3schools.com">w3schools.com</a>
<a href="http://www.disney.com" target="_blank">disney.com</a>
<a href="http://www.wikipedia.org" target="_top">wikipedia.org</a>

```

```css
a[target] {
  background-color: yellow;
}
```
![[Pasted image 20240411212256.png]]

---
# Selector [attribute = "value" ] 

El selector se utiliza para seleccionar elementos con un atributo y valor.`[attribute="value"]`

En el ejemplo siguiente se seleccionan todos los elementos `<a>` con un atributo target="_blank":

```html
<a href="https://www.w3schools.com">w3schools.com</a>
<a href="http://www.disney.com" target="_blank">disney.com</a>
<a href="http://www.wikipedia.org" target="_top">wikipedia.org</a>

```

```css
a[target="_blank"] {
  background-color: yellow;
}
```

![[Pasted image 20240411212812.png]]

---
## Selector [atributo~="valor"] 

El selector se utiliza para seleccionar elementos con un atributo valor que contiene una palabra especificada.`[attribute~="value"]`

En el ejemplo siguiente se seleccionan todos los elementos con un atributo title que contiene una lista de palabras separadas por espacios, una de las cuales es "flor":

>El ejemplo anterior coincidirá con los elementos  title="flower", title="summer flower", and title="flower new", but not title="my-flower" or title="flowers".

```html
<img src="klematis.jpg" title="klematis flower" width="150" height="113">
<img src="img_flwr.gif" title="flower" width="224" height="162">
<img src="img_tree.gif" title="tree" width="200" height="358">

```

```css
[title~="flower"] {
  border: 5px solid yellow;
}
```

![[Pasted image 20240411213211.png]]

---
## Selector [atributo|="valor"] 
El selector se utiliza para seleccionar elementos con el atributo especificado, cuyo valor puede ser exactamente el valor especificado o el valor especificado seguido de un guión (-).`[attribute|="value"]`

>**Nota:** El valor tiene que ser una palabra entera, ya sea sola, como class="top", o seguido de un guión( - ), como class="top-text".

```html
<h1 class="top-header">Welcome</h1>
<p class="top-text">Hello world!</p>
<p class="topcontent">Are you learning CSS?</p>
```

```css
[class|="top"] {
  background: yellow;
}
```

![[Pasted image 20240411213709.png]]

---
## Selector [atributo^="valor"] 
El selector se utiliza para seleccionar elementos con el atributo especificado, cuyo valor comienza con El valor especificado.`[attribute^="value"]`

En el ejemplo siguiente se seleccionan todos los elementos con un valor de atributo de clase que Comienza con "top":

>**Nota:** ¡El valor no tiene que ser una palabra completa!

```html
<h1 class="top-header">Welcome</h1>
<p class="top-text">Hello world!</p>
<p class="topcontent">Are you learning CSS?</p>

```

```css
[class^="top"] {
  background: yellow;
}
```

![[Pasted image 20240411214112.png]]


---
## Selector[attribute$="value"] 
El selector se utiliza para seleccionar elementos cuyo atributo value termina con un valor especificado.`[attribute$="value"]`

En el ejemplo siguiente se seleccionan todos los elementos con un valor de atributo de clase que termina con "test":

>**Nota:** ¡El valor no tiene que ser una palabra completa!

```html
<div class="first_test">The first div element.</div>
<div class="testsecond">The second div element.</div>
<div class="my-test">The third div element.</div>
<p class="mytest">This is some text in a paragraph.</p>
```

```css
[class$="test"] {
  background: yellow;
}
```
![[Pasted image 20240411214248.png]]

---
## Selector [attribute*="value"] 
El selector se utiliza para seleccionar elementos cuyo atributo value contiene un valor especificado.`[attribute*="value"]`

En el ejemplo siguiente se seleccionan todos los elementos con un valor de atributo de clase que Contiene "te":

>**Nota:** ¡El valor no tiene que ser una palabra completa!

```html
<div class="first_test">The first div element.</div>
<div class="second">The second div element.</div>
<div class="my-test">The third div element.</div>
<p class="mytest">This is some text in a paragraph.</p>
```

```css

[class*="te"] {
  background: yellow;
}
```

![[Pasted image 20240411214601.png]]