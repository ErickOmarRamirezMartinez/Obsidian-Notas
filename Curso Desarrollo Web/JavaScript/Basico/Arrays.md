![[Pasted image 20240410173746.png]]
![[Pasted image 20240410173833.png]]
![[Pasted image 20240410173958.png]]
![[Pasted image 20240410174250.png]]
![[Pasted image 20240410174505.png]]
![[Pasted image 20240410174541.png]]
![[Pasted image 20240410175015.png]]


---

## Opcion 1 para inicializar un arreglo

```javascript
const shopping = ["pan", "leche", "queso", "jamon", "tortillas", "huevos", "galletas"];

  

console.log(shopping);
```

## Opcion 2 para inicializar un arreglo

```Javascript
//A partir de un Array vacion, iremos agregando elementos por cada index

const cars = [];

//Agrego elementos llamando el Array y el indx de cada elemento

cars[0] = "Vorlkswagen";

cars[1] = "Audi";

cars[3] = "BMW";

cars[2] ="Volvo";

  

console.log(cars);
```

## Opcion 3 para inicializar un arreglo

```JavaScript
//Como son Arrays son objetos poseen su propia clase (Array)

const flores = new Array("Rosa", "Bugambillia", "Cempashuchitl");

console.log(flores);
```

---
# Propiedades

## Longitud de un arreglo (length)
```javascript
console.log(`El arreglo shopping tiene ${shopping.length} elementos`);
```

## Accedieendo a un elemento mediante su indice
```javascript
console.log(`Te ganaste un ${cars[3]} y un ramo de ${flores[2]}`);
```

## Accediento al ultimo elemento del array
```javascript
console.log(flores[flores.length - 1]);
```

---
# Arrays multimensionalees (Array de Arrays)

```Javascript
console.log("======Arrays multidimensionales (Arrays de Arrays)=======");

let comidas = ["tamal de caminito", "Corundas", "Memelas", "Torta Ahogada", "salbut", "Chile Atole"]

let paises = ["Yucatan", "Guadalajara", "Oaxaca", "Michoacan", "Puebla", "Tabasco"];

  

//Primra manera de escribirlo

let menu = [comidas, paises];
```


Mandando a llamar al salbut, quee se encuentra en el array comida con el indice 0 y el elemento salbut con el indice 4
```Javascript
console.log(menu[0][4]);

console.log(`La ${menu[0][3]} es tradicional en ${menu[1][1]}`);
```

---
# Metodos de Arreglos

## IndexOf()
Me permite conocer el indice de un elemento del array

```Javascript
console.log(CH39.indexOf("Benji"));

console.log(CH39.indexOf("Diana"));

console.log(CH39.indexOf("benji"));
```

## pop()
Elimina el ultimo elemento del array
```Javascript
CH39.pop();

console.log(CH39);

console.log(CH39[CH39.length-1]);
```

## push()
Agregamos un nuevo elemento al final del Array
```Javascript
CH39.push("Diana");

console.log(CH39[CH39.length-1])
```

## unshift()
Agregamos un elemento al inicio del Array
```Javascript
CH39.unshift("Liliana");

console.log(CH39[0]);
```

## shift()
Elimina el primer elemento del Array
```Javascript
CH39.shift();

console.log(CH39[0]);

````

![[Pasted image 20240410132611.png]]