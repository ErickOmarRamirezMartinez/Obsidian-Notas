noPaso #1  
en la ruta 
```
cd /export/home/dumpfiles/tlfs/
```


test colocar los archivos tlfs  
  
Paso #2  
renombrarlos de la siguiente manera  

EMMDD001  = este archivo es el de detalle  
CIF > R2MMDD = este archivo es de cifras

a los archivos se les dan permisos 
ponle en UNIX  
cd  
te va a mandar al HOME  
ahi le das asi  
ls -ltr **CARGA**  
y ejecutas este shell  
CARGA_TLF.sh

---
Vale, siendo asi que tu carga esta chida.!!  

Vamos a la BDD  

SELECT *  
FROM TRANSACCIONES  
WHERE FECHA_CARGA = '16/08/2023'  
  
SELECT *  
FROM TRAN_AUX  
WHERE FECHA_CARGA = '16/08/2023'

ambas consultas deben darte el mismo total de registros

SELECT *  
FROM TRANSACCIONES  
WHERE to_char(FECHA_CARGA, 'dd/mm/yyyy') = '16/08/2023'  
AND SUBSTR(NUMERO_CUENTA_ACCESO,1,8) = '45178000'

---
## ATM STAT

1-. Pasar el archivo que deja Online al servidor de RED.  
2-. Depositar los archivos en la ruta 
```
cd /export/home/dumpfiles/tlfs/test/
```
  
3-. Renombrar los archivos de la siguiente manera.  
   -20231010_atm_cifras >>> R2MMDD  donde MM = mes DD 
   -20231010_atm_stat   >>> EMMDDCCC  donde MM = mes DD = dia CCC = corte (001)
Los archivos deben de estar descomprimidos 

luego debes cargar los archivos

``` shell
cd $HOME
```

```shell
CARGA_TLF.sh
```

YYYYMMDD, YYYYMMDD-1,  YYYYMMDD-7 y el CCC (001)

#### Validar las tablas en RED  
   select *  
   from transaccciones  
   where fecha_carga = fecha de carga  
  
   select *  
   from tran_aux  
   where fecha_carga = fecha de carga

##### para generar archivos

debes ir a la siguiente ruta 
```
/aplic/prod/red/tlf/shell
```


para el stat 6 debes ejecutar el siguiente comando:

```
REDCTLFGEM6G01
```
YYYYMMDD

para el stat 7 

```
REDCTLFGEM7G01
```
YYYYMMDD


para ver los archivos se encuentran en la siguiente ruta: 
```
cd /export/home/red/tlfs/stats/STATS_EMV/
```

