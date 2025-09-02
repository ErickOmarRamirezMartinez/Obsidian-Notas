![[Pasted image 20250408192311.png]]
	Nos metemos a Sactrans (239)

Nos metemos a la ruta /aplic/prod/procesadores/getnet/ent

```` shell
cd /aplic/prod/procesadores/getnet/ent
````
```
```
Y checamos cuales estan vacias y cuales no
Y las que no las descargamos
![[Imagen de WhatsApp 2025-04-08 a las 19.08.32_3ae5438c.jpg]]

Las 330.000 Son las vacias, por lo que solamente tomaremos estas


![[Pasted image 20250408192620.png]]

Las descargamos y las cargamos aqui , (LA FECHA DEL DIA DE HOY)
/export/home/ent/ABR_04 en PMT (233)

```` shell

cd /export/home/ent/JUL_07

````
```
```
![[Pasted image 20250408192648.png]]
![[Pasted image 20250408192743.png]]

Despues nos metemos a esta ruta
 $SCRIPT

```` shell
cd $SCRIPT
````
```
```

Y basandonos en el nombre de nuestros archivos ejecutaremos estos comandos 
   2.2 Ejecutar el proceso de carga; $SCRIPT
        EXECS010.sh 20241129 1661241129_004 1661
        EXECS010.sh 20241129 1916241129_002 1916
      Carga de todos los cortes 01,02,03,04 siempre y cuando tenga informacion la fuente

EXECS010.sh 20250408 1661250408_004 1661
EXECS010.sh 20250408 1916250408_003 1916
EXECS010.sh 20250408 1661250408_003 1661


![[Pasted image 20250408192933.png]]


Despues de ejecutar, debemos meternos a la base de datos y confirmar si no tenemos transacciones rechazadas

![[Pasted image 20250408195052.png]]

![[Pasted image 20250408195109.png]]

![[Pasted image 20250408195128.png]]

![[Pasted image 20250408195211.png]]

Como veemos que tenemos una transaccion invalida
La tendremos que hacer manualmente 

![[Pasted image 20250408200614.png]]

![[Pasted image 20250408200629.png]]

![[Pasted image 20250408200736.png]]

Y hacemos el query 
Y checamos siempre, que coincidan el FIID de error y el REJEC_Value

E Hacemos el Insert
![[Pasted image 20250408203620.png]]



Y tenemos que ver que coincidan BIT_FECHA en ambas consultas

Ahora tenemos que depurar la carga
![[Pasted image 20250408213033.png]]

CZLDDF01.sh 1661250624_004


---
Compensa 
Te metes a la ruta $HOME


![[Pasted image 20250409195457.png]]

![[Pasted image 20250409195553.png]]

---
Replica
![[Pasted image 20250409203412.png]]

27 apartir de las 7


---
Generamos Archivos
cd /aplic/prod/pmt/adq/shell/

ksh -x PMTGADQB999G02 20250410 0346 1919
ksh -x PMTGADQB999G02 20250410 0346 1918
ksh -x PMTGADQB999G02 20250410 1019 1897
ksh -x PMTGADQB999G02 20250410 0346 1663

EXECS005.sh 01 20250422 I1664.B0346ADQ.TXS 0000001664 /aplic/prod/pmt/out/adq
EXECS005.sh 01 20250422 I1665.B0346ADQ.TXS 0000001665 /aplic/prod/pmt/out/adq
EXECS005.sh 01 20250422 I1917.B1019ADQ.TXS 0000001917 /aplic/prod/pmt/out/adq
EXECS005.sh 01 20250422 I1997.B1019ADQ.TXS 0000001997 /aplic/prod/pmt/out/adq
EXECS005.sh 01 20250422 I2004.B0346ADQ.TXS 0000002004 /aplic/prod/pmt/out/adq




Se generan en esta ruta
/aplic/prod/pmt/out/adq