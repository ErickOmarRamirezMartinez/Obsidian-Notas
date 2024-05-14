![[Pasted image 20240513153741.png]]
![[Pasted image 20240513153756.png]]![[Pasted image 20240513153825.png]]

---
## Main
```Java
package hilos;

  

public class Hilos {

public static void main(String[] args) {

HilosUno ejemploUno = new HilosUno();

Thread ejemploDos = new Thread(new HilosDos());

ejemploUno.start();

ejemploDos.start();

}

}
```

## Treads
```Java
package hilos;

  

public class HilosUno extends Thread{

@Override

public void run () {

for (int i = 0; i <= 5; i++) {

System.out.println("Ejemplo 1");

}

}

}
```

## Runnable
```Java
package hilos;

  

public class HilosDos implements Runnable{

@Override

public void run () {

for (int i = 0; i <= 5; i++) {

System.out.println("Ejemplo 2");

}

}

}
```