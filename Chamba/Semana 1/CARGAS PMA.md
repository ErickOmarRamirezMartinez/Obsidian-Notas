### Guardar archivos de carga PMT
``` bash
cd  /export/home/ent/ABR_04
```
 agrega tambíen el día y el mes
 #NOTA Hay un limite de consecutivo para la corte, por lo cual una vez llegado debe cambiarse. por el 201,202,203.
### para hacer la carga 

Ubicación:
```bash
cd $HOME/pmt 
```

comando:
``` bash
CARGA_PTLF.sh  
```
AAAAMMDD NNN

### para depurar la carga 
-- Cuando hay en la base de datos rechazadas y se tuvieron que subir de forma manual.

ubicación:  
``` bash
cd $UUSR
```


comando:
```bahs
PMTGADMBORPV01
```
 005AAMMDD_NNN

#### COMPENSACIÓN 
comando: 
``` bash
COMPENSA_PTLF.sh
```
 

NNN AAAAMMDD

### Hacer replica PMTEXE
ubicación: 
``` bash
cd $HOME/pmt
```


comando:
``` bash
REPLICA_PTLF
```

AAAAMMDD NNN

### Generar Archivos

``` bash
cd /aplic/prod/pmt/adq/shell
```
  
``` bash
ksh -x PMTGADQB999G02 20231211 0346 1757 == 103
ksh -x PMTGADQB999G02 20231211 0346 1758 == 103
ksh -x PMTGADQB999G02 20231211 0346 1759 == 103
ksh -x PMTGADQB999G02 20231211 0346 1760
ksh -x PMTGADQB999G02 20231211 0346 1761
ksh -x PMTGADQB999G02 20231211 0346 1762
ksh -x PMTGADQB999G02 20231211 0346 1763
ksh -x PMTGADQB999G02 20231211 0346 1764
ksh -x PMTGADQB999G02 20231211 0346 1765
```

```bash
ksh -x PMTGADQB999G02 20231211 1019 1907 == 101
ksh -x PMTGADQB999G02 20231211 1019 1908 == 102
ksh -x PMTGADQB999G02 20231211 1019 1909 == 103
ksh -x PMTGADQB999G02 20231211 1019 1910
ksh -x PMTGADQB999G02 20231211 1019 1911
ksh -x PMTGADQB999G02 20231211 1019 1912
ksh -x PMTGADQB999G02 20231211 1019 1913
ksh -x PMTGADQB999G02 20231211 1019 1914
ksh -x PMTGADQB999G02 20231211 1019 1915
```
								
![[Pasted image 20250408205542.png]]


### Donde se guardan los archivos creados

ubicación: 
``` bash
cd /aplic/prod/pmt/out/adq
```

``` bash
chmod 775 *
```


---
### Generar Reportes SAC 

SICMOR0280
SICMIR0290
SICMOR0170
SICLIR0200
siccmr0060

---

#### Borra el caché de otras txt de cargas anteriores y/o duplicados
comandos: 

``` bash
cd $SCRIPT
```

```
CZDCS140.sh
```


---
#### Borrado de cliclos 
```bash
cd $UUSR
```

ejecutas este script
```bash
CZLDDC01.sh
```


con los siguientes parametros

``` bash
CZLDDC01.sh
``` 

YYYYMMDD 04

contraseña control M: Nautic@202211

120 se encarga de validar que la tsx se encuentran en la bd, este cobol hace es al momento de hacer la carga.

La replica de tsx prosa lo hace mediante ligas; 

2121, 2356, son las bu unit de genet 