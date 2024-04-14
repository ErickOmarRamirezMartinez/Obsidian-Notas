# HTML Avanzado
![[Pasted image 20240401100658.png]]

## Tablas
![[Pasted image 20240401102358.png]]

## Navegacion
![[Pasted image 20240401104601.png]]


## Formularios

[https://developer.mozilla.org/es/docs/Web/HTML](https://developer.mozilla.org/es/docs/Web/HTML "https://developer.mozilla.org/es/docs/web/html")


```html
<!DOCTYPE html>

<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Document</title>

    <link rel="stylesheet" href="estilo.css">

</head>

<body>

    <header>

        <h1>Haz tu primer carta atral</h1>

    </header>

    <section id="fondo">

        <h3>Tu carta astral es una "foto" del nacimiento: puedes ver la ubicacion y conexcion de los planetas en ese instante para hacer de la astrologia tu herramienta de auto observacion y crecimiento</h3>

    </section>

    <main>

        <section id="main">

            <h2>Ingresa tus datos para comenzar</h2>

            <p><b>Atencion :</b> Es importante que tenga la informacion correcta, de lo contrario el calculo que obtendras no sera preciso.</p>

            <form action="" id="formulario">

                <label ><b>Tu informacion:</b></label>

                <label for="">Tu Nombre:</label>

                <input type="text" name="Nombre" id="" placeholder="Ingresa tu nombre">

                <label for="">E-mail:</label>

                <input type="email" name="Email" id="" placeholder="Ingresa tu email">

  

                <label for=""><b>Hora de Nacimiento </b></label>

                <input type="time" name="" id="">

  

                <label for=""><b>Fecha de Nacimiento </b></label>

                <input type="date" name="" id="">

  

                <label for=""><b>Lugar de Nacimiento </b></label>

                <label for="">Pais</label>

                <input type="text" name="Pais" id="">

                <label for="">Ciudad de Nacimiento</label>

                <input type="text" name="Ciudad" id="">

                <input type="button" value="Enviar" style="margin: auto;">

  

            </form>

        </section>

    </main>

</body>

</html>
```

```css
header{

    background-color: antiquewhite;

    display: flex;

    font-size: 20px;

    font-weight: bold;

    justify-content: center;

    align-items: center;

  

}

h2, p{

    display: flex;

    justify-content: center;

     justify-items: center;

     align-items: center;

     margin: auto;

  

}

main{

    background-color: bisque;

  

}

  

input[type="text"], input[type="email"], input[type="date"], input[type="time"] {

    width: 100%;

    padding: 8px;

    margin: 10px 0;

    border-radius: 4px;

    border: 1px solid #ccc;

    box-sizing: border-box;

}

body{

    padding: 10px;

}

#main{

    background: white;

    width: 50%;

    padding: 30px;

    border-radius: 8px;

    box-shadow: 0 0 10px rgba(0,0,0,0.1);

    margin: 20px auto;

  

}

input[type="button"] {

    width: 100%;

    padding: 10px;

    background-color: #007bff;

    color: white;

    border: none;

    border-radius: 4px;

    cursor: pointer;

    font-size: 16px;

}

label {

    font-weight: bold;

    margin-top: 15px;

    display: block; /* Hace que cada label aparezca en su propia línea */

}

#fondo{

    background-image: url("https://i.ytimg.com/vi/65nK5Vj0QIk/maxresdefault.jpg");

    color: white;

    height: 100px;

    margin: 10px 10px;

  

    display: flex;

    justify-content: center;

    align-items: center;

  

}
```

