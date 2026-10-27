<!-- Slide number: 1 -->

# Compras: Conceptos básicos
SAP Business One
Versión 10.0

### Notes:
Le damos la bienvenida al curso sobre los conceptos básicos de compra.

<!-- Slide number: 2 -->

# Objetivos
Al finalizar este tema, podrá:
Enumerar los pasos básicos del proceso de aprovisionamiento
Utilizar un proceso de aprovisionamiento optimizado

### Notes:
En esta sesión, observaremos un resumen del proceso de aprovisionamiento. Al final, podrá enumerar los pasos del proceso de aprovisionamiento y comprar un artículo usando un proceso de aprovisionamiento optimizado.

<!-- Slide number: 3 -->

# Ejemplo empresarial
Su empresa compra artículos de proveedores externos.
Normalmente usted utiliza el proceso de aprovisionamiento completo.
No obstante, en algunos casos, puede realizar el pedido por teléfono y su proveedor entrega los artículos de forma inmediata.

### Notes:
Imagínese que su compañía compra artículos de proveedores externos. Normalmente usted utiliza el proceso de aprovisionamiento completo.
No obstante, a veces, necesita los artículos de inmediato.   Realiza el pedido por teléfono y su proveedor entrega los artículos de forma inmediata.  Para agilizar el proceso no utilice el proceso completo, use sólo un documento de compra para mantener el proceso lo más simple y veloz posible.

<!-- Slide number: 4 -->
# Resumen el proceso de aprovisionamiento




Proceso de cuatro partes básicas: pedir, recibir y pagar para mercancías o servicios.

### Notes:
El proceso de compras no es simplemente realizar un pedido y pagar por lápices y sujetapapeles. En cambio, la compra es el proceso de asegurar que un flujo constante de materiales necesarios llegue a su empresa cuándo y dónde lo necesite. Como una aplicación de gestión empresarial global, SAP Business One lo ayuda a realizar el proceso de compras, empezando con un pedido y siguiendo con el resto de los documentos de compra. SAP Business One captura información automáticamente a cada paso para que siempre conozca lo que hay en el inventario como también el estado financiero actualizado de su empresa. La visualización en tiempo real ayuda a identificar posibles insuficiencias de stock antes de que sucedan. La información precisa del historial ayuda a realizar un seguimiento de los proveedores que siempre cumplieron.
El gráfico muestra los procesos de cuatro partes básicas: pedir, recibir y pagar por las mercancías o los servicios.

<!-- Slide number: 5 -->
# Compra de artículos: Resumen del proceso




El pedido (PO) es el documento que le proporciona al proveedor especificando los artículos o servicios que desea comprar.
Representa su compromiso con el proveedor.

### Notes:
El pedido (PO) es el documento que proporciona al proveedor especificando los artículos o servicios que desea comprar, incluidas las cantidades y los precios acordados.  Representa su compromiso con el proveedor para comprar los artículos.

<!-- Slide number: 6 -->
# Compra de artículos: Resumen del proceso




Entrada de mercancías de pedido es el documento que muestra la entrega de las mercancías de un proveedor.
Se usa para actualizar la cantidad de inventario y los precios.

### Notes:
La entrada de mercancías de pedido es el documento que muestra la entrega de las mercancías del proveedor a la empresa. Se usa para actualizar las cantidades y los valores del inventario.

<!-- Slide number: 7 -->
# Compra de artículos: Resumen del proceso




La factura de proveedores es el documento en el cual Proveedores introduce la solicitud de pago del proveedor.

### Notes:
La factura de proveedores es el documento en el cual su departamento de Proveedor introduce la información de la factura del proveedor para solicitar que se realice un pago al proveedor.

<!-- Slide number: 8 -->
# Compra de artículos: Resumen del proceso




El pago efectuado es el documento que inicia un pago a la cuenta del proveedor.
La funcionalidad y los informes para el procesamiento de pagos pertenecen al módulo Gestión de bancos.

### Notes:
El pago efectuado es el documento que inicia un pago a la cuenta del proveedor. Hay, en general, cuatro formas de efectuar un pago: efectivo, cheques, tarjetas de crédito y transferencias bancarias. También hay disponibles otras formas de pago específicas del país. En SAP Business One, se puede acceder a la funcionalidad y a los informes asociados con el procesamiento de pagos mediante el módulo Gestión de bancos.

<!-- Slide number: 9 -->
# Datos maestros clave en la compra: Proveedor

Contiene:
Cuándo se utiliza:

Todas las transacciones de compra
Transacciones de aprovisionamiento financiero automáticas y manuales

Personas de contacto
Direcciones
Medio de pago
Información contable

Proveedores

### Notes:
Ahora miremos la información sobre los datos maestros claves necesarios para el pedido.  La primera parte de datos maestros necesarios es el proveedor.
El proveedor es uno de los tres tipos de datos maestros de interlocutores comerciales que se mantienen en SAP Business One. Los datos del proveedor identifican quién provee las mercancías y los servicios.
Utilice registros maestros de proveedor en todas las transacciones de compra. El proveedor también se utiliza en las transacciones de aprovisionamiento financiero automáticas y manuales.
El registro maestro de proveedores contiene: detalles de la persona de contacto, direcciones, condiciones de pago y otra información contable.
Puede buscar el proveedor apropiado en cualquier documento de compra. Si está autorizado, también podrá introducir nueva información de proveedor al crear un documento de compra.

<!-- Slide number: 10 -->
# Datos maestros clave en la compra: Artículos

Campos maestros del artículo útiles en la compra
Proveedores preferentes
Número de catálogo del fabricante
Unidad de medida de compra
Dimensiones del artículo
Información fiscal
Grupo aduanero de los artículos importados
Enlace al análisis de compra

### Notes:
Otra parte clave de los datos maestros en el proceso de compra son los datos maestros de artículo. Los datos maestros del artículo identifican lo que se compra.
Con frecuencia, se compran, se incluyen en el inventario y se venden los mismos artículos. La información es la misma, solamente se usa de forma diferente.  Esta es la ventaja de usar un registro maestro de artículo, el cual se puede copiar en cualquier documento de los módulos de compra, venta, producción, MRP, inventario y servicio.
La cabecera del registro de datos maestros de artículo contiene información general acerca del artículo, incluido un número de ID único asignado por el usuario, una descripción (incluida una descripción en un idioma extranjero) y parametrizaciones para determinar el tipo de artículo, el grupo al que pertenece y la lista de precios seleccionada. Las casillas de selección situadas a la derecha indican si el artículo se mantiene en el inventario y si se ofrece para la compra o venta (en muchos casos, ambas opciones son válidas).
La ficha General en la ventana Datos maestros de artículo cuenta con una combinación de información sobre el fabricante del artículo, identificadores adicionales, métodos de envío y método de emisión.
La ficha Datos de compras indica el proveedor usual que vende el artículo, cómo identificar el artículo en un catálogo, las unidades de medida utilizadas para el artículo con fines de compra y las dimensiones del artículo físico.  Se encuentra también disponible la información sobre impuestos y grupos de aduanas para la información importada. Si el artículo cuenta con un historial de compra, puede hacer clic en el icono del gráfico, a la izquierda de la ficha, a fin de visualizar un análisis gráfico de compras.

<!-- Slide number: 11 -->
# Efectos en el inventario y en la contabilidad

Pedido de compra
Entrada de mercancías de pedido
Factura de proveedores




Cuenta de asignación
100
100

Proveedor
100
100

Cuenta de asignación
Cuenta de existencias
Ninguna contabilización

### Notes:
Ahora observemos el proceso de aprovisionamiento y su efecto en el inventario y la contabilidad.
Cuando se crea un pedido, no existen contabilizaciones en el inventario y la contabilidad.
La primera contabilización se realizará cuando se registre una entrada de mercancías de  pedido. La entrada de mercancías de  pedido crea un asiento que contabiliza el valor de las mercancías recibidas en el Debe de la cuenta de stock y en el Haber de la cuenta de costes de asignación.
La cuenta de stock y la cuenta de costes de asignación se recuperan desde el campo Cuenta de inventario y el campo Cuenta de asignación en la ficha Datos de inventario del registro maestro de artículos.
La cuenta de costes de dotación es una cuenta de transferencia que se usa para controlar si las entradas de mercancías de pedidos y las facturas de proveedores coinciden.
El balance total de la cuenta de asignación representa el valor de todas las entradas de mercancías de pedidos pendientes que todavía no se copiaron a una factura de proveedores.
Luego, cuando se contabiliza la factura del proveedor, se cierra la entrada de mercancías de pedido.
En este punto, la factura de proveedores crea un asiento que contabiliza la cantidad facturada en la columna del Debe de la cuenta de costes de asignación y en la columna del Haber de la cuenta del proveedor.
De esta manera, la cantidad en la cuenta de costes de asignación desde la entrada de mercancías pedido está seleccionada y el sistema registra la cantidad que se le debe al proveedor.

<!-- Slide number: 12 -->
# Proceso de aprovisionamiento optimizado
Puede optimizar el proceso de compras mediante una factura de proveedores independiente.

Para órdenes urgentes, omita el pedido y la entrada de mercancías de pedido

La factura de proveedores:
Aumentará el stock
Mostrará lo que se le debe  al proveedor


Cuenta de existencias
Proveedor
100
100

### Notes:
A veces, es posible que deba optimizar o simplificar el proceso de compra para que sea más eficiente.  Quizás necesite obtener un artículo de inmediato.  En ese caso, llame al proveedor y pídale que se lo entregue hoy.  Debido a la urgencia, saltea el pedido.
Cuando se entrega el artículo, también se entrega la factura del proveedor.
Por lo tanto, en lugar de crear una entrada de mercancías de pedido, introduzca una factura de proveedor para procesar la recepción de los artículos en las existencias y la obligación de pagar al proveedor.
En este caso, cuando contabiliza directamente la factura del proveedor sin crear primero una entrada de mercancías de pedido, se omiten las contabilizaciones a la cuenta de costes de dotación.  La contabilización carga la cuenta de stock para mostrar el aumento en las existencias y el Haber a la cuenta del proveedor para mostrar la necesidad de pagarle al proveedor.
Debido a que una factura de proveedor que no hace referencia a una entrada de mercancías de pedido aumentará las existencias, es importante asegurarse de que no haya una entrada de mercancías de pedido anterior si crea una factura de proveedor sin referencia.
