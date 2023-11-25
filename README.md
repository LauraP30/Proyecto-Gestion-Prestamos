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

- La variable colaPrestamos de tipo Queue<Prestamo>, la cual se inicializa con una instancia de la clase LinkedList, que implementa la interfaz Queue, que se empleara para visualizar los préstamos solicitados. 

- La variable preguntas y se le asigna una nueva lista mutable de preguntas mutableListOf<Pregunta>(), que almacenara las preguntas realizadas por los usuarios. 

Definimos la función inicioSesion que verifica si un usuario (con un correo electrónico y contraseña) existe en el registroUsuario, que toma los parámetros: email y contraseña de tipo String, devolviendo un valor Boolean.  

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/6.jpeg?raw=true) 

- Se declara la variable user, que utiliza la función find sobre la lista registroUsuario, que busca en la lista y devuelve el primer elemento que cumple con la condición especificada dentro de las llaves {}, con la condición de que el correo electrónico (it.email) y la contraseña (it.contraseña) del usuario en la lista coincidan con los proporcionados como argumentos a la función. Esta función devuelve true si user no es nula (que encontró un usuario en registroUsuario con el correo electrónico y la contraseña proporcionados); y devuelve false si user es nulo (si no encontró ningún registro). 

Definimos la función registroUser para agregar un nuevo usuario al registroUsuario, que tiene cinco parámetros: nombre, email, celular, password, y verificationCode (todos de tipo String).  

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/7.jpeg?raw=true) 

- Dentro de la función se crea una nueva instancia de la clase Usuario con los valores proporcionados como argumentos y se emplea el método add para agregarlos a la lista. 

Se define la función datos que imprimirá en la consola la información sobre un objeto de la clase Usuario. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/8.jpeg?raw=true) 

- Se utiliza la función println para imprimir en la consola el nombre del usuario (mediante la expresión ${user.nombre}), el correo (mediante la expresión ${user.email}) y el celular (mediante la expresión ${user.celular}) 

Definimos la solicitarPrestamo, que permite al usuario (Usuario) solicite un préstamo. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/9.jpeg?raw=true) 

- Se imprime un mensaje indicando que el usuario está solicitando un préstamo, seguido de datos del usuario como nombre, correo electrónico y teléfono del usuario. 

- Se le solicita una información adicional al usuario, como la dirección, la cantidad del préstamo, la cantidad de cuotas, y el tipo de cuota (mensual, trimestral, etc.). los cuales se leen mediante la entrada estándar readLine(). 

- Se formatea la fecha actual utilizando SimpleDateFormat para tener el formato "dd-MM-yyyy". 

- Se calcula el porcentaje de interés utilizando la función calcularPorcentajeInteres. 

- Se crea un nuevo objeto Prestamo (nuevoPrestamo) con la información proporcionada por el usuario y los cálculos realizados y este se agrega a la lista prestamos mediante el método add. 

- Se imprime un mensaje indicando que el préstamo fue solicitado con éxito y se llama a la función visualizarPrestamosSolicitados (que se encargara de mostrar información sobre los préstamos solicitados). 

Se define la función visualizarPrestamosSolicitados, para que muestra la información sobre los préstamos en una cola (colaPrestamos). 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/10.jpeg?raw=true) 

- Se imprime un mensaje indicando que se mostrarán los préstamos en cola. 

- Se emplea un bucle for junto con la función de extensión withIndex (que itera sobre cada elemento en la cola de préstamos (colaPrestamos), obteniendo tanto el índice como el objeto prestamo). 

- Para cada préstamo en la cola, se imprime información detallada, incluyendo la fecha, la cantidad del préstamo, la cantidad de cuotas, el tipo de cuota, el interés, la dirección, y la información del usuario que solicitó el préstamo (nombre y correo electrónico). 

- Se imprime una línea en blanco después de cada préstamo para mejorar la legibilidad. 

Se define la función calcularPorcentajeInteres, que calcula el porcentaje de interés para un préstamo basándose en el monto del préstamo y la cantidad de cuotas. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/11.jpeg?raw=true) 

- La función toma dos parámetros: montoPrestamo (Double) y las cuotas (Int)  

- Se establece la tasaInteresBase en 0.05. 

- Se calcula el porcentajeInteres sumando la tasa de interés base con la proporción de las cuotas respecto a 12 (asumiendo que las cuotas son mensuales). 

- Se calcula el interés total multiplicando el monto del préstamo (montoPrestamo) por el porcentaje de interés calculado. 

- Se devuelve el resultado del cálculo del interés total. 

Se define la función editarDatosUsuario que permitirá al usuario editar sus datos. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/12.jpeg?raw=true)  

- Se imprime un mensaje indicando que se están editando los datos del usuario, seguido de un menú con opciones para cambiar el nombre, correo, número de teléfono, o volver al menú principal. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/13.jpeg?raw=true) 

- Empleando readLine()?.toIntOrNull(), lee la entrada del usuario como un número entero, y se utiliza when para determinar la acción a realizar según la opción seleccionada. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/14.jpeg?raw=true) 

- Para cada opción, se solicita al usuario la entrada correspondiente (nuevoNombre, nuevoCorreo, nuevoTelefono) y se actualizan los datos del usuario si la entrada no está en blanco, seguido de un mensaje indicando el éxito o la cancelación de la operación. 

- Si el usuario elige la opción 4, se imprime un mensaje indicando que se está volviendo al menú principal.  

- Si la entrada no coincide con ninguna opción válida, se imprime un mensaje de error. 

Se define la función cambiarContraseña, que permitirá al usuario cambiar su contraseña. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/15.jpeg?raw=true) 

- Se imprime un mensaje indicando que se está cambiando la contraseña para el usuario. 

- Se solicita al usuario que ingrese la contraseña actual empleando readLine().orEmpty(). 

- Se compara la contraseña ingresada con la contraseña actual del usuario (user.contraseña). Si son iguales, se permite al usuario ingresar una nueva contraseña. 

- Si la contraseña actual es correcta, se solicita al usuario que ingrese la nueva contraseña (nuevaContraseña) a la cual se le asigna a la propiedad contraseña del objeto Usuario y se imprime un mensaje indicando que la contraseña ha sido cambiada exitosamente. 

- Si la contraseña actual es incorrecta, se imprime un mensaje indicando que la contraseña actual es incorrecta y se le pide al usuario que lo intente nuevamente. 

Se define la función eliminarCuenta, que permitirá al usuario eliminar su cuenta.  

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/16.jpeg?raw=true) 

- Se imprime un mensaje preguntando al usuario si está seguro de que desea eliminar su cuenta. 

- Se lee la entrada del usuario utilizando readLine().orEmpty().toLowerCase() y se convierte a minúsculas para asegurar que las respuestas "Sí" o "No" sean reconocidas. 

- Si la confirmación es "si", se elimina el usuario actual (registroUsuario.remove(user)), y se imprime un mensaje indicando que la cuenta ha sido eliminada exitosamente. 

- Si la confirmación es "no" o cualquier otra entrada, se imprime un mensaje indicando que la operación ha sido cancelada y la cuenta no ha sido eliminada. 

Se define la función realizarPregunta, que permitirá al usuario realizar preguntas y agregarla a una lista de preguntas. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/17.jpeg?raw=true)  

- Se imprime un mensaje pidiendo al usuario que ingrese su pregunta utilizando readLine().orEmpty() para manejar el caso en que la entrada sea nula. 

- Se crea un nuevo objeto Pregunta utilizando la información proporcionada por el usuario: el objeto Usuario que hizo la pregunta (user), el texto de la pregunta (preguntaTexto), y la fecha actual (Date()). 

- El objeto Pregunta recién creado se agrega a la lista preguntas mediante el método add. 

- Se imprime un mensaje indicando que la pregunta ha sido enviada con éxito. 

Se crea la función verPreguntas, que permitirá visualizar las preguntas realizadas, ordenadas por fecha.  

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/18.jpeg?raw=true) 

- Se verifica si la lista de preguntas (preguntas) está vacía. Si es así, se imprime un mensaje indicando que no hay preguntas disponibles. 

- Si hay preguntas, se crea una nueva lista llamada preguntasOrdenadas que contiene las preguntas ordenadas por fecha utilizando sortedBy { it.fecha }. 

- Se imprime un encabezado indicando que se mostrarán las preguntas realizadas. 

- Mediante un bucle for y la función de extensión withIndex(), se itera sobre las preguntas ordenadas, imprimiendo el índice, el texto de la pregunta, y el nombre del usuario que hizo la pregunta. 

Para que el programa funcione se crea la función principal (main) 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/19.jpeg?raw=true)  

- Se imprime un menú principal con tres opciones: Iniciar Sesión, Crear Cuenta y Salir. 

Si el usuario escoge la opción 1 (Iniciar Sesión), se le mostrara lo siguiente:  

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/20.jpeg?raw=true) 

- Debe ingresa su correo electrónico y contraseña. 

- Se llama a la función inicioSesion con el correo electrónico y la contraseña proporcionados, que devuelve un objeto de tipo Usuario si el inicio de sesión es exitoso, o null si no lo es. 

- Si el inicio de sesión es exitoso, se imprime un mensaje indicando que el inicio de sesión ha sido exitoso. 

- Se inicia un bucle infinito (while (true)) que presenta un menú con varias opciones para el usuario después del inicio de sesión. 

- Se presenta un nuevo menú con opciones como "Préstamo", "Gráficas", "Cambiar Contraseña", "Configuración" y "Cerrar Sesión". 

Después de iniciar sesión el usuario podrá elegir más opciones: 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/21.jpeg?raw=true)

-Si el usuario elige la opción 1, y si está autenticado, se llama a la función datos para mostrar los datos del usuario y luego a solicitarPrestamo para permitir al usuario solicitar un préstamo y se imprime un mensaje indicando que el préstamo ha sido solicitado con éxito. 

- Si el usuario elige la opción 2, se imprime un mensaje indicando que la opción de gráficas ha sido seleccionada.  

- Si el usuario elige la opción 3, se presenta un submenú de configuración con las opciones "Editar Datos de Usuario", "Cambiar Contraseña", "Cerrar Sesión" y "Eliminar Cuenta". 

Si el usuario eligió la opción 3 (Configuración) se le mostrara lo siguiente:  

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/22.jpeg?raw=true)

- Si escoge la opción de Editar Datos, y si el usuario está autenticado, se llama a la función editarDatosUsuario para permitir que el usuario edite sus datos. 

- Si escoge la opción de Cambiar Contraseña y si el usuario está autenticado, se llama a la función cambiarContraseña para permitir que el usuario cambie su contraseña. 

- Si escoge la opción de Cerrar Sesión, se imprime un mensaje indicando que se está cerrando la sesión, se asigna null a la variable usuario, y se rompe el bucle (break) para salir del submenú. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/23.jpeg?raw=true)

- Si escoge la opción de Eliminar Cuenta, y si el usuario está autenticado, se llama a la función eliminarCuenta y se utiliza return para salir completamente del programa después de eliminar la cuenta. 

- Si la entrada del usuario no coincide con ninguna opción válida, se imprime un mensaje indicando que la opción no es válida. 

Si el usuario eligió la opción 4 (Preguntas) le mostrara lo siguiente:  

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/24.jpeg?raw=true)

- Se presenta un submenú relacionado con preguntas como "Realizar una pregunta", "Ver preguntas realizadas" y "Volver al menú principal".  

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/25.jpeg?raw=true)

-Si escoge la opción 1 y si el usuario está autenticado, se llama a la función realizarPregunta para permitir que el usuario realice una pregunta. Si no está autenticado, se muestra un mensaje de error. 

-Si escoge la opción 2, se llama a la función verPreguntas para mostrar las preguntas realizadas. 

-Si escoge la opción 3, imprime un mensaje indicando que el usuario está volviendo al menú principal. 

-Si la entrada del usuario no coincide con ninguna opción válida, se imprime un mensaje indicando que la opción no es válida. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/26.jpeg?raw=true)

- Si eligió opción 5 (Cerrar Sesión), imprime un mensaje indicando que se está cerrando la sesión y utiliza break para salir del bucle infinito (while (true)) que maneja el menú principal que termina la ejecución del menú. 

- Si la entrada del usuario no coincide con ninguna opción válida, se imprime un mensaje indicando que la opción no es válida. 

Si eligió la opción "2" en el menú principal (Crear Cuenta) se mostrará lo siguiente:  

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/27.jpeg?raw=true)

- Se solicita al usuario varios datos, incluyendo nombre, correo electrónico, número de teléfono, contraseña y confirmación de contraseña y se utiliza readLine().orEmpty() para manejar casos en los que la entrada del usuario sea nula. 

- Verifica si la contraseña y la confirmación de la contraseña coinciden. Si coinciden, se procede con el registro del usuario. Si no coinciden, se imprime un mensaje indicando que las contraseñas no coinciden y se solicita al usuario que lo intente nuevamente. 

- Se genera un código de verificación utilizando la función generateVerificationCode().  

- Si las contraseñas coinciden, se llama a la función registroUser para registrar al usuario con los datos proporcionados y al código de verificación generado, luego, se llama a sendVerificationEmail para enviar un correo de verificación al correo electrónico del usuario. 

- Se imprime un mensaje indicando que el registro fue exitoso y que se ha enviado un correo de verificación al usuario. 

![image](https://github.com/LauraP30/Proyecto-Gestion-Prestamos/blob/main/28.jpeg?raw=true). 

- Si eligió la opción 3 (Cerrar Sesión) en el menú principal, imprime un mensaje de despedida ("¡Hasta luego!") y emplea return para salir completamente del programa. 

- Si la entrada del usuario no coincide con ninguna opción válida, se imprime un mensaje indicando que la opción no es válida. 
