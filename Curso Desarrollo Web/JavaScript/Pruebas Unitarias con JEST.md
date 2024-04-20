Ultima Tema de JavaScript Vanilla 

![[Pasted image 20240419113807.png]]
![[Pasted image 20240419113919.png]]
![[Pasted image 20240419114041.png]]

[Pruebas Unitarias](https://aws.amazon.com/es/what-is/unit-testing/)

![[Pasted image 20240419115005.png]]
![[Pasted image 20240419115308.png]]
![[Pasted image 20240419115439.png]]

https://www.hiberus.com/crecemos-contigo/los-estandares-de-calidad-del-software-mas-importantes/

![[Pasted image 20240419120816.png]]

https://g.co/kgs/ocpKapc
Puestos QA : Intern o new grad o trainee

![[Pasted image 20240419122047.png]]
![[Pasted image 20240419122107.png]]
https://jestjs.io/
https://jestjs.io/docs/getting-started

---
# Pruebas Unitarias con Jest

## Inicializar node con la configuracion por default

 ```sh

npm init -y

```

## Crear nuestro enter point

`index.js`


## Instalar jest

```sh

npm install --save-dev jest

```

  

## Configurar las dependencias de jest

```javascript

{

  "scripts": {

    "test": "jest"

    }

}

```


## Configurando nuestros archivos

 1. Crear carpeta `src` y dentro las carpetas `modules` y `tests`

  
 2. Dentro de `modules`, crear el archivo `calculator.js` con las funciones requeridas

    >Nota: En este proyecto estamos usando modulos de CommondJS y no de EcmaScript(ES)

  

 3. Dentro de `test` crear el archivo `calculator.test.js`


 4. Crear funciones de `tests`, para evaluar y probar el codigo.


 5. Ejecutar las pruebas unitarias con el comando

 ```sh

npm test

 ```

  

 ```sh

Erick  …\󰈙 \CH-39\JS-Jest    v21.6.1  ♥ 13:42   npm test

  

> js-jest@1.0.0 test

> jest

  

 PASS  src/test/calculator.test.js

  √ Suma de dos numeros  (12 ms)

  √ Resta de dos numeros

  √ Multiplicacion de dos numeros

  √ Division de dos numeros

  

Test Suites: 1 passed, 1 total

Tests:       4 passed, 4 total

Snapshots:   0 total

Time:        0.609 s, estimated 1 s

Ran all test suites.

 ```


```js
// Pruebas Unitarias Automatisadas

  

//Importo el archivo .js en donde vive mi modulo

const calculator = require('../modules/calculator');

  

//Estructura de test: test("string", callback =>{expect(function})

test("Suma de dos numeros ", () => {

    expect(calculator.suma(10,20)).toBe(30);

});

  

test("Resta de dos numeros ", () => {

    expect(calculator.substract(10,20)).toBe(-10);

});

  

test("Multiplicacion de dos numeros ", () => {

    expect(calculator.multply(10,20)).toBe(200);

});

  

test("Division entre 0 ", () => {

    expect(calculator.divide(55,0)).not.toBeNull();

});

  

test("Division de dos numeros ", () => {

    expect(calculator.divide(10,2)).toBe(5);

});

//Test para obtener un valor cercano al esperado

test("Division de dos numeros ", () => {

    expect(calculator.divide(55,7)).toBeCloseTo(7.858);

});
```


```sh
Erick  …\󰈙 \CH-39\JS-Jest    v21.6.1  ♥ 14:01  npm test

> js-jest@1.0.0 test
> jest

 PASS  src/test/calculator.test.js
  √ Suma de dos numeros  (3 ms)
  √ Resta de dos numeros                                                                                                                                                          
  √ Multiplicacion de dos numeros  (1 ms)                                                                                                                                         
  √ Division entre 0  (1 ms)                                                                                                                                                      
  √ Division de dos numeros                                                                                                                                                       
  √ Division de dos numeros                                                                                                                                                       
                                                                                                                                                                                  
Test Suites: 1 passed, 1 total                                                                                                                                                    
Tests:       6 passed, 6 total    
```

---
# Genererar archivo .gitignore 
https://www.toptal.com/developers/gitignore