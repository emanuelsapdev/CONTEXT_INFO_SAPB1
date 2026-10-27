<!-- Slide number: 1 -->

# Ventas - clientes: Descripción general del proceso de ventas

SAP Business One
Versión 10.0

### Notes:
Le damos la bienvenida al tema de resumen del proceso de ventas.

<!-- Slide number: 2 -->

# Objetivos
Al finalizar este tema, podrá:
Enumerar los pasos básicos del proceso de ventas
Utilizar un proceso de ventas optimizado

### Notes:
En este tema presentamos el proceso de ventas.  Primero enumeramos los pasos básicos y los datos clave del proceso de ventas y después le mostramos cómo puede optimizar el proceso de ventas de modo que solo haga falta un documento.

<!-- Slide number: 3 -->

# Escenario empresarial
Su empresa estableció que la satisfacción del cliente es su mayor prioridad
Revisa los pasos básicos del proceso de ventas y decide utilizar un proceso optimizado para los pedidos con entrega inmediata para garantizar que las demandas del cliente se cumplan lo más rápido posible.

### Notes:
Imagínese que su empresa estableció que la satisfacción del cliente es su mayor prioridad. Revisa los pasos básicos del proceso de ventas y decide utilizar un proceso optimizado para los pedidos con entrega inmediata para garantizar que las demandas del cliente se cumplan lo más rápido posible.

<!-- Slide number: 4 -->
# Proceso de ventas




El proceso de Ventas- Clientes se traslada de la venta de mercancías (y servicios) a la entrega de dichas mercancías, la facturación al cliente y a la recepción del cobro.

### Notes:
El proceso de Ventas -Clientes, abarca desde la venta de mercancías (y servicios), la entrega de esas mercancías y la facturación al cliente por las compras, hasta el último paso de contabilidad que es la recepción del cobro.
Cada uno de los pasos involucra el uso de un documento, por ejemplo, un pedido de cliente, un documento de entrega o una factura de clientes. SAP Business One transfiere eficientemente la información pertinente de un documento al siguiente durante el flujo de documentos.  Según las necesidades comerciales, puede seleccionar qué documentos incluir como pasos del proceso. El único documento obligatorio en el proceso de ventas es la factura de clientes.
Los documentos de venta contienen, en su mayoría, la misma información durante todo el proceso de ventas. El contenido de este tema le ayudará a reconocer cuál es la información que se repite en cada documento, de modo tal que pueda concentrarse rápidamente sólo en la información que necesita.
Tenga en cuenta que también tiene la opción de usar una oferta para iniciar el proceso de ventas.  La oferta no está incluida en este curso de e-learning.

<!-- Slide number: 5 -->
# Proceso de ventas




El pedido de cliente representa un compromiso de compra del producto o servicio por parte del cliente o cliente potencial, según el precio y las cantidades acordadas.

### Notes:
El pedido de cliente representa un compromiso de compra del producto o servicio por parte del cliente o cliente potencial, según el precio y las cantidades acordadas.

<!-- Slide number: 6 -->
# Proceso de ventas




La entrega indica que se llevó a cabo el envío de las mercancías.

### Notes:
La entrega indica que se llevó a cabo el envío de las mercancías.

<!-- Slide number: 7 -->
# Proceso de ventas




La factura de clientes es el único documento obligatorio en el proceso de ventas.
También representa la solicitud de pago y registra los ingresos en la cuenta de pérdidas y ganancias.

### Notes:
La factura de clientes es el único documento que se debe crear en el proceso de ventas. También representa la solicitud de pago y registra los ingresos en la cuenta de pérdidas y ganancias.

<!-- Slide number: 8 -->
# Proceso de ventas




El cobro recibe el pago del cliente y borra la deuda de la cuenta del cliente.
Los pagos efectuados se realizan en el módulo Gestión de bancos.

### Notes:
El cobro recibe el pago del cliente y borra la deuda de la cuenta del cliente. La reconciliación interna se realiza automáticamente.
Los pagos efectuados se realizan en el módulo Gestión de bancos.
Como parte de un proceso de ventas optimizado, es posible contabilizar un pago y crear la factura.  Para hacerlo, seleccione el icono Medios de pago cuando cree la factura e introduzca el importe del cobro.  Esto creará un importe a pagar de cobro que se aplica a la factura que acaba de crear.

<!-- Slide number: 9 -->
# Datos clave: Interlocutores comerciales
Cada documento en el proceso de ventas debe tener asignado un interlocutor comercial.

Interlocutores comerciales del proceso de ventas:
Clientes potenciales
Clientes

Datos sobre los clientes potenciales y clientes:
Un cliente potencial puede convertirse fácilmente en un cliente.
Los pedidos de cliente pueden tener asignado un cliente o un cliente potencial.
Una vez que pasa a la entrega, debe tener un cliente.


### Notes:
Cada documento en el proceso de ventas debe tener asignado un interlocutor comercial. Los interlocutores comerciales utilizados en el proceso de ventas son clientes potenciales y clientes.  Un cliente potencial puede convertirse fácilmente en un cliente.
Un pedido de un cliente puede tener asignado a un cliente o a un cliente potencial. Una vez que pasa a la entrega, debe tener un cliente.
Los datos maestros de clientes describen a las personas y organizaciones a quienes su empresa les vende productos y servicios. Los registros maestros de datos de clientes se utilizan como base para la creación de documentos relacionados con el procesamiento y cumplimiento de pedidos para clientes y para el asistente para reclamaciones de clientes.

<!-- Slide number: 10 -->
# Datos clave: Artículos

Los artículos representan productos en venta
Los artículos pueden ser tanto para mercancías como para servicios
La información sobre artículos se almacena en el registro maestro de artículo.


### Notes:
Además del interlocutor comercial, otros datos clave que se introducen en el pedido de cliente son los datos del artículo.
Los artículos representan productos en venta, ya sean mercancías o servicios.
Al igual que los datos maestros del cliente, la información de los artículos se almacena en informes de datos maestros.
Los servicios que vende también pueden definirse como informes de datos maestros de artículos.  Si los servicios se definen como artículos, pueden introducirse junto con los artículos físicos en el pedido de cliente.  En caso contrario, utilice el campo Clase de artículo/servicio para cambiar a un documento de servicio en el cual puedan introducirse las descripciones de los servicios y los precios.

<!-- Slide number: 11 -->
# Uso de listas de precios
Conceptos básicos de la lista de precios:
Se proporcionan 10 listas de precios estándar.
Fije los precios para sus artículos en las listas de precios.
Asigne una lista de precios a cada cliente.
La lista de precios asignada aparece automáticamente en el documento de venta.

Lista de precios

Registro maestro de clientes

Documentos de ventas

### Notes:
Cuando introduce un artículo en un documento de ventas, se encuentra automáticamente un precio.  ¿Cómo funciona?
SAP Business One proporciona 10 listas de precios estándar.  Luego, defina los precios para cada lista de precios de sus artículos.  Claro que, no debe usar las diez listas de precios, pero se le proporcionan para que pueda ofrecer diferentes precios a los diferentes grupos de clientes.
Asigna una lista de precios a cada cliente mediante las condiciones de pago estándar.  Sin duda, la lista de precios se puede cambiar en el registro maestro de clientes.
Cuando introduce un cliente en un documento de venta, la lista de precios asignada aparece por defecto en el documento automáticamente.
El sistema usa dicha lista para asignar los precios a los artículos en el pedido.
Sin duda, pueden utilizarse asignaciones de precios más complejas, como precios especiales, grupos de descuento y jerarquías de precios.  Éstas se explican en los temas de e-learning sobre precios.
Los usuarios autorizados pueden modificar los precios en el pedido de cliente. Por ejemplo, un vendedor puede otorgar un 5% de descuento en un artículo específico o en un pedido de cliente completo.

<!-- Slide number: 12 -->
# Factura de clientes en un proceso de ventas optimizado

Factura de clientes:
 El único documento obligatorio en el proceso de ventas.
Diseñada como documento extremadamente eficiente para un negocio pequeño con pocos empleados.
Puede realizar el trabajo de registrar el pedido del cliente, iniciar la entrega, contabilizar la salida de mercancías y registrar lo que el cliente debe.

### Notes:
Para nuestro proceso optimizado, utilizaremos solo un documento: la factura de cliente.
La factura de clientes es el único documento obligatorio en el proceso de ventas.  La factura de cliente está diseñada para ser un documento extremadamente eficiente para pequeños negocios con solo algunos empleados.
La factura de cliente puede realizar el trabajo de registrar el pedido del cliente, iniciar la entrega, contabilizar la salida de mercancías y registrar lo que el cliente debe.

<!-- Slide number: 13 -->
# Contabilizaciones de factura de clientes

Cuando una factura de clientes no posee documentos precedentes, se realizan dos contabilizaciones adicionales
Debe en el coste de los artículos vendidos
Haber en una cuenta de existencias

Grabar una factura de cliente siempre activa dos contabilizaciones:
Debe en la cuenta del cliente
Haber en los ingresos por ventas

Ingresos por ventas

100
Cta. existencias
50

Cta. de gastos
50

Cliente

100

### Notes:
Grabar una factura de cliente siempre activa dos contabilizaciones: un débito a la cuenta del cliente para mostrar lo que se debe y un crédito para los ingresos de ventas.
Cuando un artículo de inventario se vende en una factura de cliente que no posee documentos precedentes, se realizan dos contabilizaciones adicionales.  Estas son las contabilizaciones para sacar el artículo del inventario que generalmente se gestiona por un documento de entrega en un sistema de inventario permanente: un débito para el coste de la cuenta de mercancías vendidas y un crédito para la cuenta de stock.
Sin duda, este gráfico cubre solo las transacciones contables básicas.  Es posible que existan contabilizaciones adicionales para los impuestos o ingresos y gastos adicionales.

<!-- Slide number: 14 -->

# Resumen
A continuación, se detallan algunos puntos clave:
Los documentos principales del proceso de venta son el pedido de cliente, entrega y factura de cliente.  El cobro al final del proceso de venta se lleva a cabo en un módulo bancario.
Todos los documentos de ventas deben tener un interlocutor comercial asignado.
Un documento de ventas puede vender productos o servicios. Las mercancías se representan por los registros maestros de artículos. Si los servicios se representan como artículos, pueden venderse con artículos físicos en documentos de ventas, de lo contrario se venden en documentos de tipo servicio.
SAP Business One calcula la determinación de precios de forma automática en los pedidos de cliente.  La determinación de precios puede modificarse en los documentos de ventas por parte de usuarios autorizados.
El único documento de venta obligatorio es la factura de clientes.  Cuando una factura de cliente se utiliza sola sin documentos precedentes, puede llevar a cabo las funciones del pedido del cliente, entrega y la factura.
La factura de cliente con frecuencia se utiliza en un proceso de ventas optimizado.

### Notes:
Los documentos principales del proceso de venta son el pedido de cliente, entrega y factura de cliente.  El cobro al final del proceso de venta se lleva a cabo en un módulo bancario.
Todos los documentos de ventas deben tener un interlocutor comercial asignado.
Un documento de ventas puede vender productos o servicios. Las mercancías se representan por los registros maestros de artículos. Si los servicios se representan como artículos, pueden venderse con artículos físicos en documentos de ventas, de lo contrario se venden en documentos de venta de tipo servicio.
SAP Business One calcula la determinación de precios de forma automática en el pedido de cliente.  La determinación de precios puede modificarse en los documentos de ventas por parte de usuarios autorizados.
El único documento de venta obligatorio es la factura de clientes.  Cuando una factura de cliente se utiliza sola sin documentos precedentes, esta puede llevar a cabo las funciones del pedido del cliente, entrega y la factura.
Esto es por qué la factura de cliente con frecuencia se utiliza en un proceso de ventas optimizado.
