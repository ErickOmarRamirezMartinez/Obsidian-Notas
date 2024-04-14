##  Ciclo While
Recorre un bloque de codigo mientras una condicion especifica sa verdadera
Imprimir los elementos de un array

```javascript
const frutas = ["fresa", "sandia", "naranja", "maanzana","zapote", "pera","mandarina","toronja", "guayaba"];

  

let fruta = 0;

while (fruta < frutas.length){

    console.log(frutas[fruta]);

    fruta++;

}
```

Imprimir una seciencia crecieente de asteriscos 1 a 5
```javascript
let limite = 5;

let iteracion = 0;

let asterisco = "";

  

while (iteracion < limite){

    asterisco += "*";

    iteracion++;

}
```

## Do While
Recorre un bloque de codigo mientras una condicion especifica sa verdadera, perso se ejecuta una veez sin importar la condicion

```Javascript
let j = 0;

while (j >1){

    console.log(j);

    j++;

}

  

do {

    console.log(j);

    j++;

}while (j > 1)
```


---
## Control de Ciclos
Podemos recurrir a dos sentencias: break y continue

Break detiene un ciclo, en cambio, continiue poermite que el ciclo continuea y muestra un valor distinto




---
# Retos
![[Pasted image 20240411110214.png]]
![[Pasted image 20240411110225.png]]
![[Pasted image 20240411110244.png]]
![[Pasted image 20240411110303.png]]

## Inspeccionar 
En la pestaña source, podemos acceder el debugger de nuestro codigo.
Para ello dbemos realizar lo siguieente:

1. Marca breakpoitn
2. recargar el navegador
3. Presionar el boton con la flecha circular  para recorrer paso por paso
4. En la lista de Scope aparece el paso a paso 

---

![[Pasted image 20240411132801.png]]

## Operador de comparacion: 

Son operadores que comparan dos expresionees y devuelven un valor booleano 

### Operador de Igualdad
heca si un valor es igual a otro

`==`
`<=`
`>=`

### Operadores Logicos
`AND &&`
`OR ||`
`NOT !`

![[Pasted image 20240411141107.png]]
