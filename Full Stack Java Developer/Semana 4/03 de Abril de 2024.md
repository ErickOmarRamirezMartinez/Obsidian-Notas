![[Pasted image 20240403100055.png]]

![[Pasted image 20240403100234.png]]
![[Pasted image 20240403102426.png]]

![[Pasted image 20240403102447.png]]

# Media Query
Una media query en CSS es una herramienta utilizada para aplicar estilos de forma condicional según las características del dispositivo de visualización, como su ancho, altura, resolución, orientación, entre otros. Esto es esencial en el diseño web responsive, donde el objetivo es asegurar que el contenido de un sitio web se vea bien en una amplia gama de dispositivos, desde computadoras de escritorio hasta tablets y teléfonos móviles.

![[Pasted image 20240403104139.png]]

# Display Flex (FlexBox)
![[Pasted image 20240403105227.png]]

![[Pasted image 20240403122428.png]]

[https://flexboxfroggy.com/#es](https://flexboxfroggy.com/#es "https://flexboxfroggy.com/#es")

# Display Grid
![[Pasted image 20240403132529.png]]


[https://cssgridgarden.com/#es](https://cssgridgarden.com/#es "https://cssgridgarden.com/#es")


### Comparación y Elección

**Flexibilidad vs. Control**:

- **Flexbox** ofrece más flexibilidad para distribuir espacio y alinear ítems dentro de un contenedor cuando el diseño es principalmente en una dimensión.
- **Grid** ofrece más control sobre la disposición y alineación de elementos cuando el diseño se extiende tanto vertical como horizontalmente.

**Uso Combinado**:

- En la práctica, Flexbox y Grid no son mutuamente excluyentes y a menudo se utilizan juntos en los mismos proyectos. Por ejemplo, Grid puede ser utilizado para crear la estructura general de la página, mientras que Flexbox puede manejar el diseño de componentes más pequeños dentro de esa estructura.
![[Pasted image 20240403155239.png]]

```html
<!DOCTYPE html>

<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Document</title>

    <link rel="stylesheet" href="../styles/grid-example.css">

</head>

<body>

    <div class="container-1">

        <header class="responsive-1">Header</header>

        <sidebar class="responsive-1">Sidebar</sidebar>

        <main class="responsive-1">Main</main>

        <section class="responsive-1">Section</section>

        <content class="responsive-1">Content</content>

        <footer class="responsive-1">Footer</footer>

    </div>

</body>

</html>
```

```css
:root{

    --primary-color: #BF0404;

    --secondary-color: #590202;

    --terciary-color: #8C0303;

    --font-color-primary: #ffffff;

    --font-color-secondary: #A68444;

    --background-color: #260101;

    --font-size-title: 22px;

    --font-size-subtitle: 18px;

    --font-size-text: 16px;

    --font-family: 'Karla', sans-serif;

}

body{

    background-color: var(--background-color);

    font-family: var(--font-family);

    color: var(--font-color-primary);

}

/*Grid*/

header {

    background-color: #A68444;

    grid-area: head;

}

sidebar {

    background-color: blueviolet;

    grid-area: sidebar;

}

main {

    background-color: yellowgreen;

    grid-area: main;

}

section {

    background-color: steelblue;

    grid-area: section;

}

content {

    background-color: springgreen;

    grid-area: content;

}

footer {

    background-color: mediumvioletred;

    grid-area: footer;

}

/* Items de Grid */

.container-1 {

    display: grid;

    /* gap: 5px; */

    grid-template-columns: repeat(3, 1fr);

    grid-template-rows: 1fr 2fr 2fr 1fr;

    grid-template-areas:

        "head head head"

        "sidebar main main"

        "sidebar section content"

        "footer footer footer";

    width: auto;

    height: 500px;

    border: solid #ffffff 1px;

    margin: 14px;

    color: #ffffff;

    text-align: center;

}

@media (max-width: 420px) {

    .container-1 {

        display: grid;

        /* gap: 5px; */

        grid-template-columns: 1fr;

        grid-template-rows: 10% 30% 30% 10%;

        grid-template-areas:

            "head"

            "sidebar"

            "main"

            "section"

            "content"

            "footer";

        width: auto;

        border: solid #ffffff 1px;

        margin: 14px;

        color: #ffffff;

        text-align: center;

        font-size: 25px;

        padding: 10px;

    }

}
```
