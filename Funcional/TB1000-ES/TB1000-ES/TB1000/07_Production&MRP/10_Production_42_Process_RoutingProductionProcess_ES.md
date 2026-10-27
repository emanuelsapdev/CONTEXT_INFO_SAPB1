<!-- Slide number: 1 -->

# Producción y MRP: Orden de producción con hoja de ruta
SAP Business One
Versión 10.0

### Notes:
Bienvenido al tema de formación Orden de producción: Escenario de hoja de ruta.
Para hacer este curso se recomienda completar antes el tema Lista de materiales y Proceso de producción básico.

<!-- Slide number: 2 -->

# Objetivos
Al finalizar este tema, podrá:
Crear y gestionar un orden de producción con hoja de ruta

### Notes:
Al finalizar este tema, podrá:
Crear y gestionar un orden de producción con hoja de ruta

<!-- Slide number: 3 -->

# Ejemplo empresarial

OC WoodTrend fabrica muebles de madera.
Para la producción compleja, OC WoodTrend ha definido la lista de materiales con hoja de ruta que incluye etapas en secuencia y dependencias de fecha.
Desean empezar a fabricar estas listas de materiales.

### Notes:
OC WoodTrend fabrica muebles de madera.
Para la producción compleja, OC WoodTrend ha definido la lista de materiales con hoja de ruta que incluye etapas en secuencia y dependencias de fecha.
Desean empezar a fabricar estas listas de materiales.

<!-- Slide number: 4 -->
# Lista de materiales con hoja de ruta
LdM de un armario blanco
| Componentes | Etapa de ruta |
| --- | --- |
| Cortadora | Etapa 1: Corte |
| Operario de la máquina |  |
| Planchas de madera |  |
| Lijadora | Etapa 2: Lija |
| Operario de la máquina |  |
| Máquina de pintura | Etapa 3: Pintura |
| Operario de la máquina |  |
| Pintura blanca |  |
| Carpintero | Etapa 4: Montaje |
| Bisagras |  |
| Estanterías |  |
| Pomos |  |
| Tornillos |  |
Armario blanco

Recurso
Artículos

### Notes:
En este escenario analizaremos el proceso de producción de la lista de materiales de un armario blanco.
Existen 4 pasos en el proceso de producción del armario: Corte, lija, pintura y montaje, como se muestra en la imagen.
Esta lista de materiales se copia en la orden de producción.

<!-- Slide number: 5 -->
# Orden de producción con hoja de ruta

Haga clic con el botón derecho


Seleccione lo que desea visualizar

### Notes:
Se trata de una orden de producción de la la lista de materiales del armario blanco.
Como se explicó en el tema lista de materiales, una lista de materiales con hoja de ruta se compone de varias etapas en las que cada etapa agrupa un conjunto de artículos y los recursos correspondientes para la etapa.
En la imagen vemos dos de las etapas. Detrás de cada etapa podemos ver los componentes relacionados la misma. Esta visualización se pueden ajustar desde el menú contextual o desde el menú Ir a en la parte superior de la pantalla.
Además, las órdenes de producción con hoja de ruta permiten el cálculo automatizado de las dependencias de fecha entre etapas de ruta.  El sistema puede programar de forma automática las fechas de inicio y de fin del artículo y los componentes de recurso para obtener más fechas relevantes. Trataremos este tema en las siguientes diapositivas.

<!-- Slide number: 6 -->
# Campo Cálculo de la fecha de hoja de ruta
Desde la cabecera de orden de producción:

Cálculo de la fecha de hoja de ruta

En la fecha de inicio
En la fecha de fin
Fe. de inicio en adelante
Fecha de fin para atrás
Efectos en las etapas
Fecha de inicio
Fecha final
Asignación de la capacidad de recursos

### Notes:
Cuando se utilizan órdenes de producción con hoja de ruta, es importante comprender cómo funcionan el campo y función Cálculo de la fecha de hoja de ruta.
Esta definición en la orden de producción puede afectar a la fecha de inicio y a la fecha de fin de cada fila en la orden de producción, así como la asignación de la capacidad de recursos en la línea.
En función del valor del cálculo de la fecha de hoja de ruta, también podrían verse afectadas la fecha de inicio y la fecha de fin en la cabecera.
La fecha de programación también es relevante para los componentes de artículo porque la fecha de inicio de línea de los mismos afecta a la planificación de necesidades de material.
OC WoodTrend gestiona la capacidad de recursos para garantizar que un recurso determinado está disponible durante la producción y para poder planificar con antelación la producción.
Existen cuatro métodos de cálculo de la fecha de hoja de ruta: En la fecha de inicio, En fecha de fin, Fecha de inicio en adelante y Fecha de fin en adelante.
Vamos a analizarlos en la siguiente diapositiva.

<!-- Slide number: 7 -->
# Cálculo de la fecha de hoja de ruta – Fechas de las etapas y consumo de recursos

El recurso se asigna a la fecha de inicio en cada etapa

No afecta
a las fechas en las etapas
En la fe. de inicio
El recurso se asigna a la fecha de fin de cada etapa

En la fe. de fin

### Notes:
La fecha de inicio y la fecha de fin de la cabecera son el rango de tiempo para el consumo de los componentes en la orden de producción.
Sin embargo, varios métodos de cálculo pueden definir fechas de inicio y de fin distintas de las etapas en ese rango.

Con los métodos: En la fecha de inicio y En la fecha de fin, no hay dependencias de fecha entre las etapas de la orden.
La fecha de inicio de todas las etapas se establece por defecto a partir de la fecha de inicio de la cabecera.
La fecha de fin de todas las etapas se establece por defecto a partir de la fecha de vencimiento de la cabecera.
Con el método En la fecha de inicio, los recursos se asignan a la fecha de inicio de la etapa y con el método En la fecha de fin, los recursos se asignan a la fecha de fin de la etapa.

<!-- Slide number: 8 -->
# Cálculo de la fecha de hoja de ruta – Fechas de las etapas y consumo de recursos

El recurso se asigna a la fecha de inicio en cada etapa
No afecta
a las fechas en las etapas

En la fe. de inicio
El recurso se asigna a la fecha de fin de cada etapa
En la fe. de fin

La asignación de recursos empieza a partir de la fecha de inicio de la primera etapa
La fecha de fin de una etapa fija la fecha de inicio de la etapa siguiente
La fecha de fin de la última etapa establece la fecha de vencimiento en la cabecera
Fecha de inicio en adelante

La asignación de recursos se inicia a partir de la fecha final de la última etapa
La fecha de inicio de una etapa fija la fecha de fin de la etapa anterior
La fecha de inicio de la primera etapa fija la fecha de inicio en la cabecera
Fecha de fin para atrás

### Notes:
Los otros dos métodos son más sofisticados:

Con el método Fecha de inicio en adelante, la fecha de inicio de la cabecera se copia en la fecha de inicio de la primera etapa. Si no hay suficiente capacidad para cumplir con la cantidad del recurso planificada, el sistema sigue asignando capacidad de recursos en los próximos días hasta que se asigna toda la capacidad planificada. La fecha de fin de esta etapa es el último día de la asignación de la capacidad. En la fase siguiente, la fecha de inicio es la fecha de fin de la etapa anterior. Cuando se alcanza la última etapa, la fecha de fin se fija en la fecha de vencimiento de la cabecera. Tenga en cuenta que laasignación de capacidad se calcula desde del comienzo del día.

El método  Fecha de fin para atrás funciona de forma similar pero partiendo de la fecha de fin de la última etapa.
La fecha de vencimiento de la cabecera se copia en la fecha de fin de la última etapa. Si no hay suficiente capacidad para cumplir con la cantidad del recurso planificada, el sistema sigue asignando capacidad de recursos de cada día precedente hasta que se asigne toda la capacidad planificada. La fecha de inicio de esta etapa será el último día de la asignación de la capacidad. La fecha de fin de la etapa anterior será la fecha de inicio calculada de la última etapa.
Al alcanzar primera etapa, la fecha de inicio se fija en la fecha de inicio de la cabecera.
Tenga en cuenta que la asignación de capacidad se calcula desde del final del día.

Tenga en cuenta también que con estos dos métodos la orden de producción solo tendrá en cuenta la clase de capacidad denominada: Capacidad de ejecución única. Esta clase de capacidad asume que sólo se puede utilizar un recurso a la vez.
Para conocer más acerca de la capacidad de recursos, consulte la formación Capacidad de recursos.

<!-- Slide number: 9 -->
# Cálculo de días necesarios
Recurso Cantidad  planificada en la etapa = 12
|  | Día 4 | Día 3 | Día 2 | Día 1 |  |
| --- | --- | --- | --- | --- | --- |
| Cap. ejec.  única disp.: |  |  |  |  |  |
| Días neces. | Asignación de capacidad |  |  |  |  |
| Fe. inicio en adelante: | 4 Fe. ini. etapa | 6 | 2 Fe. fin de etapa |  | 2,5 |
| Fecha de fin  p. atrás: |  |  | 2 Fe. inicio etapa | 10 Fe. fin etapa | 1,5 |
10
6
4
4
#1
#2

### Notes:
Analizaremos este escenario para los métodos Fecha de inicio en adelante  y Fecha de fin para atrás.
Analizaremos el efecto sobre la fecha de inicio y de fin de una etapa y sobre la asignación de la capacidad de recursos.

En nuestro escenario, la cantidad planificada del recurso en la etapa es 12.
La capacidad de ejecución única disponible se fija en 4 el día 1, 6 el día 2, 4 el día 3 y 10 el día 4.

Al utilizar el cálculo de fecha de hoja de ruta Fecha de inicio en adelante, el sistema empieza a asignar la capacidad disponible para lograr la capacidad necesaria de la etapa, a partir de la fecha de inicio de la etapa (día 1). Para asignar 12 unidades de recurso, el sistema consume las 4 unidades del día 1, luego otras 6 del día 2 y, finalmente, otras 2 de las 4 unidades disponibles en el día 3. Esto también significa que son necesarios 2 días completos del tiempo disponible del recurso + 2 de las 4 unidades de recurso, lo que equivale a medio día de recurso. Por lo tanto, los días necesarios son 2.5.

Al utilizar el cálculo de la fecha de hoja de ruta del Fecha final para atrás, el sistema comienza a realizar asignaciones a partir de la fecha de fin de la etapa (día 4). El sistema consume las 10 unidades disponibles el día 4 y otras 2 de las 4 disponibles el día 3. Con este método, los días necesarios son 1,5.

<!-- Slide number: 10 -->
# Cálculo de días totales
Días totales = Días necesarios + días de espera
|  | Componentes | Días de espera | Días necesarios | Días totales |
| --- | --- | --- | --- | --- |
| Etapa 3: | Pintura: | 1,5 días | 1 2,5 |  |
|  | Recurso:  Máquina pintura | 1,5 |  |  |
|  | Recurso:  Operario de la máquina | 0,5 |  |  |
|  | Artículo: Pintura blanca |  |  |  |


### Notes:
Existen varios campos de cálculo en la orden de producción que ofrecen información sobre los tiempos en la fabricación. Esta formación cubre algunos.

Este es un ejemplo de una etapa de nuestra lista de materiales: la etapa de pintura.
Para cada línea de recurso se calculan los días necesarios. Los días necesarios de la etapa son el valor máximo de días necesarios de todas las líneas de recurso de la etapa.
También hemos tratado el campo Días de espera en la formación Lista de materiales. Se trata de un valor agregado manualmente que refleja los tiempos de espera entre etapas.
Una vez finalizada la etapa de pintura, es necesario esperar 1 día para que se seque la pintura del armario.
Estos días de espera se añaden a los días necesarios y se obtiene un valor de días totales de 2.5.

<!-- Slide number: 11 -->
# Cálculo de tiempo de producción
| Componentes | Tiempo de producción |
| --- | --- |
| Etapa 3: Pintura | 10 horas |
| Recurso:  Máquina de pintura | 10 horas |
| Recurso:  Operario de la máquina | 5 horas |
| Artículo: Pintura blanca |  |


### Notes:
El recurso Tiempo de producción es la cantidad de recursos planificada expresada en tiempo (de acuerdo con el campo Tiempo por unidad de recursos en los datos maestros del recurso).
En este caso, es un total de 10 horas para la máquina de pintura y 5 horas para el operador que maneja la máquina.
Para calcular el tiempo de producción de una etapa, el sistema simplemente toma el tiempo de producción más alto de todas las líneas de recurso en la etapa, que en este caso es 10.

Es importante comprender la diferencia principal entre los valores Tiempo de producción y Días necesarios. Por ejemplo, Tiempo de producción en la línea puede representar el tiempo de máquina real de un recurso mientras que Días necesarios es el tiempo total que el recurso debe estar asignado a esta tarea en general.

<!-- Slide number: 12 -->
# Recálculo de hoja de ruta
Se realiza una modificación en la orden de producción

Actualizar ahora
Cálculo de la fecha de  hoja de ruta

Actualiza la fecha de inicio y de fin de etapas y líneas

Actualiza la asignación de capacidad de los recursos

### Notes:
En una orden de producción con hoja de ruta, es posible que las modificaciones manuales realizadas en la cabecera de la orden de producción o en la línea requieran volver a calcular las fechas de la línea y la asignación de capacidad de los recursos.
El sistema no inicia automáticamente esta actualización, sino que permite al usuario decidir si desea actualizar las líneas o no. Para indicar al usuario que hay una actualización, el botón Actualizar ahora se pone de color rojo como se muestra en la imagen.

En OC WoodTrend existe la necesidad de recalcular las fechas de etapa cuando se pospone la fecha de inicio de producción y el cálculo de fecha de hoja de ruta es Fecha de inicio en adelante.
Cuando el jefe de producción cambia la fecha de inicio en la cabecera de la orden de producción, el botón Actualizar ahora se pone en rojo. El director de producción selecciona el botón y aparece un mensaje del sistema que le pide autorización al usuario para actualizar las fechas de línea según corresponda.
Un procedimiento similar sucede cuando un determinado recurso se sustituye por otro. Dado que el recurso nuevo posee otro tiempo de producción y capacidad disponible, el jefe de producción selecciona el pulsador rojo para actualizar las fechas de inicio y de fin de la etapa y la asignación de capacidad de los recursos.

Consulte el documento: Cómo trabajar con los recursos y la producción en SAP Business One 9.3 para ver la lista de condiciones que hacen que el botón se vuelva de color rojo.

<!-- Slide number: 13 -->
# Salida para producción: Escenario de hoja de ruta

Enviar componentes: Criterios de selección

Secuencia de ruta

Etapa de ruta

Es posible enviar componentes por etapa de ruta

Corte
Lija
Pintura
Montaje
Estado

…

### Notes:
Cuando se libera una orden de producción, el jefe de producción de OC WoodTrend envía componentes a fabricación de etapa en etapa.
El envío de componentes de una orden de producción con hoja de ruta se puede realizar por etapa de ruta.
Desde el menú contextual Orden de producción, seleccione la opción Enviar componentes, que muestra la ventana Enviar componentes: Criterios de selección. Desde esta ventana puede ajustar las etapas o componentes que desea enviar.   Recuerde que solo está disponible el envío de artículos manual.
