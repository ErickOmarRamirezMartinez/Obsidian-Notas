![[Pasted image 20240520101511.png]]
![[Pasted image 20240520101519.png]]

---
![[Pasted image 20240520101852.png]]
![[Pasted image 20240520102128.png]]
![[Pasted image 20240520102602.png]]


```sql
-- Sintaxis para traer solamente infor de una columna en especifico
-- SELECT column_name FROM table_name

select nombre from clientes;
```
![[Pasted image 20240520102846.png]]

---
```sql
-- Sintaxis para seleccionar un atributo en especifico 
-- Select * From 
-- Where Column_name = "";

select * from clientes where nombre = "Fernanda Ramos";
```
![[Pasted image 20240520104024.png]]

---
```sql
-- Order By Ordena a partir de la columna indicada
-- Puede ser de forma ascendente y de forma descendente
-- ASC ascendente, DESC descendente

Select * from clientes order by nombre asc;
Select * from clientes order by nombre desc;
```
![[Pasted image 20240520104856.png]]
![[Pasted image 20240520104920.png]]

---
```sql
-- Nos permite mostrar las bases de datos almacenada
SHOW databases;
```

![[Pasted image 20240520105019.png]]


---
```sql
-- Mostrar las tablas que se encuentran dentro de la base de datos 
show tables;
```

![[Pasted image 20240520105133.png]]



---
```sql 
-- Sintaxis para utilizar un alias en mis columnas 
select nombre AS "name" from clientes;
```



---
```sql
-- Between (entre) Es un operador complementario para WHERE (Define el rango)

select * from detalles_pedido
where id_Detalles_Pedido between 1 and 4;

```
![[Pasted image 20240520113706.png]]

---
![[Pasted image 20240520113828.png]]
![[Pasted image 20240520113835.png]]


---
```sql
 -- Insert Into es el comando de DML que nos permite agregar nuevas filas o registros alter
 
 insert into detalles_pedido(id_Detalles_Pedido, cantidad, precio_unitario, descuento)
 VALUES (null, 15, 80, 6.00);
 
 -- Sintaxis 2
 
 insert into clientes
 values (null, "Eduardo Sosa", "edu@gmail.com", "Calle Poniente 6");
 
```

![[Pasted image 20240520115638.png]]

---

```sql
 /*
 Update vamos a poder actualizar los registros de mis columnas
 Update table_name 
 set column_name = "value"
 where unique_id = "value";
 
 */
 
 update clientes
 set nombre = "Lalo Sosa"
 where id_Cliente = 10;
 
```

![[Pasted image 20240520120338.png]]


---
![[Pasted image 20240520141715.png]]