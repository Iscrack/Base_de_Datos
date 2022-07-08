## Práctica 9.
### Operaciones en una base de datos.
Objetivo: Demostrar las operaciones que se realizan en una base de datos, aplicar el modelo relacional y el lenguaje SQL

Evaluación: Para poder tener correcto cada ejercicio deberán de mostrar el resultado que se da en cada respuesta.

Lista el nombre de todos los productos que hay en la tabla producto.


1. Lista los nombres y los precios de todos los productos de la tabla producto.
**SELECT nombre_prod, precio
**FROM producto;


2. Lista todas las columnas de la tabla producto.
**SELECT*
**FROM producto;


3. Devuelve una lista con el nombre del producto, precio y nombre de fabricante de
todos los productos de la base de datos.
**SELECT nombre_prod, precio, nombre_fab
**FROM producto INNER JOIN fabricante ON fabricante.nombre_fab = producto.nombre_fab1; 


Subconsultas (En la cláusula WHERE)
1. Devuelve todos los productos del fabricante Lenovo. (Sin utilizar INNER
JOIN).
**SELECT nombre_prod, nombre_fab
**FROM producto LEFT JOIN fabricante ON fabricante.nombre_fab = producto.nombre_fab1
**WHERE nombre_fab = 'LENOVO';


2. Devuelve todos los datos de los productos que tienen el mismo precio que el
producto más caro del fabricante Lenovo. (Sin utilizar INNER JOIN).



3. Lista el nombre del producto más caro del fabricante Lenovo.


https://www.db-fiddle.com/f/7NeGqjyLxKKDtu9uefS7mC/6
