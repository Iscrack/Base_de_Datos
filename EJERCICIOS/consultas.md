En la BD utilizada en clase realiza las siguientes consultas:

* La tabla empleado
**USE editorial;
** SELECT *
** FROM empleados;


* Los titulos de las revistas
** SELECT titulo
** FROM revista;


* Los nombres, apellidos y especialidad de los periodostas
** SELECT nombre_periodista, apellidos_periodista, especialidad
** FROM periodistas;


* Muestra los empleados que estan en x sucursal
** SELECT nombre_empleado,codigo_de_sucursal
** FROM empleados INNER JOIN sucursal ON sucursal.codigo_de_sucursal = empleados.codigo_de_sucursal1;


* Muestra que periodistas colaboraron en x revista y en que sucursal se publico la revista
** SELECT nombre_periodista,apellidos_periodista,titulo,codigo_de_sucursal
** FROM sucursal INNER JOIN revista INNER JOIN periodistas
** WHERE titulo = 'POLITICA HOY' AND codigo_de_sucursal = 1;


* Mustra que seccion esta en x revista, en que sucursal se imprimio y que empleados estan en esa sucursal.
** SELECT id,titulo_revista,codigo_de_sucursal,nombre_empleado,apellidos_empleado
** FROM secciones INNER JOIN revista ON revista.numero_de_registro = secciones.numero_de_registro3 INNER JOIN publican ON publican.numero_de_registro1 = revista.numero_de_registro INNER JOIN sucursal ON sucursal.codigo_de_sucursal = publican.codigo_de_sucursal2 INNER JOIN empleados ON empleados.codigo_de_sucursal1 = sucursal.codigo_de_sucursal;


* En la tabla peridistas muestra solo los que escriban sobre cine
** SELECT nombre_periodista, apellidos_periodista, especialidad
** FROM periodistas
** WHERE especialidad = 'CINE';


* De la tabla revistas muestra las que sean de publicacion quincenal
** SELECT periodicidad, titulo_revista,tipo
** FROM revista
** WHERE periodicidad = 'QUINCENAL';


* Muestra el nombre de ka revista que se hayan impreso despues del 30 de septiembre del 2021
** SELECT fecha, titulo_revista, numero_de_registro, titulo_revista
** FROM revista INNER JOIN ejemplares ON ejemplares.numero_de_registro4 = revista.numero_de_registro
** WHERE fecha > 2021-09-30;

* Muestra el nombre de la revista que se haya publicado en la sucursal 1 cuyos ejemplares tengan más de 80 páginas.
** SELECT titulo_revista, codigo_de_sucursal, numero_de_paginas
** FROM ejemplares INNER JOIN revista ON ejemplares.numero_de_registro4 = revista.numero_de_registro INNER JOIN publican ON publican.numero_de_registro1 = revista.numero_de_registro INNER JOIN sucursal ON sucursal.codigo_de_sucursal = publican.codigo_de_sucursal2
** WHERE codigo_de_sucursal=1;


https://www.db-fiddle.com/f/iAUjGLoFoHtam2pK68Xh1B/1

https://www.db-fiddle.com/f/iAUjGLoFoHtam2pK68Xh1B/19
