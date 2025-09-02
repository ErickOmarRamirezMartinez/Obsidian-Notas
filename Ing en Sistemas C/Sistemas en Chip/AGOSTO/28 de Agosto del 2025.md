## MOS6502

[MOS 6502 - Wikipedia, la enciclopedia libre](https://es.wikipedia.org/wiki/MOS_6502)
### Modos de direccionamiento
Es la forma en que 
- _implied_ (instrucciones de 1 byte)
- _absolute_ (3 bytes)
- _relative_ (2 bytes)
- _acumulador_ (1 byte)
- _indirect, x_ e _indirect, y_ (2 bytes)
- _immediate_ (2 bytes)
- _indexado, X_ e _indexado, Y_ (2 o 3 bytes, dependiendo de que la base esté en la página cero o no)

![[Pasted image 20250828072556.png]]

Del 33 al 26, son Bus de datos bidireccional 

34
Red/Write

De A0 a A15, Son de Bus de Direcciones unidireccional (Salidas)
Al tener 16 bits (2^16=65536)



VCC 8 - 
VSS 1 y 21 - Es Tierra

NC 5 , 35 y 36  No tienen ninguna funcion 

PI 0 , 1 y 2 en 3 , 37 y 39
Son Salidas Reloj

8
SYNC 
Detiene las señales 

2
RDY
Es un indicador que ya termino la instruccion 

38
S0
Set Overflow
Restablece el sobreflujo


>CRC = Registro de codigo de verificacion 

El microprocesador es una maquina de estados y debe tener una señal de reloj para poder pasar al estado siguiente 

RES -> Reset
NMI -> Interrupcion no Mascorable
IRQ -> Solicitud de peticion de interrupcion 

---
