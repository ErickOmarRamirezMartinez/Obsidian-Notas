[ServerSocket (Java Platform SE 8 )](https://docs.oracle.com/javase/8/docs/api/java/net/ServerSocket.html)
# Constructores 

SERVERSOCKET
![[Pasted image 20250903085417.png]]


``` Java
try {
ServerSocket s = new ServerSocket();

//
InetSocketAddress l = new InetSocketAddress ("200.1.1.1", 1234);

s.bind(l);

}catch(Exeption e){

e.printStackTrace();

}

```


---
## Otra Alternativa para utilizar el contructor 



``` Java
try(){
ServerSocket s = new ServerSocket();

InetScoektAddress l = new ServerSocket(1234)
s.bind(l);
}
```


---

> Cual es le backlog de valor que se puede usar en el socket de flujo?


---

En el contexto de la clase **`ServerSocket`** en Java, el parámetro **`backlog`** se refiere al tamaño máximo de la cola de conexiones pendientes que el sistema operativo mantiene para ese socket.

---


# Metodos
![[Pasted image 20250903090300.png]]

``` java
try(){

ServerSocket s = new ServerSocket(1234);
System.out.prtintln("Servidor iniciado en el puerto" ts.getLocalPort());

for(;;){
socket cl = s.accept();
System.out.prtintln("CLiente conectado desde "+ cl.getInetAddress()+":"+cl.getPort());

System.out.prtintln("Tam ventana = "+":"cl.getOption(StandarSocketOptiion.SO_RCUBUFF));
}


}
```

----

 # Lectura y Escritura

``` Java
BufferedReader br = new BUfferedReader (new InputStreamReader(cl.getInputStream()));
String datos = br.readLine();

PrintWriter pw = new PrintWriter(New OutputStreamWriter(cl.getOutOutStream()));
pw.pritnln("Un mensaje dede el servidor bloqueante")
```




---

# Para poder escribir datos de diferentes tipos

PRIMITOS, Objetos y String

``` Java
DataOutputStream dos = new DataOutputStream(cl.getOutputStream());

dos.writeInt(s);
dos.writeLong(7);
dos.writeFloat(1.0f);
dos.writeDouble(3.7);
dos.writeUTF("cadena");

```