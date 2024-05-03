# Funciones
![[Pasted image 20240502100520.png]]
![[Pasted image 20240502100623.png]]
![[Pasted image 20240502100747.png]]
![[Pasted image 20240502100948.png]]

Las funciones de tipo `void` pueden realizar una variedad de tareas, como imprimir mensajes en la consola, modificar objetos, realizar cálculos internos, interactuar con bases de datos, entre otras. Aquí hay algunos ejemplos de funciones de tipo `void`

## Ejemplo de Carrito de Compras
```Java
package FuncionesEjemplo;

  

import java.util.ArrayList ;

import java.util.Iterator;

import java.util.List;

  

  

  

public class funciones {

static class Producto{ //Clase para mis productos

String nombre;

double precio;

Producto(String nombre, double precio){ // Constructor

this.nombre = nombre;

this.precio = precio;

}

}

static class CarritoDeCompra{

List<Producto> productos = new ArrayList<>(); // Lista que almacena los productos en el carrito de compra

void agregarProducto (Producto barbie) { //Funcion para agregar productos

productos.add(barbie);

}

double calcularTotal() { //Metodo para calcular el total de la compra

double total = 0;

for (Producto barbie : productos) {

total += barbie.precio;

}

return total;

}

double calcularDescuento() {

double total1 = calcularTotal();

double descuento = total1 * 0.10;

return descuento;

}

double calcularTotalDescuento() {

double total1 = calcularTotal();

double descuento = calcularDescuento();

double totaldecuento = total1 - descuento;

return totaldecuento;

}

}

public static void main(String[] args) {

Producto muñeca1 = new Producto("Chelsie", 98.80);

Producto muñeca2 = new Producto("Skipper", 99.80);

Producto muñeca3 = new Producto("Kelly", 72.50);

Producto muñeca4 = new Producto("Teresa", 120.00);

Producto muñeca5 = new Producto("Summer", 50.36);

Producto muñeca6 = new Producto("Barbara", 200.50);

CarritoDeCompra carrito = new CarritoDeCompra(); // Instanciar un nuevo carrito de compra

carrito.agregarProducto(muñeca5);

carrito.agregarProducto(muñeca6);

double totalCarrito = carrito.calcularTotal();

double totalDescuento = carrito.calcularTotalDescuento();

System.out.println("Total de tu carrito $"+totalCarrito);

System.out.println("Su total con el 10% de descuento seria: "+totalDescuento);

}

}
```


## Refactorizacion
La refactorización es el proceso de reestructurar el código existente sin cambiar su comportamiento externo. Se realiza para mejorar su legibilidad, mantenibilidad, y/o rendimiento sin alterar su funcionalidad. En el código que proporcionaste, podríamos realizar algunas refactorizaciones para mejorarlo:

1. **Separación de responsabilidades**: Actualmente, la clase `CarritoDeCompra` es responsable tanto de mantener una lista de productos como de calcular el total y el descuento. Sería más limpio dividir estas responsabilidades en métodos más pequeños y cohesivos.
    
2. **Nombres descriptivos**: Los nombres de variables y métodos deben ser descriptivos y representar con precisión su propósito. Por ejemplo, los nombres como `muñeca1`, `muñeca2`, etc., podrían ser más descriptivos para indicar qué tipo de productos son.
    
3. **Evitar cálculos repetidos**: En el método `calcularTotalDescuento`, se calcula el total dos veces: una vez para el total y otra vez para el descuento. Sería más eficiente calcular el total una vez y luego calcular el descuento basado en ese total.
    
4. **Utilizar constantes**: Si hay valores que se utilizan en varios lugares y no cambian, es una buena práctica definirlos como constantes para evitar errores tipográficos y mejorar la mantenibilidad.
    
5. **Comentarios explicativos**: Aunque el código que proporcionaste tiene algunos comentarios, podrían agregarse más para explicar partes complejas del código o el propósito de ciertas secciones.
    
6. **Uso de estructuras de datos adecuadas**: Dependiendo de los requisitos del programa, podríamos considerar si `ArrayList` es la estructura de datos más adecuada para el carrito de compra. Otras estructuras como `HashSet` podrían ser más eficientes si no necesitamos mantener el orden de los elementos.


### Una refactorización podría verse así:

```Java
// En la clase Producto, mantener solo la definición del producto
class Producto {
    String nombre;
    double precio;
    
    Producto(String nombre, double precio) {
        this.nombre = nombre;
        this.precio = precio;
    }
}

// En la clase CarritoDeCompra, mantener solo la lógica relacionada con el carrito
class CarritoDeCompra {
    List<Producto> productos = new ArrayList<>();

    void agregarProducto(Producto producto) {
        productos.add(producto);
    }

    double calcularTotal() {
        double total = 0;
        for (Producto producto : productos) {
            total += producto.precio;
        }
        return total;
    }

    double calcularDescuento(double total) {
        return total * 0.10;
    }

    double calcularTotalDescuento() {
        double total = calcularTotal();
        double descuento = calcularDescuento(total);
        return total - descuento;
    }
}

public class FuncionesEjemplo {
    public static void main(String[] args) {
        Producto muñeca1 = new Producto("Chelsie", 98.80);
        Producto muñeca2 = new Producto("Skipper", 99.80);
        Producto muñeca3 = new Producto("Kelly", 72.50);
        Producto muñeca4 = new Producto("Teresa", 120.00);
        Producto muñeca5 = new Producto("Summer", 50.36);
        Producto muñeca6 = new Producto("Barbara", 200.50);

        CarritoDeCompra carrito = new CarritoDeCompra();
        carrito.agregarProducto(muñeca5);
        carrito.agregarProducto(muñeca6);

        double totalCarrito = carrito.calcularTotal();
        double totalDescuento = carrito.calcularTotalDescuento();

        System.out.println("Total de tu carrito $" + totalCarrito);
        System.out.println("Su total con el 10% de descuento sería: " + totalDescuento);
    }
}

```


---
![[Pasted image 20240502140046.png]]
Astros.api
json.placeholder


JSON
FETCH


![[Imagen de WhatsApp 2024-05-02 a las 14.01.57_33ef7492.jpg]]


![[Pasted image 20240502163739.png]]