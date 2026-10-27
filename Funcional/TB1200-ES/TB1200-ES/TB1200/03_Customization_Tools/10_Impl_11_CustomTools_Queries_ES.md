<!-- Slide number: 1 -->

# Herramientas de personalización:  Consultas
SAP Business One
Versión 10.0

### Notes:

Este tema presenta las herramientas que SAP Business One proporciona para crear consultas SQL.

<!-- Slide number: 2 -->

# Objetivos
Objetivos:
Crear consultas SQL con las herramientas de consulta proporcionadas por SAP Business One
Identificar el campo de base de datos y los nombres de tabla en un formulario o documento mediante la información del sistema
Grabar, gestionar, ejecutar y controlar el acceso a consultas grabadas

### Notes:
En este tema, aprenderá a crear consultas SQL con las herramientas de consulta proporcionadas en SAP Business One.
Aprenderá a identificar el campo de base de datos y los nombres de tabla en un formulario o documento mediante la información del sistema.
También aprenderá cómo grabar, gestionar, ejecutar y controlar el acceso a consultas grabadas.
Tenga en cuenta que los ejemplos de consulta proporcionados en este curso están escritos para SAP Business One, versión SAP HANA.

<!-- Slide number: 3 -->

# Escenario empresarial
Las consultas permiten visualizar datos rápidamente de las tablas de base de datos de empresa de SAP Business One. Puede usar las consultas para:
Generar informes ad hoc (consultas de usuario)
Crear alertas definidas por el usuario y procesos de aprobación
Completar el contenido de un campo, incluidos los campos definidos por el usuario. La consulta se añade al campo como valores definidos por el usuario (UDV)
Mostrar información dinámica para análisis en paneles y KPI
Validar los valores importados en una tabla o campo durante la migración de datos
No se permite utilizar las herramientas de consulta para insertar, actualizar o eliminar campos de tablas estándar.

### Notes:
Las consultas le permiten visualizar y formatear rápidamente los datos de la base de datos de empresa de SAP Business One. Las consultas se pueden utilizar de varias maneras, por ejemplo:
Para generar informes ad hoc que puedan ejecutarse una y otra vez. Estas se conocen como consultas de usuario.
Crear alertas definidas por el usuario y procesos de aprobación en SAP Business One. La consulta puede comprobar condiciones que no están cubiertas por alertas o procedimientos de autorización estándar predefinidos.
Completar el contenido de un campo, incluidos los campos definidos por el usuario. La consulta se añade al campo como valores definidos por el usuario (búsquedas formateadas) y pueden rellenar el valor del campo desde los resultados de consulta.
Para mostrar información dinámica para análisis en paneles y KPI
Para validar el contenido de una tabla o campo durante la migración de datos.
Debe tener en cuenta que las herramientas de consulta no se diseñaron para generar diseños de impresión o informes completamente formateados complejos. Debe utilizar Crystal Reports para dichos propósitos. Por otra parte, no se permite el uso de las herramientas de consulta para insertar, actualizar o eliminar campos de tablas estándar.

<!-- Slide number: 4 -->
# Información del sistema


### Notes:
Para ejecutar consultas, debe conocer los nombres de las tablas y los campos de SAP Business One. Esta información se muestra cuando habilita Información del sistema.

<!-- Slide number: 5 -->
# Objetos y tablas

Un objeto puede abarcar varias tablas en la base de datos
Por ejemplo, el objeto de datos maestros de interlocutor comercial está en varias tablas de base de datos, como:
OCRD
OCPR
CRD1
OSLP

### Notes:
Un objeto puede abarcar varias tablas en la base de datos de SAP Business One.
Por ejemplo, el objeto de datos maestros de interlocutor comercial se ha retenido en múltiples tablas en la base de datos, incluida la tabla de cabecera OCRD. Existen tablas secundarias relacionadas, como OCPR, CRD1, OSLP, etc. Estas subtablas contienen los datos que puede ver en las diferentes fichas del registro de interlocutores comerciales.

Los nombres de tabla de SAP Business One contienen 4 caracteres.

<!-- Slide number: 6 -->
# Información del sistema
Ver > Información de sistema (Ctrl+Shift+I)
La información del sistema muestra la tabla y los nombres de campo de un formulario que visualice
Para ver la tabla y el nombre de campo, habilite la Información del sistema desde el menú Vista (o pulse Ctrl + Shift + I)
Al mover el ratón sobre un campo, se muestra la información en la barra de estado
Ejemplo: Si desplaza el ratón sobre el nombre en los Datos maestros de interlocutor comercial, verá que la tabla es OCRD y el nombre del campo es CardName



### Notes:
Para desarrollar una consulta SQL es necesario conocer la tabla de base de datos y el nombre del campo para la selección.
Al abrir un objeto en SAP Business One, puede conocer el nombre de la tabla para un campo habilitando la información del sistema en el menú Vista. También puede utilizar la abreviatura de teclado Ctrl + Shift + I.

Al mantener el ratón sobre un campo en el objeto, la información de tabla relevante para el campo se muestra en la barra de estado en la parte inferior de la ventana.
Ya tiene el nombre de la tabla y el nombre del campo que se introducirán en la consulta SQL.
Se visualiza información adicional del campo, como su largo máximo.

El objeto de datos maestros de interlocutor comercial se muestra en la diapositiva. Si desplaza el ratón sobre el campo Nombre, verá que la tabla es OCRD y el nombre del campo es CardName.

<!-- Slide number: 7 -->
# Documentos y objetos


Los documentos de compra y venta también se representan como objetos
Cada clase de documento (pedido, entrega, factura de clientes, pedido, factura de proveedores, etc.) tiene la misma estructura y se basa en varios objetos, incluidos:
El objeto Documentos (las partes de la cabecera)
El objeto Document_Lines (la matriz o la parte de la línea)
Un documento, como el documento de pedido de cliente que se muestra aquí, abarca varias tablas, como por ejemplo:
ORDR
RDR1

Cabecera

Líneas

Cabecera

### Notes:
Los documentos de compras y ventas, como los pedidos, las ofertas y las facturas, tienen todos la misma estructura y se basan en dos objetos principales:
El objeto Documentos para las partes de cabecera del documento
El objeto Document_Lines para la matriz o la sección de línea del documento

Una clase de documento como, por ejemplo, un pedido de cliente, abarca varias tablas.  Las tablas serán distintas para cada clase de documento, de manera que el conjunto de tablas de un pedido sea diferente del conjunto de tablas para un pedido de cliente.
Por ejemplo, el pedido de cliente utiliza la tabla de base de datos ORDR para la cabecera y la tabla RDR1 para las líneas.

<!-- Slide number: 8 -->
# Información del sistema - Números de artículo y de columna

La información del sistema también muestra:
El número de artículo para un campo de cabecera
El número de artículo, columna y línea de un campo basado en líneas
El número de artículo y de columna de un campo es el mismo en clases de documentos similares
Puesto que todos los documentos de marketing tienen el mismo número de columnas y de artículo en un campo, puede escribir consultas que sirven en distintas clases de documentos haciendo referencia a los números de artículo y de columna

Número de artículo para el campo cabecera



Número de artículo, columna y fila para el campo de línea


### Notes:
La información del sistema también muestra, además del nombre de tabla y de campo, el número de artículo de un campo de cabecera y el número de artículo, columna y línea para un campo basado en filas.
Por ejemplo, en un pedido de cliente, el número de artículo para el campo CardCode es 4. El número de columna para el campo CardCode no se muestra ya que es un campo de cabecera es ORDR y el número de columna para todos los campos de cabecera es 0.
Si abre otros documentos de marketing, verá que el campo CardCode siempre es 4.
¿Por qué es importante? El número de artículo de un campo es común en todos los tipos de documentos con la misma estructura, como documentos de compras o de ventas. En estos documentos, los números de artículo son iguales, pero los nombres de las tablas difieren. Al utilizar el número de artículo en lugar del nombre de campo puede escribir consultas que sirven en varias clases de documento, haciendo referencia al mismo número de artículo.
En la captura de pantalla inferior de la diapositiva, puede ver que el campo ItemCode en el documento matriz de pedido de cliente tiene el número de artículo 38 y el número de columna 1. El número de línea 1 indica la primera línea del documento (es decir, los números de línea comienzan por 1).
Verá que el número de artículo y de columna de un campo de línea es el mismo en tipos de documentos similares, por ejemplo, el campo ItemCode tiene el número de artículo 38 y el número de columna 1 en todos los documentos de ventas y de compras.

<!-- Slide number: 9 -->
# Información del sistema - Campos calculados

Los nombres de campo y tabla no se visualizan en la información del sistema para los campos que incluyen el símbolo de moneda en la visualización de documentos (p. ej., totales e impuestos)
Para utilizar estos campos en una consulta:
Utilice el número de artículo
Vea las tablas de base de datos de referencia


### Notes:
Verá que el nombre de tabla y de campo no se visualiza en algunos campos, incluido los campos de precio por unidad y los campos calculados como totales e impuestos. Estos campos se muestran en el documento concatenados con el símbolo de moneda, mientras que en la base de datos el importe se almacena sin el símbolo de moneda.
Aún puede utilizarlos en una consulta. Puede utilizar el número de posición para consultar el campo, o puede obtener el nombre de campo de la base de datos desde la referencia de tables de base de datos.

<!-- Slide number: 10 -->
# Referencia de tablas de base de datos


Acceda al fichero REFDB desde el SDK de SAP Business One > Ayuda o desde el menú de ayuda de DTW
Muestra:
Longitud máxima de un campo
Tipo
Valor por defecto (si existe)
Restricciones (valores permitidos)

### Notes:
Puede encontrar el fichero de Referencia de tablas de base de datos REFDB en la carpeta SDK de SAP Business One > Ayuda, o bien, si ha instalado el Workbench de transferencia de datos puede abrirlo desde el menú de ayuda.
Además de los nombres de campo de un objeto, el archivo de referencia proporciona:
La descripción
El tipo de campo (por ejemplo, Int, VarChar, Numeric, Text, etc.)
La longitud máxima de un campo
Si el campo es una clave externa, hay un enlace a la tabla relacionada
Un valor por defecto si existe.
Restricciones en los valores de campo

<!-- Slide number: 11 -->
# Herramientas de consulta


### Notes:
SAP proporciona dos herramientas de consulta que le ayudan a desarrollar la sintaxis de consulta.

<!-- Slide number: 12 -->
# Herramientas de consulta
Las herramientas para crear consultas de usuario se ubican en el menú Herramientas > Consultas

Generador de consultas
Asistente de consultas


### Notes:
Las herramientas para crear y gestionar consultas de usuario se ubican en el menú Herramientas de la barra de menús superior de la aplicación del cliente.
SAP Business One proporciona dos herramientas, el Generador de consultas y el Asistente de consultas para ayudarle a crear consultas utilizando el lenguaje de consulta estructurado (SQL). SQL es un conjunto estandarizado de comandos para formatear y acceder a datos de bases de datos relacionales. Al final, ambas herramientas generan los mismos resultados, y la herramienta que se vaya a utilizar es simplemente una cuestión de preferencia.

<!-- Slide number: 13 -->
# Asistente de consultas
Asistente de varios pasos



Seleccione Finalizar para mostrar y ejecutar la consulta

### Notes:
Como su nombre indica, el asistente de consulta le guía paso a paso a través del proceso de creación de una consulta sin tener que escribir los comandos y la sintaxis SQL. Utilice esta herramienta si no tiene mucha experiencia con SQL. El asistente de consultas es un asistente de varios pasos.
Para ejecutar una consulta desde el asistente de consultas, en el paso final y seleccione el botón Finalizar.
La consulta generada y los resultados de la consulta aparecen en la ventana de vista previa de la consulta.

<!-- Slide number: 14 -->
# Ejemplo de consulta con Asistente de consultas

Para generar la consulta con el asistente:
Pulse Tab para visualizar y seleccionar el nombre de la tabla
En el siguiente paso, pulse el tabulador en cada fila para seleccionar un campo de la lista
En el paso final del asistente, se genera la consulta



Consulta generada:
SELECT T0."DocNum" AS “Document Number", T0."CardCode" AS "Customer/Vendor Code", T0."CardName" AS "Customer/Vendor Name", T0."DocTotal" AS "Document Total"
FROM  “OPOR" T0

### Notes:
En el primer paso del asistente, pulse Tab para visualizar la lista de tablas de base de datos y seleccione la tabla requerida (se muestran las tablas correspondientes y se pueden seleccionar).
A continuación, en el siguiente paso, pulse Tab para visualizar y seleccionar los campos. Se muestran todos los campos de la tabla y puede introducir nombres parciales en el campo Buscar. Haga doble clic en un campo para seleccionarlo para la consulta. Seleccione cada campo en una fila separada en el paso del asistente.
El sistema genera las sentencias SQL en segundo plano por lo que no requiere un conocimiento preciso de la sintaxis SQL. Sin embargo, debido a que esto lo hace un asistente, una consulta se realizará en varios pasos.
También resultará más fácil utilizar el asistente de consultas si no está muy familiarizado con las tablas de SAP Business One y cómo se relacionan entre sí. Cuando selecciona una tabla, el asistente de consultas le muestra todas las tablas que se relacionan con la tabla seleccionada, lo que le permite seleccionar datos de varias tablas. Si selecciona varias tablas para la consulta, el asistente se ocupará de las combinaciones de tabla.
En la diapositiva se muestra la sintaxis de la consulta generada.

<!-- Slide number: 15 -->
# Generador de consultas
Interfaz de paso individual para crear una consulta



Seleccione Ejecutar para ejecutar la consulta

### Notes:
La segunda herramienta, el Generador de consultas, le permite crear el SQL en una sola pantalla. Si posee algunos conocimientos básicos de SQL, encontrará el generador de consultas mucho más rápido que el asistente de consultas.
Seleccione las tablas y, a continuación, los campos y la consulta se mostrará en la parte derecha de la ventana.
Para ejecutar la consulta creada en el generador de consultas, seleccione el botón Ejecutar.
Los resultados de la consulta aparecen en la ventana de vista previa de la consulta.

<!-- Slide number: 16 -->
# Ejemplo de consulta con Generador de consultas

Para generar la consulta con el generador de consultas:
Introduzca el nombre de la tabla, o pulse Tab para ver la lista de tablas
Haga doble clic para seleccionar cada campo de la lista mostrada; los elementos de la consulta se integran y muestran en la parte derecha.

SELECT T0."DocNum", T0."CardCode", T0."CardName", T0."DocTotal" FROM OPOR T0 WHERE T0."DocStatus" ='O' ORDER BY T0."DocDate"

### Notes:
Para generar la consulta, introduzca el nombre de la tabla en el cuadro de texto en la parte superior izquierda de la ventana, o pulse Tab en esta casilla para ver la lista completa de tablas.
Pulse Tab de nuevo para ver una lista de todos los campos de la tabla. Haga doble clic para seleccionar cada campo de la lista visualizada. Los elementos de la consulta se crean y muestran en la parte derecha de la ventana de herramientas.
Como el Asistente de consultas, el Generador de consultas proporcionará automáticamente la relación interna al seleccionar más de una tabla para una consulta. A pesar de que no se visualiza la lista de tablas relacionadas con la tabla elegida, los campos que hacen referencia a las tablas relacionadas se muestran en negrita. Puede arrastrar y soltar el campo en negrita en la columna de selección de tabla y el Generador de consultas abrirá la tabla relacionada, permitiéndole seleccionar campos de dicha tabla.

<!-- Slide number: 17 -->
# Ventana de vista previa de consulta

La ventana Vista previa de consulta muestra la sintaxis de la consulta y los resultados
La sintaxis SQL generada por las herramientas de consulta integradas depende de la base de datos subyacente, ya sea la base de datos SQL Server o SAP HANA. No obstante, los resultados serán los mismos.
En la Vista previa de consulta tiene la opción de editar la consulta, o escribir su propia consulta desde cero

### Notes:
La ventana Vista previa de consulta muestra la sintaxis de la consulta y los resultados
La sintaxis SQL generada por las herramientas de consulta integradas depende de la base de datos subyacente, ya sea la base de datos SQL Server o SAP HANA. No obstante, los resultados serán los mismos.

Desde la ventana de vista previa de consulta, tiene la opción de editar la consulta creada. Haga clic en el icono del lápiz para editar la sintaxis de la consulta. En el modo de edición puede escribir y ejecutar su propia consulta desde cero.

La ventana de vista previa de consulta también le permite grabar consultas para su reutilización. Esto se tratará más adelante en el curso.

<!-- Slide number: 18 -->
# Sintaxis de la consulta


### Notes:
Las dos herramientas de consulta le ayudan en el desarrollo de la consulta, pero también necesita conocimientos básicos de los elementos que conforman la sintaxis de la consulta SQL.

<!-- Slide number: 19 -->
# Elementos básicos de una consulta
Instrucción Select
Select (campos o cálculo)
Condiciones (Where) (opcional)
Clasificar (Order by) (opcional)
Agrupar por (opcional)

SELECT T0."DocNum", T0."CardCode", T0."CardName", T0."DocTotal" FROM OPOR T0

WHERE T0."DocStatus" ='O’

ORDER BY T0."DocDate"

Nota: SQL no distingue entre mayúsculas y minúsculas, por lo que los comandos no deben estar en mayúsculas.
Todos los ejemplos que se muestran en este curso son para SAP HANA

Ctrl + doble clic para añadir total de filas

### Notes:
Una consulta, o una instrucción SQL existente, contiene uno o más de los elementos básicos enumerados en la diapositiva:
Selección de campos. También puede especificar campos de cálculo que muestren el resultado de una suma, una resta, una multiplicación o una división de dos campos.
Condiciones de selección (cláusula Where)
Clasificar (cláusula Order by)
Agrupar y resumir (cláusula Group by)

La consulta de ejemplo que aparece en la parte superior derecha de la pantalla muestra información de pedidos pendientes que se han añadido en la última semana. La consulta selecciona datos de la tabla de pedidos OPOR. Se muestran los resultados de la consulta, en una simple instantánea de la base de datos. El total de filas no se muestra, aunque puede añadirlo al informe pulsando la tecla Ctrl y haciendo clic dos veces con su ratón.

Tenga en cuenta que SQL no distingue entre mayúsculas y minúsculas, por lo que los comandos no deben estar en mayúsculas. Para nombres de tablas y de campos que contengan letras minúsculas, en la sintaxis de SAP HANA se requiere añadir dobles comillas a los nombres de campo.

Todos los ejemplos de consulta que se muestran en este curso son para SAP HANA Para disponer de una lista de diferencias en la sintaxis SQL para SAP HANA, consulte el documento Mejores prácticas de SQL en la base de datos SAP HANA

<!-- Slide number: 20 -->
# Elementos de consulta – Cláusula Where
SELECT T0."DocNum", T0."CardCode", T0."CardName", T0."DocTotal" FROM OPOR T0

WHERE T0."DocStatus" = 'O’ and T0."DocDate" > ADD_DAYS(Current_Date, -7)

ORDER BY T0."DocDate“

Condiciones (Where) (opcional)
Condiciones fijas
Cálculos y funciones
Variables
Los operadores AND / OR pueden utilizarse para vincular múltiples condiciones

Nota: Para conocer los valores posibles de un campo como DocStatus, puede:
Ejecutar una consulta en la tabla y seleccionar el nombre del campo. En los resultados verá los valores posibles que ya están almacenados en la base de datos.
Ver la Referencia de tablas de base de datos para obtener una lista de los valores permitidos (restricciones).

### Notes:
La cláusula opcional Where le permite filtrar solo los registros que cumplen el criterio especificado. Aunque las herramientas de consulta ayudarán a ensamblar los elementos básicos de la consulta, necesitará algún conocimiento de la sintaxis de SQL para completar la cláusula Where.
En la cláusula Where puede incluir:
Condiciones fijas como comparaciones. Por ejemplo, en la consulta de ejemplo, solo se visualizarán los pedidos pendientes (DocStatus ‘O’).
Cálculos y funciones. En la consulta de ejemplo, hemos añadido un cálculo para incluir solo pedidos contabilizados en los últimos 7 días. Hacemos coincidir al valor de la fecha de contabilización (DocDate) con la fecha actual – 7. La función ADD_DAYS se utiliza para calcular la fecha actual menos 7.
Variables. Las variables se especifican como [%0], [%1], [%2], etc. Cuando incluya una variable, al usuario se le solicitará que introduzca un valor como parámetro al ejecutarse la consulta.

Los operadores AND / OR pueden utilizarse para vincular múltiples condiciones. En la consulta de ejemplo, utilizamos el operador AND ya que deben cumplirse ambos criterios.

Nota: La consulta de ejemplo que se muestra utiliza el campo DocStatus como criterio. En la base de datos, este campo contiene una lista fija de los valores permitidos (restricciones).  Hay dos formas de conocer los valores posibles de un campo como DocStatus:
Ejecutar una consulta en la tabla y seleccionar el nombre del campo. En los resultados verá los valores posibles que ya están almacenados en la base de datos.
Ver la Referencia de tablas de base de datos para obtener una lista de los valores permitidos (restricciones).

<!-- Slide number: 21 -->
# Elementos de consulta – Cláusula Where (cont.)
SELECT T0."DocNum", T0."CardCode", T0."CardName", T0."DocTotal" FROM OPOR T0

WHERE T0."DocStatus" = 'O’ and T0."DocDate" > [%0]

ORDER BY T0."DocDate“
Variables para parámetros [%0] [%1] etc.


### Notes:
Las variables le proporcionan al usuario la flexibilidad de cambiar los parámetros cuando ejecuten la consulta.
Las variables simplemente se definen entre corchetes con %0 como la primera variable, %1 la segunda variable y así sucesivamente.

En el ejemplo, la fecha de contabilización DocDate se utiliza como filtro, pero hemos añadido una condición de variable. Cuando el usuario ejecuta la consulta, se le pide que introduzca una fecha de contabilización. La fecha introducida por el usuario se utiliza en la cláusula Where y se compara con la fecha de contabilización del pedido.  Únicamente se incluye en los resultados de la consulta el registro en el que los datos de contabilización sean mayores que la fecha de parámetro.

<!-- Slide number: 22 -->
# Elementos de consulta - Clasificar
SELECT T0."DocNum", T0."CardCode", T0."CardName", T0."DocTotal" FROM OPOR T0

WHERE T0."DocStatus" ='O‘ and T0."DocDate" > ADD_DAYS(Current_Date, -7)

ORDER BY T0."DocDate“ ASC

Clasificar (Order by) (opcional)
ASC / DESC

### Notes:
Si lo desea, puede clasificar los resultados de consulta añadiendo la cláusula Order by a la consulta.
Los resultados se clasificarán en secuencia ascendente por defecto (ASC) utilizando el campo especificado. En este ejemplo, las filas de resultados (pedidos) se clasifican por fecha de contabilización (DocDate).
Puede clasificar por secuencia descendente añadiendo la palabra clave DESC.
Puede clasificar por múltiples campos, y estos campos pueden ser parte de la cláusula seleccionada u otros campos de cualquiera de las tablas de la consulta.

<!-- Slide number: 23 -->
# Elementos de consulta - Cláusula Group By
Consulta con añadido de la cláusula Group By
Consulta original
SELECT T0."DocNum", T0."CardCode", T0."CardName", T0."DocTotal" FROM OPOR T0

WHERE T0."DocStatus" ='O‘ and T0."DocDate" > ADD_DAYS(Current_Date, -7)

ORDER BY T0."DocDate"
SELECT Count (T0."DocNum") as "Total # of POs", T0."CardCode", T0."CardName", SUM(T0."DocTotal") as "Total Amount" FROM OPOR T0

WHERE T0."DocStatus" ='O' and T0."DocDate" >ADD_DAYS(Current_Date, -7)

GROUP BY T0."CardCode", T0."CardName"

Los resultados se consolidan por proveedor (CardCode), con una fila para cada proveedor con el recuento y la cantidad total de todos los pedidos pendientes


### Notes:
La cláusula opcional Group By permite visualizar los resultados de consulta agrupados o resumidos por un campo especificado, por ejemplo, por interlocutor comercial. En el ejemplo, la consulta original se volvió a escribir para utilizar el elemento Group By y se visualiza junto a la consulta original en la diapositiva.
Los resultados agrupados se recopilan en conjuntos por medio del campo o los campos Agrupar por como el valor común.
Group by generalmente se utiliza junto con una función matemática, como Count o Sum.  En la misma consulta, la función Count cuenta el número de PO y la función SUM calcula el total del documento de cada PO.

Los campos seleccionados se consolidan de acuerdo con los campos especificados en la cláusula Group by, por lo que en la consulta de ejemplo los resultados se consolidan por proveedor (CardCode) y la consulta muestra una fila consolidada por cada proveedor, con el recuento y la cantidad de todos los pedidos pendientes para el proveedor.

Tenga en cuenta que deben proporcionarse las cabeceras de columna de los campos contados y sumados, ya que las cabeceras de columnas para estos campos no se encuentran en la base de datos.

Al utilizar la cláusula Group by, los campos que utiliza en la instrucción Select también deben aparecer en la cláusula Group by o en la función de agregado (Count o SUM). Por ese motivo, hemos especificado el campo CardName en la cláusula Group by.

<!-- Slide number: 24 -->
# Alias y relaciones entre tablas
SELECT T0."DocNum", T0."CardCode", T0."CardName", T0."DocTotal", T1."Balance", T1."ListNum"

FROM OPOR T0  INNER JOIN OCRD T1 ON T0."CardCode" = T1."CardCode"

WHERE T0."DocStatus" = 'O'
Si utiliza más de una tabla para una consulta, normalmente tendrá que crear relaciones entre ellas.
Las herramientas de consulta le suministran relaciones automáticamente
Se añade un alias (T0, T1, etc.) para identificar cada tabla

Desde OCRD


### Notes:
Si especifica más de una tabla en su consulta, normalmente tendrá que crear relaciones entre ellas. Las herramientas Asistente de consultas y Generador de consultas facilitan el suministro automático de la relación interna cuando selecciona más de una tabla para una consulta. Por ejemplo, si selecciona la tabla de pedidos (OPOR) y la tabla de datos maestros de interlocutores comerciales (OCRD), las herramientas de consulta enlazarán dichas tablas por medio del código de interlocutor comercial, que es común a ambas tablas.

Las herramientas de consulta añaden automáticamente un alias para cada tabla, por ejemplo, T0, T1, etc. Si la consulta hace referencia a más de una tabla, esto ayuda a identificar la tabla correspondiente para un campo.

Cuando selecciona una tabla, el Asistente de consultas muestra todas las tablas que se relacionan con la tabla seleccionada. En el Generador de consultas, los campos clave para las tablas relacionadas se muestran en negrita. Puede arrastrar y soltar el campo en negrita en la columna de selección de tabla y el Generador de consultas abrirá la tabla relacionada, permitiéndole seleccionar campos de dicha tabla.

<!-- Slide number: 25 -->
# Cabeceras de columna del informe
Cuando se ejecuta una consulta, las cabeceras para las columnas del informe se toman de los nombres de columna de la base de datos


Para modificar la cabecera de columna por defecto en el Generador de consultas, utilice la palabra clave "as" en la consulta con el nuevo texto de cabecera entre comillas dobles
Para modificar la cabecera de la columna por defecto en el Asistente de consulta, escriba el texto que desee en la columna Cabecera



Asistente de consultas
Generador de consultas

### Notes:
Cuando se ejecuta la consulta, las cabeceras para las columnas del informe se toman de los nombres de columna de la base de datos. Para cambiar una cabecera de columna en el informe de consulta:
En el Asistente de consultas, introduzca simplemente el texto deseado en la columna Cabecera de la pantalla del asistente.
En el Generador de consultas, utilice la palabra clave “as” seguida del nuevo texto de cabecera en comillas dobles. Introduzca este texto directamente en el cuadro Select.

<!-- Slide number: 26 -->
# Sintaxis de consulta – Ventana activa
Las consultas que se utilizarán en procesos de autorización y con valores definidos por el usuario tienen que hacer referencia a campos en la ventana activa en la que trabaja el usuario

Para hacer referencia a un campo en la ventana activa, incluya un símbolo $ y corchetes alrededor del nombre de tabla y campo

Ventana activa

Ejemplo:
Select T0."Balance" FROM OCRD T0
INNER JOIN ORDR T1 ON T0."CardCode" = T1."CardCode" WHERE ($[ORDR."CardCode"] =  T0."CardCode")

### Notes:
En muchos casos, la consulta necesita hacer referencia a campos de la ventana activa. En el ejemplo, la ventana activa se identifica mediante una línea azul en la parte superior del formulario o documento.
Esto se produce para consultas utilizadas en procedimiento de autorización y con valores definidos por el usuario. En estas dos situaciones, la consulta se ejecuta mientras un usuario está procesando un documento en la ventana activa.

Si una consulta tuviera que hacer referencia a un campo de la ventana activa en lugar de la base de datos, debe incluir un símbolo $ y colocar corchetes alrededor del nombre de tabla y campo para indicar que el campo se encuentra en la ventana activa.

En el ejemplo mostrado, se ha añadido una consulta como valores definidos por el usuario en un campo del pedido de cliente. La consulta buscará el saldo de la cuenta del cliente en el registro de datos maestros y lo visualizará en el campo definido por el usuario en el pedido de cliente. El pedido de cliente es la ventana activa porque el usuario está trabajando en ella, por lo que la referencia a CardCode incluye la sintaxis especial. La consulta hace coincidir CardCode de la ventana activa con CardCode en los datos maestros.
El registro de datos maestros en este ejemplo no está en la ventana activa. Los campos a los que se accede desde la base de datos, tales como el campo de saldo del registro de datos maestros, no requieren el símbolo $.

Para obtener más información sobre las consultas y los procesos de aprobación, consulte el curso Procesos de aprobación . Para obtener más información sobre las consultas y los valores definidos por el usuario, consulte el curso Valores definidos por el usuario.

<!-- Slide number: 27 -->
# Sintaxis para referencia a ventana activa
Para hacer referencia a los campos de la ventana activa, puede utilizar la sintaxis de nombre de tabla y campo o la sintaxis de número de artículo y columna.
 Número de artículo y columna
Nombre de tabla y campo

Barra de estado
[... Artículo= ##  Columna= ## ….   Nombre de tabla, Nombre de campo]
Ejemplo de nombre de tabla y campo:

Esta consulta se puede utilizar en un modelo de aprobación para la aprobación de pedidos
En SAP HANA SQL, si no hay ninguna cláusula FROM en la sentencia, utilice FROM DUMMY.

SELECT ‘true’ from DUMMY
WHERE
$[OPOR.DocType] = ‘S’ and $[OPOR.DocTotal] > 500

### Notes:
Cuando hace referencia a un campo en la ventana activa, puede utilizar la sintaxis de nombre de tabla y campo o la de número de artículo y columna.
En la diapositiva se muestra un ejemplo de una consulta utiliza en un proceso de aprobación. Si utiliza la sintaxis de nombre de tabla y campo, la consulta incluirá un nombre de tabla que solo pueda utilizarse con un tipo de documento individual. En ese caso, la consulta solo se puede ejecutar para autorizar pedidos ya que la tabla OPOR se incluye explícitamente en la consulta.

Nota: Las consultas utilizadas en procesos de aprobación siempre deben seleccionar un resultado real. En SAP HANA SQL, si no hay ninguna cláusula FROM en la sentencia, utilice FROM DUMMY.

<!-- Slide number: 28 -->
# Sintaxis para referencia a ventana activa
Si utiliza la sintaxis de columna y artículo, el campo se devuelve como un string y deberá especificar un formato alternativo después del número de columna:
 Número de artículo y columna
Nombre de tabla y campo

$[$ Número de artículo. Número de columna.0]
                                                          .Número]
                                                          .Moneda]
                                                          .Fecha]
[... Artículo= ##  Columna= ## ….   Nombre de tabla, Nombre de campo]

Ejemplo de número de artículo y columna:

Esta consulta se puede utilizar en un modelo de aprobación para su aprobación de varios documentos de compras y ventas
En SAP HANA SQL, si no hay ninguna cláusula FROM en la sentencia, utilice FROM DUMMY.

SELECT ‘true’ from DUMMY
WHERE
$[$3.0.0] = ‘S’ and $[$29.0.number] > 500

### Notes:
Si, en su lugar, utiliza la sintaxis de número de artículo y columna, la consulta se puede utilizar con varios tipos de documentos de una estructura similar. Por ejemplo, esta consulta puede utilizarse en un proceso de autorización con varios documentos de marketing de compras y ventas seleccionados en el modelo de autorización.
El sistema identifica de forma exclusiva cada campo de un documento utilizando el número de índice y de columna del campo.
Al hacer referencia a un campo de cabecera mediante la sintaxis de artículo y de columna, especifique el número de columna como 0.
El campo se extrae como una cadena, por lo que si necesita un formato diferente, tiene que especificar el formato después del número de columna:
0 - que es el formato de cadena por defecto
Número – que devuelve el resultado como un valor numérico que puede utilizar en operadores de cálculo o relacionales. En el ejemplo de la diapositiva, el resultado se compara con 500. Ya que el campo DocTotal contiene la cantidad y el símbolo de moneda, la especificación del valor numérico aquí extraerá la cantidad.
Moneda – que devuelve el símbolo de moneda de un campo que contiene la cantidad y el símbolo de moneda, como el DocTotal.
Fecha – que solo debe utilizarse si el campo es un campo de fecha. La fecha se devuelve en un formato que pueda utilizarse en operadores de cálculo o relacionales.

<!-- Slide number: 29 -->
# Grabado y gestión de consultas


### Notes:
Después de crear una consulta, es posible que desee grabarla para su reutilización.

<!-- Slide number: 30 -->
# Grabado de una consulta
La consulta se puede grabar desde la ventana de vista previa de la consulta
Las consultas grabadas pueden ejecutarse desde: Herramientas > Consultas de usuario > Categoría > Nombre de consulta


Grabar la consulta
Proporcione un nombre, seleccione una categoría y Grabe

### Notes:
Puede grabar una consulta desde la ventana de vista previa de la consulta. Cuando grabe una consulta, debe seleccionar una categoría. Se proporciona la categoría General, aunque si tiene previsto añadir muchas consultas de usuario, debe crear categorías adicionales para gestionar las consultas.

Las consultas que graba se consideran como Consultas de usuario. Para ejecutar una consulta de usuario grabada, seleccione el menú Herramientas en SAP Business One y posteriormente la categoría y el nombre de consulta.

<!-- Slide number: 31 -->
# Gestor de consultas
Herramientas > Consultas > Gestor de consultas
Grabe y organice consultas por categoría
Elimine consultas



Cree una nueva categoría

### Notes:
Como su nombre indica, el Gestor de consultas le permite gestionar las consultas de usuario que grabe.
Puede grabar y organizar las consultas por categoría. También puede eliminar consultas.
La categoría Sistema es para las consultas proporcionadas por SAP. La categoría General se proporciona para que pueda grabar las consultas de usuario y crear más categorías.
Para crear una nueva categoría, seleccione el botón Gestionar categorías. A continuación, seleccione Añadir para añadir la nueva categoría y grabe la consulta. En este ejemplo crearemos una nueva categoría denominada Compras.

<!-- Slide number: 32 -->
# Grupos de autorización de consulta
Grupos de autorización de consulta
Autorización de usuarios
Categorías de consulta

|  | General |
| --- | --- |
|  | Ventas Pedidos por empleados de ventas |
|  | Compras Stock cercano al umbral mínimo Más de 5.000 pedidos de servicio PO durante la última semana . . . |
|  | Alertas |
|  |  |  |
| --- | --- | --- |

| Bill, Donna |  |
| --- | --- |
| Sophie, Tim |  |
| --- | --- |
|  |  |  |
| --- | --- | --- |

| Julie, Juan |  |
| --- | --- |

### Notes:
Cuando crea una nueva categoría, debe asignarla al menos a un grupo de autorización de consulta o no podrá grabar la nueva categoría.

Sólo los usuarios que tienen acceso a un determinado grupo de autorización de consulta pueden ejecutar las consultas grabadas para la categoría. Esto ofrece una forma de controlar qué usuarios pueden acceder y ejecutar la consulta de usuario grabada.

Veamos el siguiente ejemplo:
Puede ver que los grupos de autorización de consulta 1 y 2 están asignados a la categoría de consulta Ventas. Los grupos de autorización de consulta 2 y 3 están asignados a la categoría Compras.
Los usuarios Bill y Donna están asignados al grupo de autorización de consulta 1.
Los usuarios Sophie y Tim están asignados al grupo de autorización de consulta 2.
Julie y Juan están asignados al grupo de autorización de consultas 3.

Por lo tanto, Bill y Donna pueden ejecutar todas las consultas grabadas en la categoría Ventas a través de su asociación con el grupo de autorización de consulta 1. Sophie y Tim pueden ejecutar todas las consultas grabadas en las categorías Ventas y Compras ya que ambas categorías se asocian con el grupo de autorización de consulta 2. Y Julie y Juan puede ejecutar todas las consultas grabadas en la categoría Compras que se asocia con el grupo de autorización de consulta 3.

<!-- Slide number: 33 -->
# Autorización de usuario en la categoría de consulta
En la ventana Autorizaciones generales , asigne cada usuario al grupo de la categoría - la autorización es:
Informes > Generador de consultas > Consultas grabadas – Nº de grupo 1-15

Existen 15 grupos de autorización de consulta predefinidos
Puede añadir sus propios grupos de autorización mediante el Gestor de consultas
Puesto que la autorización se concende en el nivel de categoría, el usuario Bob puede ejecutar cualquier consulta grabada en una categoría que se asocie con uno de los grupos de autorización seleccionados

### Notes:
Se le proporciona a un usuario autorización a un grupo de autorización de consulta en la ventana Autorizaciones generales. Encontrará la autorización en Informes > Generador de consultas. Se visualizan 15 autorizaciones de consulta - Consultas grabadas – Grupo 1 -15. Se proporcionan lista para utilizar. Puede crear grupos de autorización de consulta adicionales en el Gestor de consultas.

En el ejemplo de la diapositiva, se le proporciona al usuario Bob permiso a los grupos de autorización 1 y 2, de solo lectura. También se le concede al mismo usuario la autorización total para el grupo llamado "Consultas de usuario para alertas", que es un nuevo grupo de autorización que se ha agregado a la lista.

Puesto que la autorización se concede a nivel de categoría, el usuario Bob puede ejecutar cualquier consulta grabada en una categoría que se asocie con uno de los grupos de autorización seleccionados.

Si desea asegurar el acceso a las consultas de usuario grabada, debe planificar cuidadosamente las categorías de consulta y los grupos de autorización de consulta.

Tenga en cuenta que los grupos de autorización de consultanoson  los mismos que los grupos de usuarios de autorización utilizados para asignar autorizaciones generales a varios usuarios. Para obtener más información sobre autorizaciones generales, consulte el tema relacionado Autorizaciones generales y Grupos de usuarios. También puede asignar la autorización de forma simultánea a varios usuarios desde un Grupo de usuarios.

<!-- Slide number: 34 -->
# Otras autorizaciones de consulta
Las autorizaciones generales también son necesarias para:
Crear nuevas consultas (Generador de consultas)
Crear y editar categorías de consulta
Utilizar la herramienta Asistente de consultas
Ejecutar el Gestor de consultas
Programar la ejecución de una consulta de usuario grabada


### Notes:
Los nuevos usuarios, a menos que sean superusuarios, no tienen autorización para crear nuevas consultas de usuario o categorías de consulta. Se ha diseñado así para proteger la información de la base de datos.  Las autorizaciones necesarias son:
Nuevas consultas: crear nuevas consultas utilizando el Generador de consultas
Crear/editar categorías: crear y editar categorías en el Gestor de consultas
Asistente de consultas: Utilizar la herramienta de consulta
Gestor de consultas: Utilizar el Gestor de consultas para gestionar consultas grabadas
Programación del informe: Programar una consulta grabada como un informe

Nota: Para ver los paneles y las vistas interactivas en SAP HANA, es necesario fijar las autorizaciones del área temática Análisis.

<!-- Slide number: 35 -->

# Puntos clave
Puntos clave de este tema:
Las consultas SQL se pueden utilizar en informes ad hoc, con alertas de usuario y procedimientos de autorización, y para validar los datos migrados de las tablas
Ver  Información del sistema puede ayudarle a identificar los nombres de tablas y de campos o los números de artículo y columna para utilizarlos en consultas
Existen dos herramientas para ayudarle a crear consultas SQL, el Asistente de consultas y el Generador de consultas
Puede grabar consultas como consultas de usuario y organizarlas por categoría
Los usuarios necesitan autorización para ejecutar las consultas de usuario grabadas. Seleccione primero grupo de autorización de consulta para la categoría y, a continuación, asigne un usuario al grupo de autorización de consulta de la categoría en la ventana Autorizaciones generales
Se utiliza una sintaxis especial para consultas que se ejecutan mientras se está procesando un documento en la ventana activa.

### Notes:
Estos son algunos puntos clave de esta sesión. Tómese un momento para revisar estos puntos clave:
Las consultas SQL se pueden utilizar para crear informes ad hoc, como primer paso para diseñar un informe más complicado, con alertas de usuario y procedimientos de autorización, y durante el proyecto de implementación para validar datos migrados importados en tablas.
La información del sistema puede ayudarle a identificar nombres de tablas y de campos o números de artículos y columnas. Con el comando Ver > Información del sistema, visualice la información del sistema.
Existen dos herramientas para ayudarle a crear consultas SQL, el Asistente de consultas y el Generador de consultas. Pruebe ambas para ver cuál prefiere.
Puede grabar consultas como consultas de usuario y organizarlas por categoría. El Gestor de consultas le permite organizar y gestionar las consultas de usuario grabadas.
Los usuarios necesitan autorización para ejecutar las consultas de usuario grabadas. Seleccione primero un grupo de autorización de consulta para la categoría en la que se grabado la consulta y, a continuación, asigne un usuario al grupo de autorización de consulta de la categoría en la ventana Autorizaciones generales.
Se utiliza una sintaxis especial para consultas que se ejecutan mientras se está procesando un documento en la ventana activa. Esto se aplica principalmente a las consultas utilizadas en procesos de aprobación.

<!-- Slide number: 36 -->
# Thanks!
You have completed the topic for Queries.
Thank you for your time!

### Notes:
You have completed the topic for queries in SAP Business One.  Thank you for your time!

<!-- Slide number: 37 -->
