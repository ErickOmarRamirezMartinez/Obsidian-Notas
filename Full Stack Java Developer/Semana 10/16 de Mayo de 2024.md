![[Pasted image 20240516095857.png]]
![[Pasted image 20240516100835.png]]
Estas opciones van a ejecutar el codigo 


```
-- comentarios de una sola linea

/*
	Comentarios Multilinea 
*/

```


## Crear base de datos

```
CREATE DATABASE ch39;
```

![[Pasted image 20240516101435.png]]
![[Pasted image 20240516103647.png]]
![[Pasted image 20240516103935.png]]
![[Pasted image 20240516110538.png]]
![[Pasted image 20240516120058.png]]
![[Pasted image 20240516120202.png]]
![[Pasted image 20240516120223.png]]
![[Pasted image 20240516120236.png]]
![[Pasted image 20240516120252.png]]


```png
-- MySQL Workbench Forward Engineering

SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0;
SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0;
SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='ONLY_FULL_GROUP_BY,STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION';

-- -----------------------------------------------------
-- Schema mydb
-- -----------------------------------------------------

-- -----------------------------------------------------
-- Schema mydb
-- -----------------------------------------------------
CREATE SCHEMA IF NOT EXISTS `mydb` DEFAULT CHARACTER SET utf8 ;
USE `mydb` ;

-- -----------------------------------------------------
-- Table `mydb`.`Clientes`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `mydb`.`Clientes` (
  `id_clientes` INT NOT NULL AUTO_INCREMENT,
  `nombre` VARCHAR(80) NOT NULL,
  `correo` VARCHAR(250) NOT NULL,
  `direccion` VARCHAR(45) NOT NULL,
  PRIMARY KEY (`id_clientes`))
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `mydb`.`Detalles_Pedido`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `mydb`.`Detalles_Pedido` (
  `id_Detalles_Pedido` INT NOT NULL,
  `cantidad` INT NOT NULL,
  `precio_unitario` INT NOT NULL,
  `descuento` DECIMAL(10,2) NOT NULL,
  PRIMARY KEY (`id_Detalles_Pedido`))
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `mydb`.`Pedidos`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `mydb`.`Pedidos` (
  `Id_pedidos` INT NOT NULL AUTO_INCREMENT,
  `fecha` DATE NOT NULL,
  `estado_pedido` VARCHAR(255) NOT NULL,
  `total` DECIMAL(10,2) NOT NULL,
  `Clientes_id_clientes` INT NOT NULL,
  `Detalles_Pedido_id_Detalles_Pedido` INT NOT NULL,
  PRIMARY KEY (`Id_pedidos`),
  INDEX `fk_Pedidos_Clientes_idx` (`Clientes_id_clientes` ASC) VISIBLE,
  INDEX `fk_Pedidos_Detalles_Pedido1_idx` (`Detalles_Pedido_id_Detalles_Pedido` ASC) VISIBLE,
  CONSTRAINT `fk_Pedidos_Clientes`
    FOREIGN KEY (`Clientes_id_clientes`)
    REFERENCES `mydb`.`Clientes` (`id_clientes`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION,
  CONSTRAINT `fk_Pedidos_Detalles_Pedido1`
    FOREIGN KEY (`Detalles_Pedido_id_Detalles_Pedido`)
    REFERENCES `mydb`.`Detalles_Pedido` (`id_Detalles_Pedido`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION)
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `mydb`.`Productos`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `mydb`.`Productos` (
  `id_productos` INT NOT NULL AUTO_INCREMENT,
  `nombre` VARCHAR(80) NOT NULL,
  `descripcion` TEXT(300) NOT NULL,
  `precio` DECIMAL(10,2) NOT NULL,
  `stock` INT NOT NULL,
  `total` DECIMAL(10,2) UNSIGNED NOT NULL,
  `Detalles_Pedido_id_Detalles_Pedido` INT NOT NULL,
  PRIMARY KEY (`id_productos`),
  INDEX `fk_Productos_Detalles_Pedido1_idx` (`Detalles_Pedido_id_Detalles_Pedido` ASC) VISIBLE,
  CONSTRAINT `fk_Productos_Detalles_Pedido1`
    FOREIGN KEY (`Detalles_Pedido_id_Detalles_Pedido`)
    REFERENCES `mydb`.`Detalles_Pedido` (`id_Detalles_Pedido`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION)
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `mydb`.`Categoria`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `mydb`.`Categoria` (
  `id_Categoria` INT NOT NULL,
  `nombre` VARCHAR(80) NOT NULL,
  `descripcion` VARCHAR(300) NOT NULL,
  `fecha_creacion` VARCHAR(45) NOT NULL,
  PRIMARY KEY (`id_Categoria`))
ENGINE = InnoDB;


-- -----------------------------------------------------
-- Table `mydb`.`Productos_has_Categoria`
-- -----------------------------------------------------
CREATE TABLE IF NOT EXISTS `mydb`.`Productos_has_Categoria` (
  `Productos_id_productos` INT NOT NULL,
  `Categoria_id_Categoria` INT NOT NULL,
  PRIMARY KEY (`Productos_id_productos`, `Categoria_id_Categoria`),
  INDEX `fk_Productos_has_Categoria_Categoria1_idx` (`Categoria_id_Categoria` ASC) VISIBLE,
  INDEX `fk_Productos_has_Categoria_Productos1_idx` (`Productos_id_productos` ASC) VISIBLE,
  CONSTRAINT `fk_Productos_has_Categoria_Productos1`
    FOREIGN KEY (`Productos_id_productos`)
    REFERENCES `mydb`.`Productos` (`id_productos`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION,
  CONSTRAINT `fk_Productos_has_Categoria_Categoria1`
    FOREIGN KEY (`Categoria_id_Categoria`)
    REFERENCES `mydb`.`Categoria` (`id_Categoria`)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION)
ENGINE = InnoDB;


SET SQL_MODE=@OLD_SQL_MODE;
SET FOREIGN_KEY_CHECKS=@OLD_FOREIGN_KEY_CHECKS;
SET UNIQUE_CHECKS=@OLD_UNIQUE_CHECKS;

```

![[Pasted image 20240516120343.png]]

![[Pasted image 20240516120501.png]]

![[Pasted image 20240516121343.png]]

![[Pasted image 20240516121358.png]]
![[Pasted image 20240516121417.png]]
![[Pasted image 20240516121541.png]]


> Eliminamos mydb y rem,plasamos con nuestra base de datos

![[Pasted image 20240516121914.png]]
![[Pasted image 20240516122158.png]]

![[Pasted image 20240516122452.png]]


```png

```