![[Pasted image 20240503101028.png]]
![[Pasted image 20240503101052.png]]
![[Pasted image 20240503101148.png]]![[Pasted image 20240503101247.png]]![[Pasted image 20240503101519.png]]
![[Pasted image 20240503102122.png]]
![[Pasted image 20240503102230.png]]
La Lista se refiere a una colección de varios elementos en una secuencia, en la que cada elemento es básicamente un objeto. Además, podemos acceder a estos elementos por sus posiciones (índice). Por otro lado, una ArrayList crea una matriz (dinámica) de objetos que puede reducir o aumentar fácilmente su tamaño cuando sea necesario.

1. **Tamaño fijo vs tamaño dinámico:**
    
    - Los arreglos tienen un tamaño fijo que se define al momento de su creación. No pueden crecer o disminuir de tamaño dinámicamente.
    - Por otro lado, las listas, especialmente `ArrayList`, pueden crecer o disminuir de tamaño dinámicamente según sea necesario. No tienen un tamaño fijo y pueden agregar o eliminar elementos fácilmente.
2. **Tipos de datos:**
    
    - En un arreglo, todos los elementos deben ser del mismo tipo de datos. Por ejemplo, si creas un arreglo de enteros, solo puedes almacenar enteros en él.
    - En una lista, especialmente en `ArrayList`, puedes almacenar elementos de diferentes tipos de datos en la misma lista. Esto se debe a que las listas en Java pueden almacenar objetos, y los objetos pueden ser de cualquier tipo.
3. **Funcionalidades:**
    
    - Los arreglos proporcionan un conjunto limitado de funcionalidades. No tienen métodos como `add()` o `remove()` para agregar o eliminar elementos.
    - Las listas, en particular `ArrayList`, ofrecen una variedad de métodos útiles para manipular los datos, como `add()`, `remove()`, `get()`, `set()`, entre otros. Estos métodos hacen que sea más fácil trabajar con colecciones de datos de manera dinámica.

## Array

```Java
/*------Array---------*/

String[] nombres = {"Dani", "Fernanda", "Gaby"};

int[] edades = {37, 30 , 30};

//Para imprimir los valores de un Array, debemos utilizar un metodo d Arrays y el array que queremos imprimir

System.out.println(Arrays.toString(nombres));

System.out.println(Arrays.toString(edades));

//Acceder un elemento del Array

String nombre1 = nombres[0];

System.out.println(nombre1);

//Longitud de un Array

int longitudEdades = edades.length;

int longitudNombres = nombres.length;

System.out.println(longitudEdades);

//Mostrar cada elemento con forEach

for (String nombre: nombres) {

System.out.println(nombre);

}
```

## ArrayList
Es un Array que puede cambiar de tamaño y permite elementos duplicados
 ```Java
 /*---------ArrayList--------------*/

//Como inicializar un ArrayList

ArrayList<String>Peliculas = new ArrayList<String>(); //Como clase

List<Double>salario = new ArrayList<Double>(); //Como interfase

List<Integer> inventario = new ArrayList<>(); //Wrapper class

//Agregando valores a los ArrayList

Peliculas.add("Titanic");

Peliculas.add("La isla siniestra");

Peliculas.add("Frozen");

salario.add(1799.00);

salario.add(1799.00);

salario.add(1799.00);

inventario.add(20);

inventario.add(15);

inventario.add(10);

System.out.println(Peliculas);

System.out.println(salario);

System.out.println(inventario);
```

---
## Metodos
```Java
//Metodo para acceder a un elemento del ArrayList : name.get(index);

String pelicula2 = Peliculas.get(1);

System.out.println(pelicula2);

//Metodo para modificar un elemento: name.set(index, newValue);

inventario.set(0, 17);

System.out.println(inventario);

//inventario.set(1, 98);

//System.out.println(inventario); //Exception no existe el indice 1 dentro del arrayList

//Metodo para eliminar un elemento

salario.add(500.0d);

System.out.println(salario);

int ultimoElemento = (salario.size())-1;

salario.remove(ultimoElemento);

System.out.println(salario);
```

---
## HashSet
En los HashSet cada elemento es unico, no existen elementos duplicados

```Java
/*-----------HashSet-------------------*/

HashSet<String> animalitos = new HashSet<String>();

animalitos.addAll(Arrays.asList("Perritos", "Gatito", "Pinguino", "Capibara", "capibara", "Capibara", "Gatito"));

System.out.println(animalitos);

//Utilizando la tabla Hash, recorre todos los elementos y muestra elementos unicos

HashSet<Character> caracteres = new HashSet<Character>();

caracteres.addAll(Arrays.asList('a','b','c','d','e','f','a','b','c','d','e','f','a','b','c','d','e','f'));

System.out.println(caracteres);

//Metodo para conocer si un elemento se encuentra en el Set

System.out.println(animalitos.contains("Gatito")); //Debe devolver true

//Aplicando size para conocer la longitud del Set

System.out.println(animalitos.size()); //Ignora los repetidos

//Eliminando elementos

caracteres.remove('a');

System.out.println(caracteres);

System.out.println(caracteres.size());

//Metodo para limpiar

animalitos.clear();

System.out.println(animalitos);
```

---
## Soft Method
Metodo Sort
Permite ordenar los elementos de una Coleccion
```Java
/*-----------Metodo Sort-------------------*/

ArrayList <String> peliculas = new ArrayList<>();

Set<Integer> edades = new HashSet<>();

//Llenar el ArrayList y el HashSet

peliculas.addAll(Arrays.asList("interestelar", "Glass", "Interestelar", "MadMax", "Jhon Wick", "Opppenhaimer"));

edades.addAll(Arrays.asList(18, 22, 37, 22, 27, 30, 25, 30, 27, 25));

System.out.println(peliculas);

System.out.println(edades);

//Metodo para Ordenar los elementos: Collection.sort(Collection);

Collections.sort(peliculas);

System.out.println(peliculas);

TreeSet<Integer> edades1 = new TreeSet<Integer>();

edades1.addAll(Arrays.asList(18, 22, 37, 22, 27, 30, 25, 30, 27, 25));

System.out.println(edades1);

edades = new TreeSet<>(edades);

System.out.println(edades);
```

---

## Hash Map
Almacena elementos en pares (Key/value) y se puede acceder a ellos mediante index. No es ordenado y permite datos duplicados
```java
public static void main(String[] args) {

/*------------Hash Map------------------*/

HashMap<Integer, String> nombreCompleto = new HashMap<>();

//Metodo para agregar pares .put();

nombreCompleto.put(36, "Daniel Maldonado");

nombreCompleto.put(12, "Gabi Cortes");

nombreCompleto.put(22, "Fer Ramos");

nombreCompleto.put(36, "Daniel Maldonado");

System.out.println(nombreCompleto);

//Recorrer un HashMap

//Vamos a implementar un metodo de la interfaz Map que se llama Entry

for (Map.Entry<Integer, String> nombre : nombreCompleto.entrySet()) {

System.out.println("Id: "+nombre.getKey() +" Nombre Completo: "+nombre.getValue());

}

}
```


---
![[Pasted image 20240503134403.png]]![[Pasted image 20240503134557.png]]