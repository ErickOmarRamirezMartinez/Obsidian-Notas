
---
![[Imagen de WhatsApp 2024-04-18 a las 12.55.49_668153b7.jpg]]
![[Imagen de WhatsApp 2024-04-18 a las 12.55.49_25de1ab4.jpg]]


NodeJS: Node.js es un entorno de ejecución de JavaScript del lado del servidor que permite a los desarrolladores crear aplicaciones web y de red de manera eficiente. Básicamente, Node.js permite ejecutar código JavaScript fuera del navegador web, lo que significa que puedes utilizar JavaScript tanto en el lado del cliente (navegador) como en el lado del servidor (backend).

![[Pasted image 20240418121201.png]]
Node es el entorno de ejecucion
Permite ejecutar

![[Pasted image 20240418123634.png]]
Permite Administrar
![[Pasted image 20240418124740.png]]

https://www.turing.com/blog/top-npm-packages-for-node-js-developers/

![[Pasted image 20240418125911.png]]

---
# Crear un nuevo paquete de npm

## Pasos para crear el package

1. Inicializar npm desde CLI en el directorio del proyecto con el comando

```sh

    npm init

```


2. Seleccionar las opciones que nos muestra npm en CLI.
``` sh
Erick  …\CH-39\JS-NPM\npm-parImpar  ♥ 13:07  npm init 
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help init` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
package name: (npm-parimpar)
version: (1.0.0)
description: Permite determinar si un numero es par o es impar 
entry point: (index.js)
test command:                                                                                                                                                                     
git repository:                                                                                                                                                                   
keywords: generation, ch39
author: erickORM
license: (ISC)                                                                                                                                                                    
About to write to C:\Users\Erick\Documents\CH-39\JS-NPM\npm-parImpar\package.json:

{
  "name": "npm-parimpar",
  "version": "1.0.0",
  "description": "Permite determinar si un numero es par o es impar ",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [
    "generation",
    "ch39"
  ],
  "author": "erickORM",
  "license": "ISC"
}


Is this OK? (yes)
```

3. Como definimos que el enter point se llama `index.js`, crear el archivo en main

  
4. Crear una carpeta llamado `module`, en donde vivira nuestro modulo

  
5. Crear el script dentro de la carpeta `moudules`, con el nombre ``parImpar.js`

    Aqui vivira el código funcional para mi package
  6. Dentro de `parImpar.js` creamos una funcion para determinar si un numero es par o impar
```JavaScript
//Funcion que me permite determinar si un numeero es par o Impar

  

const determinarParidad = (numero)=>{

    console.log((numero % 2 === 0) ? "par" : "impar");

}

  

//Exportar mi funcion para que pueda ser utilizada en cualquier parte de mi proyecto

export default determinarParidad;
```

7. Exportar la funcion para que pueda ser utilizada en cualquier parte de mi proyecto


```javascript

export default determinarParidad;

```

  
8. Importar mi funcion en `index.js` para que la podemos utilizar (`import from -ruta-`)
```JavaScript
//Importar la funcion desde la ruta especifica

import determinarParidad from "./modules/parImpar.js";
```

9. Modificar el package.json para permitir ejecutar desde module utilizando las configuracion `"type": "module"`
```json
{

  "name": "npm-parimpar",

  "version": "1.0.0",

  "description": "Permite determinar si un numero es par o es impar ",

  "main": "index.js",

  "type": "module",

  "scripts": {

    "test": "echo \"Error: no test specified\" && exit 1"

  },

  "keywords": [

    "generation",

    "ch39"

  ],

  "author": "erickORM",

  "license": "ISC"

}
```

10. Ejecuto mi aplicacion en CLI utilizando el comando

```sh

Erick  …\CH-39\JS-NPM\npm-parImpar   v21.6.1  ♥ 13:52  node index.js

El número 2369 es impar

El número 8974 es par

  

```

>   Tambien podemos utilizaar `node --watch index.js`

---
# Pasos para publicar el package en npm  

1. Registrar en el sitio de npm


[npm WebSite](https://www.npmjs.com/)

  
2. Modificar el `name` en `package.json` para que sea unico

  
3. En CLI iniciamos sesion con el comando

  

```sh

    npm login

```

  

```sh

Erick  …\CH-39\JS-NPM\npm-parImpar   v21.6.1  ♥ 13:53  npm login    

npm notice Log in on https://registry.npmjs.org/

Login at:

https://www.npmjs.com/login?next=/login/cli/eac3ef86-512a-4cd2-a2ce-061a598fd307

Press ENTER to open in the browser...

  

Logged in on https://registry.npmjs.org/.

```

  

4. Seguimos el proceso de autenticacion de 2 pasos en eel correo

  

5. Regresamos a CLI y nos muestra el mensaje `Logged in on https://registry.npmjs.org/.``

  

6. Lo unico que queda es publicar el package desde CLI con visibilidad publica usando el comando:

  

```sh

    npm publish --access=public

```

  

```sh

  

Erick  …\CH-39\JS-NPM\npm-parImpar   v21.6.1  ♥ 15:38  npm publish --access=public    

npm notice

npm notice 📦  erickomar--parimpar@1.0.0

npm notice === Tarball Contents ===

npm notice 1.8kB README.md

npm notice 192B  index.js

npm notice 335B  modules/parImpar.js

npm notice 343B  package.json

npm notice === Tarball Details ===

npm notice name:          erickomar--parimpar

npm notice version:       1.0.0

npm notice filename:      erickomar--parimpar-1.0.0.tgz

npm notice package size:  1.3 kB

npm notice unpacked size: 2.6 kB

npm notice shasum:        59e9199bba0dfb7c3382dd20e804b06dde140901

npm notice integrity:     sha512-3yotqSKkp15Mo[...]+3OJZk7xUwS6A==

npm notice total files:   4

npm notice

npm notice Publishing to https://registry.npmjs.org/ with tag latest and public access

Authenticate your account at:

https://www.npmjs.com/auth/cli/613aa78b-1c1d-4ef9-9db5-5570fbcc3985

Press ENTER to open in the browser...

  

+ erickomar--parimpar@1.0.0

```
---

> Pa hacer cambios en el mismo paquete
> Tienes que ir a `package.json` y cambiar la versión

```JavaScript
{

  "name": "erickomar--parimpar",

**"version": "1.0.1",******************************************************

  "description": "Permite determinar si un numero es par o es impar ",

  "main": "index.js",

  "type": "module",

  "scripts": {

    "test": "echo \"Error: no test specified\" && exit 1"

  },

  "keywords": [

    "generation",

    "ch39"

  ],

  "author": "erickORM",

  "license": "ISC"

}
```

