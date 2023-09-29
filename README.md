La Plataforma de Análisis Financiero para Préstamos propone una solución tecnológica avanzada que fusiona desarrollo de software y gestión financiera. Ofrece una visión detallada de la salud financiera de los préstamos, con una interfaz intuitiva y herramientas de análisis sofisticadas. El proyecto aborda desde la definición de requisitos hasta la implementación técnica, priorizando escalabilidad, seguridad y accesibilidad. El objetivo es empoderar a instituciones financieras y prestamistas individuales para mejorar la toma de decisiones y eficiencia operativa, marcando un hito en la gestión de préstamos.


IMPLEMENTACIÓN DE COLAS PARA SOLICITAR UN PRÉSTAMO Y VISUALIZAR LOS PRÉSTAMOS PENDIENTES

Se deben tener las librerías necesarias para que el código funcione correctamente. En este caso: 

- LinkedList: es una implementación de una lista enlazada, que almacena datos en un orden secuencial.
- SimpleDateFormat: se utiliza para formatear y analizar fechas, el cual se especifica mediante el patrón dd/MM/yyyy.
- Date: representa una fecha y hora.

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/Librericas-colas.png?raw=true)


Definimos la clase Deudor(), que tiene como atributos el nombre  y el numeroDocumento ambos de tipo String. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/Deudor-colas.png?raw=true)


Definimos la clase Prestamo(), que tiene como atributos deudor de tipo Deudor, cantidadPrestamo de tipo Int, fechaSolicitud de tipo Date (que representa la fecha en la que se esta solicitando el préstamo), cantidadCuota de tipo Int, tipoCuota de tipo String.

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/Prestamo-colas.png?raw=true)


Creamos la clase PrestamoSolicitud() que tiene un valor private (el cual solo se puede utilizar en esa clase) solicitudesPendientes que almacena los datos en una lista LinkedList<Prestamo>(), que permite acceder a los elementos de forma secuencial de las solicitudes que estan pendientes. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/PSolicitud-colas.png?raw=true)


Se crea la función solicitarPrestamo() con el parámetro prestamo de tipo Prestamo; y que realiza las siguientes acciones:

- Agregar un nuevo prestamo al final de la cola mediante el método offer()
- Obtener la información del deudor en la posicion requerida empleando el método size (permite saber el tamaño de la lista) - 1.
- Imprime un mensaje confirmando la solicitud del préstamo "Solicitud de préstamo recibida".
- Obtener toda la información del prestamo y la posición en la que se encuentra, mediante el método obtenerInformacinPrestamo().

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/sPrestamo-colas.png?raw=true)


Se crea la función verSolicitudesPendientes(), que realiza las siguientes acciones:

- Imprime un mensaje de "Solicitudes Pendientes".
- Itera sobre la lista de solicitudes pendientes, mediante el método withIndex() que devuelve una secuencia que contiene cada elemento de la lista junto con su índice.
- Para cada solicitud de préstamo, imprime la información del préstamo mediante el método obtenerInformacionPrestamo().

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/vSPendientes-colas.png?raw=true)


Se crea la función verSolicitudEnPosicion(), con el parámetro de posicion de tipo Int, que realiza las siguientes acciones:

- Verifica si la posición especificada es o no mayor al tamaño de la lista.
  > Si la posición es válida, obtiene e imprime la información de la solicitud de préstamo de la lista.
  > Sino devuelve un mensaje de error "La posición especificada no es válida".

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/vSPosicion-colas.png?raw=true)


Se crea una función private (para acceder a ella en solo esa clase) llamada obtenerInformaciónPrestamo(), que tiene los parámetros de prestamo de tipo Prestamo, la cual imprima los datos del préstamo:

- Se crea un valor que utiliza la clase SimpleDateFormat para formatear la fecha de solicitud del préstamo.
- Imprime el nombre del deudor.
- Imprime el número de documento del deudor.
- Imprime la cantidad del préstamo.
- Imprime la fecha de solicitud del préstamo empleando SimpleDateFormat.
- Imprime la cantidad de la cuota del préstamo.
- Imprime el tipo de cuota del préstamo.

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/Informacion-colas.png?raw=true)


Se crea la función principal main(), en la cual realiza las siguientes acciones: 

- Se crea un valor gestionarPrestamo() que sera igual a la clase PrestamoSolicitud().
- Se crea tres valores de posibles Deudores tales como antonio, maria y pedro, que son de tipo Deudor con los atributos mencionados en esa clase.
- Se emplea el valor gestionarPrestamo() junto con la función solicitarPrestamo() de tipo Prestamo con los atributos mencionados en esa clase.
- Se emplea el valor gestionarPrestamo() junto con la función verSolicitudesPrendientes().
- Se emplea el valor gestionarPrestamo() junto con la función verSolicitudesEnPosicion() más la posición de la cual queremos saber la información.

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/Main-colas.png?raw=true)


Como resultado tenemos lo siguiente: 

- Las solicitudes de los Dedudores que se crearon: 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/Resultado1-colas.png?raw=true)


- Las solicitudes pendientes de los Deudores: 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/Resultado2-colas.png?raw=true)


- La información del Deudor en la posición 1, en este caso María Garcia: 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/Resultado3-colas.png?raw=true)


IMPLEMENTACIÓN DE PILAS PARA LOS PRÉSTAMOS REALIZADOS

Se deben tener las librerías necesarias para que el código funcione correctamente. En este caso: 

- SimpleDateFormat: se utiliza para formatear y analizar fechas, el cual se especifica mediante el patrón dd/MM/yyyy.
- Date: representa fechas.
- Stack: se utiliza para implementar una pila de datos, la cual sigue el principio LIFO (Last In First Out), es decir, los elementos se agregan y eliminan de la pila en orden inverso al que se agregaron.

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/Librerias-pilas.jpg.png?raw=true)


Nuevamente creamos las clases de datos Deudor y Prestamo como en la implementación de Colas, pero a la clase Prestamo se le agrega el atributo fechaPado de tipo String.

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/Deudor-Prestamo-pilas.png?raw=true)


Se crea la clase PrestamoRealizado() que tiene un valor private (el cual solo se puede utilizar en esa clase) prestamosRealizados que almacena una lista de los datos de los préstamos que ya han sido aprobados y desembolsados Stack<Prestamo>(), que permite acceder a los elementos según el principio LIFO. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/PRealizado-pilas.png?raw=true)


Se crea la función realizarPrestamo() con el parámetro prestamo de tipo Prestamo, que realiza las siguientes acciones: 

- Agrega el objeto de préstamo a la pila, mediante el método push().
- Imprime un mensaje del préstamo realizado "Préstamo realizado".
- Imprime la información del préstamo realizado mediante el método obtenerInformacionPrestamo().

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/realizarP-pilas.png?raw=true)


Se crea una función private (para acceder a ella en solo esa clase) llamada obtenerInformaciónPrestamo(), que tiene los parámetros de prestamo de tipo Prestamo, la cual imprima los datos del préstamo:

- Se crea un valor que utiliza la clase SimpleDateFormat para formatear la fecha de solicitud del préstamo.
- Imprime el nombre del deudor.
- Imprime el número de documento del deudor.
- Imprime la cantidad del préstamo.
- Imprime la fecha de solicitud del préstamo empleando SimpleDateFormat.
- Imprime la cantidad de la cuota del préstamo.
- Imprime el tipo de cuota del préstamo.
- Imprime la fecha en la cual se paga las cuotas del préstamo.

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/Informacion-pilas.png?raw=true)


Se crea la función principal main(), en la cual realiza las siguientes acciones: 

- Se crea un valor gestionarPrestamo() que sera igual a la clase PrestamoRealizado().
- Se crea un valor fechaSolicitud() que será igual a SimpleDateFormat junto con parse (que convierte la cadena que representa la fecha en un objeto Date).
- Se crea dos valores de posibles Deudores tales como antonio y pedro, que son de tipo Deudor con los atributos mencionados en esa clase.
- Se emplea dos veces el valor gestionarPrestamo() junto con la función realizarPrestamo() de los valores antonio y pedro, de tipo Prestamo con los atributos mencionados en esa clase.

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/Main-pilas.png?raw=true)


Como resultado tenemos lo siguiente: 

- Las préstamos aprobados de los Dedudores que se crearon: 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/Resultado-pilas.png?raw=true)
