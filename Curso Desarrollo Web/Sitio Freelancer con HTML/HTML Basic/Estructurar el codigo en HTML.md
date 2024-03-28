![[Pasted image 20240327175618.png]]

>En caso de no poder utilizar cualquiera de las etiquetas, siempre podemos utilizar div 

1. **`<header>`**: Se utiliza para representar el encabezado de una sección o de todo el documento. Puede contener logotipos, enlaces de navegación principales, barras de búsqueda, etc.
    
2. **`<nav>`**: Sirve para definir una sección de navegación. Contiene enlaces a otras páginas o secciones del sitio.
    
3. **`<main>`**: Esta etiqueta envuelve el contenido principal de la página. Específicamente, representa el contenido único y relevante de la página, excluyendo cualquier contenido repetitivo que aparezca en múltiples páginas (como encabezados o pies de página).
    
4. **`<section>`**: Se utiliza para agrupar contenido relacionado temáticamente. Por ejemplo, un blog puede tener secciones para artículos, comentarios, etc.
    
5. **`<article>`**: Se usa para representar un contenido independiente que puede existir por sí mismo, como un artículo de un blog, una entrada de un foro o una noticia.
    
6. **`<aside>`**: Define contenido secundario relacionado con el contenido circundante. Puede contener barras laterales, publicidad, enlaces relacionados, etc.
    
7. **`<footer>`**: Representa el pie de página de una sección o del documento completo. Suele incluir información de contacto, enlaces de navegación secundarios, créditos, etc.
    
8. **`<figure>` y `<figcaption>`**: `<figure>` se usa para encapsular cualquier contenido que se refiera a una imagen, diagrama, código, etc., mientras que `<figcaption>` proporciona una leyenda o descripción para ese contenido.


### Aqui un ejemplo sencillo de como agrupar tu codigo

```html
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Document</title>

</head>

<body>

<header>

<h1>Erick Omar Full Stack Developer</h1>

</header>

  

<section>

<h2>Desarrollador Java Full Stack </h2>

<p>Edo Mex, Mexico</p>

</section>

  
  

<main>

<h2>Mis servicios</h2>

  

<section>

<h3>Frontend</h3>

<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus reiciendis natus, adipisci consequatur culpa praesentium exercitationem?</p>

</section>

<section>

<h3>Backend</h3>

<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus reiciendis natus, adipisci consequatur culpa praesentium exercitationem?</p>

</section>

<section>

<h3>Habilidades Personales</h3>

<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus reiciendis natus, adipisci consequatur culpa praesentium exercitationem?</p>

</section>

</main>

  

<section>

<h2>Contacto</h2>

</section>

  

<footer>

<p>Todos los derechos reservaador. Erick Omar Ramirez Martinez</p>

</footer>

  

</body>

</html>
```

