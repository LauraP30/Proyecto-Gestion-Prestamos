La Plataforma de Análisis Financiero para Préstamos propone una solución tecnológica avanzada que fusiona desarrollo de software y gestión financiera. Ofrece una visión detallada de la salud financiera de los préstamos, con una interfaz intuitiva y herramientas de análisis sofisticadas. El proyecto aborda desde la definición de requisitos hasta la implementación técnica, priorizando escalabilidad, seguridad y accesibilidad. El objetivo es empoderar a instituciones financieras y prestamistas individuales para mejorar la toma de decisiones y eficiencia operativa, marcando un hito en la gestión de préstamos.


IMPLEMENTACIÓN DEL PROYECTO EN KOLTIN  

DATA CLASS USUARIO

Se crea la data class Usuario con sus respectivos atributos nombre, email, celular, y contraseña.   

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/1.png?raw=true) 
 
Se utiliza companion object para definir los métodos y propiedades estáticas que pertenecen a la clase Usuario.  

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/2.png?raw=true)  

- Se declara un valor de registroUsuario que se utiliza para almacenar los usuarios registrados en una lista. 

- Se declara una variable de usuario que puede ser null si no hay un usuario registrado. 

Se declara la función inicioSesion con los parámetros de email y contraseña ambos de tipo String y devuelve un valor Boolean de true si encuentra al usuario y false en caso contrario. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/3.png?raw=true) 

Se declara la funcion registroUser con los parámetros nombre, email, celular y password todos de tipo String; que agrega un nuevo usuario al registroUsuario con su información. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/4.png?raw=true) 

Se declara la funcion datos con el parámetro de user de tipo Usuario, que imprime la información del usuario. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/5.png?raw=true) 

Se declara la función editarUsuarioExistente(), que permite editar la información de usuario; para esto solicita un correo electrónico, busca el usuario, solicita los nuevos datos y actualiza la información. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/6.png?raw=true) 

Se declara la funcion eliminarCuenta con el parametro emailAEliminar de tipo String, que permite eliminar la cuenta del usuario. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/7.png?raw=true) 

Se declara la funcion para acceder solo a ella en la clase Usuario de private fun editarUsuario con los parámetros de nuevoNombre, nuevoEmail, nuevoCelular y nuevaContraseña todas de tipo String que se utiliza para realizar la edición de la información del usuario. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/8.png?raw=true) 


DATA CLASS PRESTAMO

Se importan las librerías necesrias para la clase.

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/9.png?raw=true) 

Se declara la data class Prestamo() con sus respectivos atributos nombreD, correoD, numeroD, direccion, cantidad, fecha, cuotas, tipo, y estado.  

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/10.png?raw=true) 

Se declara la función obtenerEstadoActual() que devuelve un dato de tipo String el cual es el estado actual del préstamo en función de la fecha actual}, devolviendo un estado como "Por Pagar", "Vencido" o "Reportado". 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/11.png?raw=true) 

Se utiliza companion object para definir los métodos y propiedades estáticas que pertenecen a la clase Prestamo.  

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/12.png?raw=true) 

- Se declara un valor prestamos que almacena los préstamos registrados en una lista. 

- Se declara un valor prestamosPorPagar que almacena los préstamos que aún están por pagar en una cola (Queue). 

Se declara la funcion solicitarPrestamo(), que permite al Usuario registrar un préstamo, recopilando la información del deudor; crea una nueva instancia de Prestamo y la agrega tanto a la lista préstamos y a la cola de préstamos por pagar. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/13.png?raw=true) 

Se declara la funcion calcularPorcentajeInteres(), con los parámetros de montoPrestamo de tipo Double; y cuotas de tipo Int, devolviendo un dato de tipo Double, calculando el porcentaje de interés basado en el monto del préstamo y el número de cuotas.  

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/14.png?raw=true) 

Se declara la funcion calcularProximaFechaPago con los parámetros de fechaActual y tipoCuota ambos de tipo String y devuelve un dato de tipo Date, que calcula la próxima fecha de pago basada en la fecha actual y el tipo de cuota (mensual, quincenal, anual). 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/15.png?raw=true) 

Se declara la funcion calcularFechaVencimiento() con los parámetros de fechaActual de tipo String y meses de tipo Int, devolviendo un dato de tipo String, que calcula la fecha de vencimiento sumando un número dado de meses a la fecha actual. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/16.png?raw=true) 

Se define la funcion mostrarPrestamos(), que muestra la información de los préstamos registrados, el interés, el total a pagar y la próxima fecha de pago para cada préstamo. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/17.png?raw=true) 


DATA CLASS PREGUNTA

Se crea la data class Pregunta() con sus respectivos atributos de pregunta y fechaP ambos de tipo String. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/18.png?raw=true) 

Se declara la class Foro, que utiliza un companion object para definir propiedades y funciones de nivel de clase. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/19.png?raw=true) 

- Se declara el valor de preguntas, que almacena las preguntas realizadas en el foro en una lista.

Se declara la función hacerPregunta() que permite al usuario ingresar una pregunta (con la fecha actual y hora), crea una nueva instancia de Pregunta y la agrega a la lista de preguntas. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/20.png?raw=true) 

Se declara la función verPreguntas() que muestra la información de las preguntas realizadas (texto de la pregunta y la fecha en que fue realizada) y en caso de que no haya ninguna pregunta se imprime un mensaje indicado para este caso. 



CLASS MAIN

En la clase main se emplea un bucle while (true) para mantenerse en ejecución hasta que el usuario elige salir. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/21.png?raw=true) 

- En este caso tendriamos el menú principal con las opciones de Iniciar Sesión, Crear Cuenta, y Salir. 

- Opción 1 - Iniciar Sesión, solicita al usuario que ingrese su correo electrónico y contraseña; y utiliza la función Usuario.inicioSesion para verificar si las credenciales son correctas; si el inicio de sesión es exitoso, se presenta un nuevo menú con opciones relacionadas con préstamos, gráficas, configuración y preguntas.

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/22.png?raw=true) 

- Opción 1 - Préstamo, solicita al usuario que escoja alguna de las opciones.  

- Opción 1 – Registrar Préstamo, utiliza la función Prestamo.solicitarPrestamo() para ingresarlos datos de un préstamo. 

- Opcion 2 – Ver Préstamos, utiliza la funcion Prestamo.mostrarPrestamos() para visualizar todos los préstamos previamente diligenciados 

- Opción 3 – Regresar al menú principal, permite volver al menu anterior.

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/23.png?raw=true) 

- Opción 3 - Configuración, solicita al usuario que escoja alguna de las opciones.

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/24.png?raw=true) 

- Opción 1 – Editar Datos, utiliza la función Usuario.editarUsuarioExistente() para cambiar los datos de usuario. 

- Opción 2 – Cerrar Sesión, termina por completo la ejecución del código. 

- Opción 3 – Eliminar Cuenta, utiliza la función Usuario.eliminarCuenta() para eliminar la cuenta del usuario. 

- Opción 4 – Regresar al menú principal permite volver al menú anterior.

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/25.png?raw=true) 

- Opción 4 – Preguntas, solicita al usuario que escoja alguna de las opciones.

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/26.png?raw=true) 

- Opción 1 – Realizar Pregunta, utiliza la función Foro.hacerPregunta, para ingresar las inquietudes que tenga el usuario. 

- Opción 2 – Ver Preguntas, permite visualizar todas las preguntas realizadas. 

- Opción 3 – Regresar al menu principal permite volver al menú anterior. 

- Opción 5 – Cerrar Sesión termina por completo la ejecución del código.

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/27.png?raw=true) 

- Opción 2 - Crear Cuenta, solicita al usuario que ingrese su nombre, correo electrónico, número de celular, contraseña y confirme la contraseña.

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/28.png?raw=true) 

Verifica que las contraseñas coincidan antes de registrar el usuario utilizando la función Usuario.Companion.registroUser. 

 ![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/29.png?raw=true) 

- Opción 3 – Salir, imprime un mensaje de despedida y termina la ejecución del programa. 
