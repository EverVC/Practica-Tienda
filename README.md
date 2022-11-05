# Practica-Tienda

EL SISTEMA CONSISTE EN APLICAR CONOCIMIENTOS BÁSICOS DE BASES DE DATOS (CRUD) EN UN FORMULARIO DE JAVA CON LOS SIGUIENTES REQUERIMIENTOS:

1 -> DEBE PERMITIR AGREGAR UN NUEVO PRODUCTO A LA BASE DE DATOS.
2 -> DEBE PERMITIR ACTUALIZAR EL NOMBRE DEL PRODUCTO.
3 -> DEBE PERMITIR ELIMMINAR UN PRODUCTO DE LA BASE DE DATOS.
4 -> MOSTRAR LISTADO DE PRODUCTOS EN UNA TABLA.
5 -> DEBE PERMITIR AGREGAR UN NUEVO PROVEEDOR BASE DE DATOS.
6 -> DEBE PERMITIR ELIMINAR UN PROVEEDOR DE LA BASE DE DATOS.
7 -> MOSTRAR LISTADO DE PROVEEDORES EN UNA TABLA.


CREE UNA BASE DE DATOS EN PostgreSQL con el nombre: db_tienda.

LUEGO CREAR LAS SIGUIENTES TABLAS:

-- TABLA 'PROVEEDOR'
CREATE TABLE tbl_proveedor(
	idproveedor SERIAL PRIMARY KEY,
	nombreproveedor VARCHAR(100)
);

-- TABLA 'PRODUCTO'
CREATE TABLE tbl_producto(
	idproducto SERIAL PRIMARY KEY,
	nombreproducto VARCHAR(100),
	precio NUMERIC(10,2),
	idproveedor INT, -- CLAVE FORANEA (RELACION CON LA TABLA PROVEEDOR)
	
	CONSTRAINT fk_producto FOREIGN KEY (idproveedor) REFERENCES tbl_proveedor(idproveedor)
);


-> IMAGENES DEL SISTEMA <-

[![Inicio-Form-Principal.jpg](https://i.postimg.cc/3N8JZ3p5/Inicio-Form-Principal.jpg)](https://postimg.cc/ftPNznBB)

![Inicio_Form_Secundario](https://user-images.githubusercontent.com/102596002/200101007-0aa5d4f0-02f1-45cb-b8d6-c2c844a827b7.jpg)

