![[Pasted image 20240507101318.png]]
![[Pasted image 20240507101415.png]]
![[Pasted image 20240507101541.png]]
![[Pasted image 20240507101710.png]]
![[Pasted image 20240507102636.png]]

![[Pasted image 20240507101717.png]]![[Pasted image 20240507101811.png]]
![[Pasted image 20240507102644.png]]![[Pasted image 20240507102806.png]]
![[Pasted image 20240507102842.png]]


---
# Iteraciones en Java
## 1. Iterar mediante ciclo for-each

```Java
ArrayList<String> nombres = new ArrayList<String>();

nombres.addAll(Arrays.asList("Mario", "Juan", "Julia","Jessica"));

System.out.println(nombres);

for (String nombre : nombres) {

System.out.println(nombre);

}
```

## 2.  Iterar mediante Iterator

```Java
ArrayList<Double> salarios = new ArrayList<Double>();

salarios.addAll(Arrays.asList(22136.22d,8766.3d,12455.01d,6222.12d));

System.out.println(salarios);

// Mandamos a llamar la interfaz Iterador y la importamos (java.util). Le asignamos un nombre y definimos el ArrayList sobre el cual va a iterar utilizando el metodo iterator)=;

Iterator<Double> iteradorSalarios = salarios.iterator();

System.out.println(iteradorSalarios); // Output: java.util.ArrayList$Itr@5b480cf9

//Utilizamos el Iterator en un ciclo while , para que los elementos se muestren en forma de lista

//Utilizando el metodo hasNext() que sera true, siempre que encuentre mas elementos en el Iterator. Estos elementos se guardan en una variable que puede imprimirse

while (iteradorSalarios.hasNext()) {

Double elemento = (Double) iteradorSalarios.next();

System.out.println(elemento);

}
```

## 3. Mediante expresiones lambda 

```Java

```