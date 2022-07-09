## Práctica 8.
### Disparadores (Triggers)

Objetivo: Demostrar las operaciones que se realizan en una base de datos.

Ejercicio: Crea una base de datos llamada test que contenga una tabla llamada
alumnos con las siguientes columnas. (valor 18)

Evaluación:

Creación de la base de datos : 9 puntos.

Creación de los Disparadores(Triggers): 9 puntos.

Tabla alumnos:

● id (entero sin signo)

● nombre (cadena de caracteres)

● apellido1 (cadena de caracteres)

● apellido2 (cadena de caracteres)

● nota (número real)

Una vez creada la tabla escriba dos triggers con las siguientes características:

● Trigger 1: trigger_check_nota_before_insert

  o Se ejecuta sobre la tabla alumnos.
  
  o Se ejecuta antes de una operación de inserción.
  
  o Se almacena la leyenda 'se ingreso un registro'

● Trigger2 : trigger_check_nota_before_update
  o Se ejecuta sobre la tabla alumnos.
  
  o Se ejecuta antes de una operación de actualización.
  
  o Se ingresa la leyenda 'se modifico un regisstro'
  
Una vez creados los triggers escribe varias sentencias de inserción y actualización
sobre la tabla alumnos y verifica que los triggers se están ejecutando
correctamente.

![image](https://user-images.githubusercontent.com/99224635/178095226-b0fd5ca7-d567-46c6-a954-919c6bd6f2a4.png)

![image](https://user-images.githubusercontent.com/99224635/178095263-6b1c8d56-ac05-4144-87db-25135f17635a.png)

![image](https://user-images.githubusercontent.com/99224635/178095286-ed1f19c7-092a-4ba1-8570-24c0a87e26b5.png)



https://www.db-fiddle.com/f/efM3KozCwgzMYRy4z2QRBR/2
