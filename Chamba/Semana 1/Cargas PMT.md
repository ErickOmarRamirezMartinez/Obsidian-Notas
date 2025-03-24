passdword:
```
$1]RH3l9kYg&qRO-0bq3:ZZlnX
```


PASO #1
1-. Validar la existencia de las fuentes 1661 y 1916 en el Dominio Sactrans (239)
    Llegan en la ruta /aplic/prod/procesadores/getnet/ent

2-. Carga de Archivos 1661 en PMT (233)

   2.1 Pasar las Ftes del sactrans a PMT. /export/home/ent/AGO_11
   2.2 Ejecutar el proceso de carga; $SCRIPT
        EXECS010.sh 20241129 1661241129_004 1661
        EXECS010.sh 20241129 1916241129_002 1916
      Carga de todos los cortes 01,02,03,04 siempre y cuando tenga informacion la fuente
   2.3 Validar que no quede ninguna Txs rechazada en la tabla PRSA_REJECTED_TXN en PMT
   2.4 Si no esta dado de alta el comercio, incluirlo manual, tomando como ejemplo un comercio ligado a la fiid P346.
   2.5 Compensar la ftes previamente cargadas con el ciclo 26. $HOME COMPENSA
   2.6 Hacer la replica de las Txs a las tablas PRSA_TXN_ACEPTADAS y PRSA_AGENCIAS_VIAJES. - PROCEDIMIENTOS
   2.7 Teniendo la informacion del punto anterior, se puede generar el Posre 1663.

### Generar archivos ####
cd /aplic/prod/pmt/adq/shell/
ksh -x PMTGADQB999G02 20241128 0346 1663
ksh -x PMTGADQB999G02 20241128 1019 1897
ksh -x PMTGADQB999G02 20241128 0346 1918
ksh -x PMTGADQB999G02 20241128 0346 1919

EXECS010.sh 20230811 1661230811_002 1661

EXECS010.sh 20230609 1662230615_003 1662	

EXECS010.sh 20230811 1916230811_001 1916

EXECS010.sh 20230609 1963230609_001 1963

EXECS005.sh  01 20241209 I1723.B0741EMI.TXS 0000001723 /aplic/prod/pmt/out/emi

[[Prosa]]

EXECS005.sh 01 20241211 I1723.B0741EMI.TXS 0000001723 /aplic/prod/pmt/out/emi
