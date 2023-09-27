Nuestro proyecto que busca gestionar de manera efectiva y eficiente los préstamos realizados por instituciones finanieras y prestamistas individuales, a través de un software de última generación proporcionando una visión integral y detallada de los préstamos realizados.

Para esto se creo un código en Kotlin con IntelliJ IDEA en el cuál se muestra los temas vistos de Pilas y Colas.


IMPLEMENTACIÓN DE COLAS PARA SOLICITAR UN PRÉSTAMO Y VISUALIZAR LOS PRÉSTAMOS PENDIENTES

Primero debemos tener las librerías necesarias para que el código funcione correctamente. En este caso: 

-LinkedList: la implementamos para mantener el seguimiento de las solicitudes de los préstamos pendientes como una cola, permitiendo que los elementos se agreguen al final de la cola y se puedan quitar del principio de la cola, según el orden de llegada de las solicitudes.

-SimpleDateFormat: permite el formateo y procesamiento de datos, convierte un objeto de fecha a un formato de fecha de cadena.

-Date: ya que la fecha se almacena como un objeto, permite que están sean manipuladas y formateadas.


![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/assets/87994943/df371136-3439-46a0-972e-984fbb4fdd43)

Después creamos los objetos de Deudor, que tiene como atributos el nombre del deudor y el número de documento; y el objeto Préstamo, que tiene como atributos un deudor de tipo Deudor, la cantidad del préstamo, la fecha de solicitud del préstamo, la cantidad de cuotas para realizar el pago y el tipo de cuota. 


![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/assets/87994943/7d4c6d53-9c80-4ff1-b935-ad735ce6bf2e)


