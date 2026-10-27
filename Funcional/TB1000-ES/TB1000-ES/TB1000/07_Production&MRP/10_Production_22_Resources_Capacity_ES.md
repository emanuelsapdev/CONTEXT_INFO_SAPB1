<!-- Slide number: 1 -->

# Producción y MRP: Capacidad de recursos
SAP Business One
Versión 10.0

### Notes:

Bienvenido al curso sobre Capacidad de recursos.

<!-- Slide number: 2 -->

# Objetivos
Al finalizar este tema, podrá:
Definir, analizar y gestionar la capacidad de recursos

### Notes:
Al finalizar este tema, podrá:

Definir, analizar y gestionar la capacidad de recursos

Tenga en cuenta que para estudiar este tema hay que estar familiarizado con los temas del curso Concepto del proceso de producción y Recurso.

<!-- Slide number: 3 -->
# Planificación de capacidad de recursos
¿Tenemos suficiente capacidad para fabricar y entregar a tiempo los productos solicitados?

Planificación y supervisión de la capacidad de producción
Visibilidad de la capacidad disponible para evitar cuellos de botella y optimizar la planificación de producción

### Notes:
Una parte importante del proceso de producción implica el consumo de recursos.  Podemos definir la capacidad disponible, la consumida en producción y gestionar la disponibilidad de la capacidad de recursos.

Esta función nos permite planificar y supervisar la capacidad de recursos para evitar cuellos de botella y optimizar la planificación de producción.

<!-- Slide number: 4 -->

# Escenario empresarial: gestionar y planificar recursos

OC WoodTrend fabrica ventanas y puertas de madera personalizadas basándose en las especificaciones del cliente.
Para OC WoodTrend, es muy importante la gestión de recursos y de sus capacidades para asegurarse de que los clientes reciben las entregas a tiempo. Deben identificar si la producción se puede llevar a cabo tal como se planificó o si se deben realizar ajustes de planificación manuales para cumplir los plazos.

### Notes:
En este ejemplo, nos fijamos en la empresa OC WoodTrend que fabrica ventanas y puertas de madera personalizadas basándose en las especificaciones del cliente. Utilizan un proceso de producción contra pedido en el que los plazos se obtienen de la fecha de entrega de los pedidos de los clientes.

Para OC WoodTrend, es muy importante la gestión de recursos y de sus capacidades para asegurarse de que los clientes reciben las entregas a tiempo. Deben identificar si la producción se puede llevar a cabo tal como se planificó o si se deben realizar ajustes de planificación manuales para cumplir los plazos.

<!-- Slide number: 5 -->
# Generar la capacidad disponible

### Notes:
Para gestionar la capacidad de un recurso, debe generar la capacidad disponible. Se realiza en dos pasos:
En el paso 1, defina un plan semanal, en el que puede fijar la capacidad del recurso prevista para cada día de la semana.
En el paso 2, debe generar la capacidad de todo un periodo (por ejemplo, un trimestre), copiando el plan semanal definido en el paso 1 en todo el periodo. O, puede definir manualmente la capacidad que tiene cada día de ese periodo.
Existen dos clases de capacidades diarias que deben definirse: Capacidades de ejecución interna y única. Una capacidad de ejecución única asume que solo se puede crear una orden de producción mediante un recurso determinado en un período en concreto. Con la capacidad interna, no se tiene en cuenta este tipo de limitación.
El resultado de estos pasos es una capacidad disponible (ejecución interna y única) que le permite gestionar y asignar las capacidades en el proceso de producción.

<!-- Slide number: 6 -->
# Gestionar capacidades de recursos: Paso 1
Primer paso Definir las capacidades diarias estándares en Datos maestros del recurso en la ficha Datos de planificación.


Solo 1 factor es relevante para la capacidad de ejecución única
32 ciclos al día  X 2 máquinas = 64 ciclos al día

### Notes:
Puede planificar las capacidades de sus recursos en la ficha Datos de planificación de cada registro de Datos maestros del recurso. Estas capacidades se definen a diario.
Hay disponibles cuatro factores  y puede definirlos para cada día de la semana. Estos factores permiten definir fácilmente las capacidades de un determinado recurso. Por ejemplo, se puede utilizar un factor para representar el número de horas trabajadas en un turno, el número de turnos de un día determinado o el número de máquinas (recursos).

Tenga en cuenta que existen dos tipos de capacidades: Interna y Ejecución única. La capacidad interna es un simple cálculo de las columnas factor multiplicadas entre sí.  En nuestro caso, 32 ciclos diarios se multiplican por 2 máquinas disponibles, lo que da como resultado una capacidad interna de 64 ciclos.
Sin embargo,, la capacidad de ejecución única solo tendrá en cuenta las columnas factor que se marcan como relevantes para la capacidad de ejecución única. En nuestro ejemplo, solo es relevante el factor 1 y, por lo tanto, solo se realizan 32 ciclos diarios en la capacidad de ejecución única.

Tenga en cuenta que también puede indicar un valor directamente en las columnas Capacidad diaria y Capacidad de ejecución única.

<!-- Slide number: 7 -->
# Gestionar capacidades de recursos: Paso 2
Recursos > Fijar capacidades internas diarias

Segundo paso
Definir manualmente las Capacidades internas diarias para un determinado periodo de tiempo o basadas en los datos por defecto de los Datos maestros del recurso
También puede copiar la capacidad de ejecución única en la capacidad interna y viceversa.

### Notes:
El paso siguiente es generar capacidades internas diarias y capacidades de ejecución única para un periodo de tiempo específico. Se realiza en la ventana Fijar capacidades internas diarias en el menú Recursos o desde el menú contextual Datos maestros del recurso. En este paso puede generar los valores de capacidad ya sea copiando las capacidades diarias estándares que están definidas en Datos maestros del recurso o introduciendo manualmente la capacidad.
También puede utilizar esta ventana para copiar las capacidades de ejecución única en las capacidades internas y viceversa.

<!-- Slide number: 8 -->
# Gestionar capacidades de recursos: Resultado
 Resultado:    Analizar y gestionar recursos en la ventana Capacidad de recursos



### Notes:
Puede consultar las capacidades internas y de ejecución única que se han generado en la ventana Capacidad de recursos y también en la ficha Datos de capacidad de Datos maestros del recurso.

La ventana Capacidad de recursos proporciona una descripción completa de la capacidad de los recursos seleccionados en un período seleccionado.  Un usuario puede seleccionar varias vistas como, por ejemplo,  interna, disponible y ejecución única. A continuación, puede consultar la capacidad del almacén especificado en un día concreto. Hablaremos de las diferentes vistas en la siguiente diapositiva.

Tenga en cuenta que se puede definir la capacidad de los recursos para varios almacenes. Esto puede ser útil cuando los almacenes se configuran como áreas de producción. Cada almacén pueden tener su propia capacidad y asignación de capacidad. Puede definir las opciones predeterminadas en la ficha Parametrizaciones generales > Recursos.

<!-- Slide number: 9 -->
# Visualizar la capacidad del recurso
Ficha Recursos > Datos maestros del recurso > Datos de capacidad


Interna
Capacidades del recurso
Comprometido
Capacidades asignadas a órdenes de producción
Consumida
Capacidades emitidas para la producción
Disponible
= Interna – Comprometida – Consumida

### Notes:
También puede consultar la capacidad de un recurso específico en la ficha Datos de capacidad en Datos maestros del recurso. En este caso, se han resumido las capacidades del periodo de capacidad seleccionado en la parte superior de la ficha. Las capacidades se muestran como: Interna, Comprometida, Consumiday Disponible.

Capacidad interna: es la capacidad total de recursos durante el periodo de tiempo seleccionado.
La capacidad comprometida es la capacidad asignada a una determinada orden de producción en el periodo elegido pero que todavía no se había enviado para fabricarla (cantidad pendiente).
La capacidad consumida es la capacidad que se consumió durante el periodo seleccionado, por ejemplo cuando se envió a producción en el periodo seleccionado.
Capacidad disponible = Interna – Comprometida – Consumida.

Tenga en cuenta que la capacidad del recurso Comprometida que está relacionada con una orden de producción específica, se asigna en función de la fecha (de inicio o fin) en la línea de esta orden de producción. Hay diferentes métodos disponibles para la asignación de recursos. Trataremos este tema en las siguientes diapositivas.

Ahora, examinaremos los números. Hemos definido una capacidad interna de 1.536 ciclos para un periodo definido. 24 ciclos de la capacidad interna son para la orden de producción, 6 ciclos ya se liberaron en una salida para producción y quedan 1506 ciclos para utilizarlos cuando sea necesario.

En la formación Recurso, aprendimos acerca de la conexión de un recurso a un artículo para comprar o vender los recursos. Algunos de los documentos de compras también generan la capacidad que se acumula en otra columna, denominada Solicitado. Para obtener más información sobre la capacidad Solicitado, consulte la guía práctica: Cómo trabajar con los recursos y la producción en SAP Business One 9.3

<!-- Slide number: 10 -->
# Métodos de asignación del recurso

Definición por defecto en el campo Datos maestros de recurso ficha General   Asignación de recursos para órdenes de producción sin hoja de ruta


Orden de producción
El método de asignación puede cambiarse por la línea de orden de producción

### Notes:
Hemos visto que la ventana Capacidad de recursos tiene una columna para cada día del intervalo especificado. En la columna del día, encontramos las cantidades Interna/ Comprometida/ Consumida/ Disponible. El sistema asigna la cantidad comprometida (que se obtiene de las órdenes de producción) en función de las fechas de inicio y de fin de las líneas de la orden.
Hay cuatro métodos de Asignación de recursos:
En la fecha de inicio: se asigna toda la cantidad de la línea a la Fecha de inicio.
En la fecha de fin: se asigna toda la cantidad de la línea a la fecha de fin.
Fecha de inicio en adelante: La cantidad comprometida se asigna según la capacidad de ejecución interna disponible de cada día. Todos los días el sistema verifica si la capacidad puede cumplir con la cantidad comprometida. Empieza por la fecha de inicio o la fecha del sistema en caso de que la fecha de inicio sea anterior. Si ese día no hay una cantidad suficiente, al día siguiente el sistema verifica la cantidad de capacidad disponible del día siguiente, y así sucesivamente, hasta que acabe de asignar toda la cantidad comprometida. Si llega la fecha de fin y todavía se debe asignar alguna cantidad, el sistema asigna la cantidad de saldo restante a la fecha de inicio.
Fecha de fin para atrás: este método se parece al método anterior pero en lugar de empezar a asignar la capacidad a partir de la fecha de inicio en adelante, se empieza a partir de la fecha de fin para atrás.
Para órdenes de producción sin hoja de ruta, es posible establecer el método de asignación de recursos por defecto en cada recurso, como se muestra en la imagen. Sin embargo, también se puede modificar el método de asignación de cada línea de la orden de producción.
En la siguiente diapositiva, examinaremos un ejemplo de imputación según los diferentes métodos.

<!-- Slide number: 11 -->
# Método de asignación de recursos: Ejemplo sin hoja de ruta
Cantidad de línea de los recursos comprometidos = 10
Fecha de inicio de línea = 1 de marzo
Fecha de fin de línea = 4 de marzo
|  | 1 de marzo | 2 de marzo | 3 de marzo | 4 de marzo |
| --- | --- | --- | --- | --- |
| Capacidad de ejecución única: | 6 | 3 | 2 | 8 |
| Método de asignación | Cantidad disponible |  |  |  |
| En la fecha de inicio | -4 | 3 | 2 | 8 |
| En la fecha de fin | 6 | 3 | 2 | -2 |
| Fecha de inicio en adelante | 0 | 0 | 1 | 8 |
| Fecha de fin para atrás | 6 | 3 | 0 | 0 |

### Notes:
Para una mejor comprensión de los diferentes métodos, veamos el ejemplo.
Tenemos una orden de producción con una cantidad de línea de recursos de 10.
La fecha de inicio de la línea es el 1 de marzo. La fecha de fin de la línea es el 4 de marzo.
Veamos ahora los posibles resultados en cada método:
Si utilizamos el método En la fecha de inicio, toda la cantidad (10) se obtiene de la Fecha de inicio 1 de marzo y da como resultado la cantidad disponible negativa de -4. Durante los días siguientes no ocurre nada.
Si se utiliza el método En la fecha de fin, toda la cantidad se obtiene del 4 de marzo y da como resultado la cantidad negativa de -2 para este día.
Si se utiliza el método Fecha de inicio en adelante, se usa toda la cantidad disponible (6) y, al día siguiente, el 2 de marzo, también se obtiene toda la cantidad disponible (3). Como todavía se necesita una cantidad 1 adicional, ésta se obtiene del 3 de marzo y solo se deja una cantidad 1. No le ocurre nada a la cantidad del 4 de marzo.
Si se utiliza Fecha de fin para atrás, la cantidad disponible (8) se obtiene de la Fecha de fin, es decir, el 4 de marzo. A continuación, si volvemos al 3 de marzo, vemos que toda la cantidad (2) también se obtiene para completar la cantidad de 10 necesaria para el recurso.

El método Fecha de inicio en adelante puede ser útil cuando se esté fabricando para aumentar el inventario y cuando la fecha de fin no sea crucial. Es más importante que el inventario se fabrique lo antes posible. El método Fecha de fin para atrás puede ser importante cuando la producción sea para una demanda específica del cliente con una fecha de vencimiento determinada.  Partiendo de la base de que deseamos tener en nuestros almacenes el mínimo inventario posible, nos gustaría fabricar en base "al momento justo" para que el pedido del cliente se entregue en la fecha acordada y no antes.

<!-- Slide number: 12 -->
# Vista acumulada

Vista normal

Vista acumulada


### Notes:
La ventana Capacidad de recursos también proporciona una vista de capacidad acumulada.
En esta vista, todas las cantidades de capacidad se acumulan diariamente. Cada día muestra una acumulación de los días anteriores. Puede ser útil a la hora de identificar si está demasiado comprometida la capacidad de un recurso.
Para cambiar la vista de capacidad acumulada, seleccione la casilla de selección Mostrar capacidad acumulada de hoy.
En la imagen superior, vemos la ventana de capacidad de recursos. Tenga en cuenta que el día 3 de mayo hay una cantidad disponible negativa de -26. Pero, ¿es una sobrecarga real? El director de producción puede pasar fácilmente la producción al día anterior.
Tal como se muestra en la imagen inferior, la vista acumulada puede indicar claramente que hay una sobrecarga de recursos real. En nuestro caso, no aparece ninguna cantidad disponible negativa ya que, a partir de hoy, se acumula la cantidad. Sin embargo, una cantidad negativa disponible indicaría que la cantidad total disponible hasta esa fecha es negativa y que el compromiso total es mayor que la capacidad total disponible. En ese caso, una modificación manual de las fechas de la orden de producción puede ayudar a evitar cantidades disponibles negativas.

<!-- Slide number: 13 -->

# Resumen
A continuación, se detallan algunos puntos clave:

La función Capacidad de recursos visualiza la capacidad disponible para evitar cuellos de botella y optimizar la planificación de producción.
Existen cuatro vistas de capacidad: Interna, Comprometida, Consumida y Disponible.
Se puede definir la capacidad diaria estándar en la ficha Datos de planificación de los Datos maestros del recurso.
Se pueden generar capacidades internas y de ejecución única según la capacidad diaria planificada.
Se puede asignar la capacidad de recursos en la fecha de inicio, fecha de fin, a partir de la fecha de inicio en adelante o a partir de la fecha de fin para atrás para la orden de producción.
En la ventana Capacidad de recursos, la vista acumulada puede ser útil para identificar si está demasiado comprometida la capacidad de una máquina.

### Notes:
Estos son algunos puntos clave de esta sesión.
La función Capacidad de recursos permite la visibilidad de la capacidad disponible para evitar cuellos de botella y optimizar la planificación de producción.
Existen cuatro vistas de capacidad: Interna, Comprometida, Consumida y Disponible.
Se puede definir la capacidad diaria estándar en la ficha Datos de planificación de los Datos maestros del recurso.
Se puede generar una capacidad interna según la capacidad diaria planificada.
Se puede asignar la capacidad de recursos en la fecha de inicio, fecha de fin, a partir de la fecha de inicio en adelante o a partir de la fecha de fin para atrás para la orden de producción.
En la ventana Capacidad de recursos, la vista acumulada puede ser útil para identificar si está demasiado comprometida la capacidad de una máquina.
