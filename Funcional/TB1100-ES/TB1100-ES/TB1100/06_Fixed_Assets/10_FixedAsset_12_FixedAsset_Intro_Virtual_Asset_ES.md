<!-- Slide number: 1 -->


# Activos fijos: Activo fijo virtual
SAP Business One
Versión 10.0

### Notes:

Bienvenido al tema Activos fijos virtuales.

<!-- Slide number: 2 -->

# Objetivos
Al finalizar este tema, podrá:
Explicar el proceso de gestión de activos fijos virtuales.

### Notes:
Después de completar este tema, podrá explicar el proceso de gestión de activos fijos virtuales.

<!-- Slide number: 3 -->
# Activo fijo virtual



Activos fijos con la función de artículo virtual:
Permite definir un artículo modelo que representa el activo fijo.
Permite a la empresa comprar activos fijos idénticos en grandes cantidades para uso interno.
Crea automáticamente la misma cantidad de registros de datos maestros de activo fijo y los capitaliza.
Opcionalmente, puede utilizar números de serie para los activos fijos virtuales generados.





### Notes:
Cuando la empresa deba comprar activos fijos idénticos en grandes cantidades para uso interno, cree un artículo virtual que represente el activo fijo.
En la Factura de proveedores seleccione este artículo modelo e indique una cantidad en la línea de artículo.
A continuación, SAP Business One creará automáticamente la misma cantidad de registros de datos maestros de activo fijo y los capitalizará.
Esta función evita tener que indicar manualmente grandes volúmenes de información repetida y, por tanto, mejora la eficiencia de la empresa en la gestión de activos fijos.
Opcionalmente, puede utilizar números de serie para los activos fijos virtuales generados.
Puede utilizar la definición de artículo virtual para los casos en los que la empresa compra activos idénticos para utilizarlos en la oficina, como portátiles, teléfonos móviles o sillas.
Veamos cómo trabajar con activos fijos virtuales.

<!-- Slide number: 4 -->
# Creación de un activo fijo virtual




### Notes:
La casilla de selección Artículo virtual solo está disponible si se utilizan series de numeración para los datos maestros de activo fijo.
Con las series de numeración, el sistema puede crear varios activos nuevos cuando se compra un artículo virtual en una única línea de transacción.
Observe que ambos datos maestros, activo fijo y artículos, utilizan la misma configuración de serie de numeración.
Una vez que define unos datos maestros de activo fijo como artículo virtual, puede empezar a utilizarlo como modelo para comprar una gran cantidad de activos fijos idénticos.
OEC Computers ha definido un artículo virtual para los teléfonos móviles que compran para sus empleados.
Si marca la casilla Forzar números de serie, cuando compre activos fijos mediante artículos virtuales en facturas de proveedores, deberá especificar un número de serie para cada activo fijo generado.

<!-- Slide number: 5 -->
# Capitalización de activos fijos virtuales










Sin Forzar números de serie


### Notes:
Los artículos virtuales solo se pueden capitalizar mediante facturas de proveedores.
La cantidad de los datos maestros de activo fijo creados automáticamente es igual que la cantidad que se ha especificado en la factura de proveedores (en nuestro ejemplo, 9).
Los números de artículo se asignan automáticamente a los datos maestros de activo fijo recién creados, según las reglas que se han definido para las series utilizadas en los datos maestros del activo fijo virtual.
En nuestro ejemplo, cuando OEC Computers indica la cantidad de 9 teléfonos móviles en la fila de factura de proveedores, el sistema crea automáticamente 9 datos maestros de activo fijo, uno para cada teléfono móvil.
La información de los datos maestros de activo fijo del activo fijo virtual se copia en los datos maestros de activo fijo recién creados, excepto la casilla de selección Artículo virtual que está desmarcada.
Los activos creados son activos fijos normales con valores monetarios. El artículo virtual funciona como modelo y, por tanto, no tendrá valores en la ficha Activos fijos.

<!-- Slide number: 6 -->
# Capitalización de activos fijos virtuales

Sin Forzar números de serie


### Notes:
Se emite automáticamente un documento de Capitalización que incluye los activos creados y también un asiento contra la cuenta de activos.
Observe que puede incluir varios activos fijos virtuales en la misma factura de proveedores, pero no puede incluir activos fijos virtuales y activos fijos normales en la misma factura de proveedores.

<!-- Slide number: 7 -->
# Capitalización de activos fijos virtuales

Activo fijo
Artículo de inventario





CON forzar números de serie
LT22005543
LT22005542
LT22005541

### Notes:
Si selecciona forzar números de serie, deberá definir estos números de serie cuando compre los activos en la Factura de proveedores.
En la Factura de proveedores, haga clic con el botón derecho del ratón y seleccione la opción Números de serie de activo fijo. En la ventana Números de serie de activo fijo: Configuración, indique números de serie para cada activo fijo comprado mediante la línea Factura de proveedores.
El resto del proceso es el mismo que se ha descrito en las diapositivas anteriores. La única diferencia es que los datos maestros de activo fijo creados incluirán el número de serie que se ha indicado en la Factura de proveedores. Puede hacer un seguimiento del número de serie en los datos maestros de activo fijo. La Factura de proveedores también incluye los números de serie creados y puede visualizarlos haciendo clic con el botón derecho del ratón en la factura de proveedores.
Observe que no se pueden definir datos maestros de activo fijo como artículo de inventario y, por tanto, no son números de serie regulares. Son números de serie de activo fijo que se graban en los datos maestros de activo fijo con finalidades de seguimiento.

<!-- Slide number: 8 -->

# Capitalización de activos fijos virtuales: Sugerencia




### Notes:
Cuando emita una factura de proveedores, para que resulte más fácil localizar un artículo virtual de la lista de artículos y activos fijos, modifique las opciones de la lista de artículos y visualice el campo Artículo de activo visual.
Para ello, después de abrir la ventana Lista de artículos, seleccione el icono Parametrizaciones de formulario de la barra de menús superior para modificar la visualización de lista.

<!-- Slide number: 9 -->

# Resumen (1/2)
| Cuando la empresa debe comprar activos fijos idénticos en grandes cantidades para uso interno: | Cree un artículo virtual que represente el activo fijo. En la factura de proveedores seleccione este artículo modelo e indique una cantidad en la fila de artículo (los artículos virtuales solo se pueden capitalizar mediante facturas de proveedores). |
| --- | --- |
| Una vez se añade la factura de proveedores con el artículo virtual: | Se crean automáticamente los registros de datos maestros de activo fijo en la misma cantidad que se ha especificado en la línea de factura de proveedores. Se emite automáticamente un documento de Capitalización que incluye los activos creados y también un asiento contra la cuenta de activos. |

### Notes:
Cuando la empresa deba comprar activos fijos idénticos en grandes cantidades para uso interno, cree un artículo virtual que represente el activo fijo.
En la factura de proveedores seleccione este artículo modelo e indique una cantidad en la fila de artículo (los artículos virtuales solo se pueden capitalizar mediante facturas de proveedores)
Una vez se añade la factura de proveedores con el artículo virtual:
Se crean automáticamente los registros de datos maestros de activo fijo en la misma cantidad que se ha especificado en la línea de factura de proveedores.
Se emite automáticamente un documento de Capitalización que incluye los activos creados y también un asiento contra la cuenta de activos.

<!-- Slide number: 10 -->

# Resumen (2/2)
| Algunos datos sobre los activos fijos virtuales: | La casilla de selección Artículo virtual solo está disponible si se utilizan series de numeración para los datos maestros de activo fijo. Si selecciona forzar números de serie para unos datos maestros de activo fijo, deberá definir estos números cuando compre el activo fijo en la factura de proveedores. No se pueden definir datos maestros de activo fijo como artículo de inventario y, por tanto, no son números de serie regulares. Son números de serie de activo fijo que se graban en los datos maestros de activo fijo con finalidades de seguimiento. |
| --- | --- |

### Notes:
Algunos datos sobre los activos fijos virtuales:
La casilla de selección Artículo virtual solo está disponible si se utilizan series de numeración para los datos maestros de activo fijo.
Si selecciona forzar números de serie para unos datos maestros de activo fijo, deberá definir estos números cuando compre el activo fijo en la factura de proveedores.
No se pueden definir datos maestros de artículo de inventario como artículo de inventario y, por tanto, no son números de serie regulares. Son números de serie de activo fijo que se graban en los datos maestros de activo fijo con finalidades de seguimiento.

<!-- Slide number: 11 -->
# Thanks

You have completed the Virtual Fixed Asset topic.
Thank you for your time!

### Notes:
You have completed the Virtual Fixed Asset topic. Thank you for your time.
