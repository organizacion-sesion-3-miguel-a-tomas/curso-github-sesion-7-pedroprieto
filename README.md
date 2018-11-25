# sesion7-tarea-individual
Tarea GitHub Classroom Sesión 7
# Ejercicio evaluable: Manejo de Ficheros

Para el tema de manejo de ficheros se va a implementar la gestión basada en ficheros de los empleados de una empresa a través de una aplicación en modo consola.

De los empleados se guardarán los siguientes datos:

* ID de empleado - Entero

* Apellido - Array de 16 caracteres.

* Departamento - Entero

* Salario - Número fraccionario de doble precisión

Teniendo en cuenta estos datos se necesita implementar las siguientes funcionalidades:

1. Inserción de un empleado en un fichero aleatorio.

2. Consulta de los datos de un empleado en un fichero aleatorio.

3. Inserción de los datos de empleados a partir de un fichero de texto (CSV)

4. Modificación de los datos de un empleado.

5. Borrado de un empleado.

6. Imprimir por pantalla un listado de los empleados insertados.

7. Exportar todos los empleados a un fichero XML utilizando DOM

8. Crear una Clase Empleado y serializar todos los empleados a XML utilizando JAXB.

A continuación, se detallan las particularidades de las funciones anteriormente mencionadas.

1. Inserción de Empleados.

Para insertar un empleado se debe calcular la posición donde irá guardado el empleado dentro del fichero a partir del ID del empleado. Hay que tener en cuenta que mientras que los empleados comenzarán a partir del ID 1 el fichero tiene el puntero al inicio en la posición 0. También hay que considerar que el empleado ya esté introducido dentro del fichero.

Para calcular el tamaño de los datos de un empleado hay que notar que en Java, el tipo entero ocupa 4 bytes, cada caracter ocupa 2 bytes y el tipo flotante de doble precisión ocupa 8 bytes. A partir de estos datos será posible realizar el cálculo de la posición donde el empleado va insertado dentro del fichero.

2. Consulta de un empleado.

Para consultar los datos de un empleado tenemos que recibir por pantalla el identificador del empleado del que queremos mostrar su información y acudir a la posición donde se guardan sus datos y mostrarlos.

En esta función tendremos que comprobar que el usuario existe y si no es así deberemos mostrar un mensaje por pantalla indicándolo.

3. Insertar empleados desde CSV.

Un fichero CSV es un fichero de texto plano donde los valores van separados por comas. A través de un fichero que se puede crear fácilmente con una hoja de cálculo se leerán los valores y se insertarán de forma masiva en el fichero aleatorio.

4. Modificar datos de empleados.

En la modificación de datos ofreceremos la posibilidad al usuario de modificar los datos de un empleado excepto el identificador que será permanente y indicará la posición del usuario dentro del fichero.

5. Borrado de un empleado.

Para borrar un empleado se establecerán en el fichero una serie de caracteres que indiquen que el empleado ha sido borrado. Así, podemos establecer el ID a -1, rellenar con 0 el nombre, establecer a 0 tanto el departamento como el salario del empleado.

6. Imprimir listado de empleados.

En esta funcionalidad se recorrerá secuencialmente el fichero y se mostrarán todos aquellos empleados insertados en el mismo. Se ha de considerar, que puedan existir empleados que han sido borrados.

7. Exportar a XML con DOM.

Utilizando la interfaz DOM proporcionada por Java se exportarán todos aquellos empleados que estén guardados en el fichero aleatorio a XML.

8. Serializar la Clase Empleado a XML utilizando JAXB.

Para serializar una clase mediante JAXB a XML tenemos que definir la Clase Empleado en un nuevo fichero con los datos anteriormente mencionados. A partir de esta clase se creará otra clase que podemos llamar ListaEmpleados que representará mediante un ArrayList el conjunto de empleados que tenemos guardado en el fichero aleatorio, además de un nombre de la empresa y la localización. La serialización de un objeto ListaEmpleados convertirá el nombre de la empresa junto con el conjunto de sus empleado a una representación XML. 



