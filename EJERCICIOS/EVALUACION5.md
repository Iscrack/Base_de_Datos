## Práctica 9.
### Operaciones en una base de datos.
Objetivo: Demostrar las operaciones que se realizan en una base de datos, aplicar el modelo relacional y el lenguaje SQL

Evaluación: Para poder tener correcto cada ejercicio deberán de mostrar el resultado que se da en cada respuesta.

Lista el nombre de todos los productos que hay en la tabla producto.


1. Lista los nombres y los precios de todos los productos de la tabla producto.
**SELECT nombre_prod, precio
**FROM producto;

![image](https://user-images.githubusercontent.com/99224635/178092345-47266f6d-48de-4583-adc6-81ec00c2acd7.png)



2. Lista todas las columnas de la tabla producto.
**SELECT*
**FROM producto;

![image](https://user-images.githubusercontent.com/99224635/178092354-7e9e3ed6-a753-4250-afdf-36b0a1d871fe.png)



3. Devuelve una lista con el nombre del producto, precio y nombre de fabricante de
todos los productos de la base de datos.
**SELECT nombre_prod, precio, nombre_fab
**FROM producto INNER JOIN fabricante ON fabricante.nombre_fab = producto.nombre_fab1; 

![image](https://user-images.githubusercontent.com/99224635/178092370-0e0547b6-f887-4e3d-b793-7c2cb5b358cb.png)



Subconsultas (En la cláusula WHERE)
1. Devuelve todos los productos del fabricante Lenovo. (Sin utilizar INNER
JOIN).
**SELECT nombre_prod, nombre_fab1
**FROM producto
**WHERE nombre_fab1 = 'LENOVO';

![image](https://user-images.githubusercontent.com/99224635/178092410-035deada-7a01-4938-879a-7bc52ed826bc.png)



2. Devuelve todos los datos de los productos que tienen el mismo precio que el
producto más caro del fabricante Lenovo. (Sin utilizar INNER JOIN).
**SELECT *
**FROM producto 
**WHERE nombre_fab1 <> 'LENOVO' AND precio = (SELECT MAX(precio) FROM producto WHERE nombre_fab1 = 'LENOVO');

![image](https://user-images.githubusercontent.com/99224635/178092436-32c06113-bcb6-4be3-be48-e8ab507eb5ab.png)



3. Lista el nombre del producto más caro del fabricante Lenovo.
**SELECT nombre_prod, MAX (precio), nombre_fab
**FROM producto INNER JOIN fabricante ON fabricante.nombre_fab = producto.nombre_fab1
**WHERE precio = (SELECT MAX (precio) FROM producto WHERE nombre_fab1 = 'LENOVO')
**GROUP BY (codigo_prod);
![image](https://user-images.githubusercontent.com/99224635/178092454-a424f558-67e0-4c64-ac40-60d924640278.png)


https://www.db-fiddle.com/f/7NeGqjyLxKKDtu9uefS7mC/7
