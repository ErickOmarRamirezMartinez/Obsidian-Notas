[Index of /axel/aplicaciones/diapositivas](http://148.204.58.221/axel/aplicaciones/diapositivas/)

# TCP
TCP (Protocolo de Control de Trasmision) esta Estandarizado validado por IETF (Internet Engineering Task Force)
Es el protocolo de la capa de transporte que proporciona un servicio de entrega confiable de transferencia de datos de extremo a extremo

Y ofrece un metodo para pasar datos encapsulados mediante TCP a un protocolo de la capa de aplicacion 


## Carcateristicas de TCP
*  **Orientado a Conexion
	  * Antes de poder transferir datos, procesos (local y rmeoto) deben negociar una conexion TCP mediante un proceso establecido de conexion (handshake)
	  * Las conexiones TCP se cierran formalmente mediante el proceso de finalizacion de xonecion TCP
*  **FULL DUPLEX
	* Para cada terminal TCP, la conexion TCP esta formada por dos canales logicos: un canal para tramitir datos (salidas) y uno para recibir datos (entrada)
	* La interfaz de red, podria tramsitir y recibir datos al mismo tiempo
	* El encabezado TCP contiene el numero de secuencia de los datos de salida y un reconocimiento de los datos

* **Fiable
	* En el tramisor, los datos enviados en una conexion TCP estan secuenciados y se espera un reconocimiento afirmativo por parte del receptor
	* Si no se recibe ningun reconocimiento, el segmento se trasmite de nuevi 
	* Los segmentos duplicados, se descartan 
* **Secuencia de bytes
	* TCP reconoce los datos enviados a traves de los canales de entrada y salida como una secuencia continua de bytes
	* El numero de secuencia y el numero de reconocimiento en cada enzabezado TCP se define en limites de bytes
	*  **TCP NO RECONOCE limites de mensajes o registros en la secuencia de bytes
* **Control de flujo del emisor y receptor
	* Para evitar el envio de demasiados datos a la vez y la saturacion de la red IP
	* TCP implementa control de flujo del emisor que, gradualmente, escala la cantidad de datos a la vez
	* Para evitar que el emisor envie datos que el receptor no puede almacenar en buffer
* **Entrega uno a uno
	* Las conexion de TCP son un circuito logico punto a punto entre dos protocolos de la capa de Aplicacion
	* TCP no proporciona un servicio de uno a varios 

>Normalmente , TCP se utiliza cuando el protocolo de la capa de Aplicacion requiere un servicio de transferencia de datos confiable y el protocolo de aplicacion no proporciona este tipo de servicios 


![[IMG_20250828_090811.jpg]]


---
# Formato de encabezado de TCP
![[IMG_20250828_092717.jpg]]


PPP o MTU


* Source Port y Destination port
  ID Identificadores , para saber de que aplicacion viene y que aplicacion va 

* Sequence Number 
  Numero de secuencia, Se utiliza al envio cada paquete y se utiliza para que el destinario pueda saber si ese segmento que esperaba es el correcto 

+ Acuse
  Numero de byte que se esperaba recibir en el siguiente segmento por recibir 

* Tamaño de Ventana
  Es el espacio en Buffer de datos de TCP

* Conjunto de Banderas
	* SYN = Sincronizacion , es el proceso remoto en un dispositivo quiere establecer una conexion con otro dispositivo
	* RST = Rechazo de Sincronizacion
	* FIN = EL cliente ya no quiere la conexion por lo que envia una finalizacion de conexion 
	* ACK = Se va encender, siempre que yo responde cualquier trama 
	* PSH = la app emisora informa a TCP que los datos deben enviarse inmediatamente (Flush). Tambien informa al receptor que los datos deben entrgados a la app destino en cuanto lleguen
	* URG = Bandera Urgente
	* ECE = Congestionamiento Explicito Encontrado
	  CWR = Reduccion de Ventana por Congestionamiento
	  
	  

##  Apuntador Urgente
Especifica donde terminan los datos urgentes contenidos en la carga util del segmento que debenser entregados antes que los datos normales al proceso destino (Comando durante transferencia FTP)  //oobinline



![[IMG_20250828_093128.jpg]]