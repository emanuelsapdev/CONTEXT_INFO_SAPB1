<!-- Slide number: 1 -->

# Compras: Problemas con las entradas de mercancías de pedido

SAP Business One
Versión 10.0

### Notes:

Le damos la bienvenida al curso Problemas con las entradas de mercancías de pedido.

<!-- Slide number: 2 -->

# Objetivos
Al finalizar este tema, podrá:
Describir las opciones disponibles para la recepción de entregas incorrectas por parte de un proveedor.

### Notes:
En este tema, exploraremos cómo recibir los envíos incorrectos de un proveedor en un documento Entrada de mercancías de pedido.

<!-- Slide number: 3 -->

# Escenario empresarial
A veces, su proveedor solo entrega una orden parcial.
Otras veces, el proveedor entrega demasiado de un artículo.
Cualquiera sea el caso, se hace un seguimiento del monto entregado para asegurarse de que reciba una factura correcta.

### Notes:
En algunos casos su proveedor sólo entrega un pedido parcialmente y en otras ocasiones una gran cantidad de un artículo.  Cualquiera sea el caso, se hace un seguimiento del monto entregado para asegurarse de que reciba una factura correcta.

<!-- Slide number: 4 -->
# Inconvenientes en la entrada de mercancías




Muy poca cantidad
Demasiada cantidad
Artículos sustituidos


### Notes:
Algunas veces los proveedores entregan cantidades mayores o menores de un artículo. Es posible que un proveedor envíe un artículo diferente del que se solicitó originalmente. En esos casos puede ajustar la entrada de mercancías de pedido según corresponda para reflejar la cantidad que se recibió realmente.
Examinaremos las opciones disponibles en SAP Business One para resolver los inconvenientes que surgen en la entrada de mercancías.
En primer lugar, veremos cómo puede gestionar una cantidad pequeña creando una entrada de mercancías de pedido para una cantidad parcial.
En segundo lugar, veremos cómo se puede incrementar la cantidad en una entrada de mercancías de pedido cuando recibe una cantidad muy grande.
En tercer lugar, veremos cómo añadir nuevos artículos al recibir artículos sustituidos.

<!-- Slide number: 5 -->
# Entregas parciales
Entrada de mercancías de pedido

Pedido de compra
Prov.
Y1000

Prov.

Y1000
N.º
1	Art. A	6
2
3

1ª entrega parcial

1

N.º
1	Art. A	10
2	Art. B	15
3	Art. C	  2

Entrada de mercancías de pedido

   2ª entrega parcial
Prov.
Y1000

Más adelante, cuando el proveedor haga una entrega  posterior, se puede hacer referencia al pedido de nuevo.
N.º
1	Art. A	4

### Notes:
Más adelante, cuando el proveedor haga una entrega posterior, se puede hacer referencia al pedido una segunda vez.
 Se puede hacer referencia a un pedido las veces que sea necesario, siempre que el estado sea Pendiente.

<!-- Slide number: 6 -->
# Entregas parciales
Entrada de mercancías de pedido

Pedido de compra
Prov.
Y1000

Prov.

Y1000
N.º
1	Art. A	6
2
3

1

N.º
1	Art. A	10
2	Art. B	15
3	Art. C	  2

Entrada de mercancías de pedido

Prov.
Y1000

No se esperan entregas adicionales: Cerrar el pedido
El pedido continúa en el sistema, pero no se puede copiar
El pedido aparece en el informe de análisis de compras
Opción para cerrar una línea en lugar de cerrar todo el documento

N.º
1	Art. A	4

### Notes:
Si no espera recibir entregas adicionales de una cantidad de artículos que aún no recibió, debería cerrar el pedido para reducir la cantidad del pedido pendiente. El estado del pedido cambiará a Cerrado.
El sistema cierra automáticamente un pedido cuando se reciben todas las mercancías. Si se recibió un pedido parcial o si no se recibió, puede cerrarlo manualmente.  No se borra el pedido para que se pueda visualizar o duplicar el documento, pero no está más disponible para copiar a otro documento, como una entrada de mercancías, devolución de mercancías o factura de proveedores.
Otra opción es cancelar un pedido. Esta opción se usa generalmente cuando no se recibirán artículos en un pedido.
Puede cancelar un pedido que nunca se ha copiado.  Al igual que con el estado Cerrado, un pedido Cancelado no se elimina.  Puede visualizar o duplicar el documento, pero no puede copiarlo a otro documento.
No aparece un pedido cancelado en el informe del análisis de compra, en tanto que aparecerá un pedido cerrado.
También puedes elegir una fila en particular y no el documento completo.

<!-- Slide number: 7 -->
# Entrega de una cantidad mayor
Puede aumentar las cantidades copiadas para reflejar la cantidad recibida real.

Pedido de compra
Pedido entrada de mercancías

Y1000
Y1000
Prov.
Prov.

N.º
1	Art. A	  10
	Art. B	  15

N.º
1	Art. A	  10
2	Art. B	  20

### Notes:
A veces los proveedores entregan cantidades mayores de un artículo.
Cuando hace referencia a un documento de un pedido mientras ingresa, puede aumentar la cantidad que se copia para reflejar la cantidad actual que se entregó.

<!-- Slide number: 8 -->
# Sustitución de artículos

Pedido de compra
Entrada de mercancías de pedido

Y1000
Y1000
Prov.
Prov.

N.º
1	Art. A	  10
	Art. B	  15
3	Art. C	    1

N.º
1	Art. A	  10
2	Art. B	  15
3
4

Dos artículos recibidos, aunque no se ha entregado un tercero.

### Notes:
Un proveedor puede enviar un artículo distinto del que se solicitó originalmente, quizás para sustituir un artículo que no estaba en stock.
En el gráfico, dos de los tres artículos que se solicitaron se entregaron al proveedor.  Esos dos artículos se copiaron desde el pedido a la entrada de mercancías de pedido.  Sin embargo, el tercer artículo no se entregó.

<!-- Slide number: 9 -->
# Sustitución de artículos

Pedido de compra
Añadir  artículos
Entrada de mercancías de pedido

Y1000
Y1000
Prov.
Prov.


N.º
1	Art. A	  10
	Art. B	  15
3	Art. C	    1

N.º
1	Art. A	  10
2	Art. B	  15
3
4

 3	 Art. D	    1

4

En su lugar, el proveedor envió un artículo de sustitución.
Si el artículo original no se va a enviar, cierre el pedido.
.
Añadir el artículo adicional a la entrada de mercancías de pedido.

### Notes:
En su lugar, el proveedor envió un artículo de sustitución.
Cuando esto sucede, puede añadir el artículo adicional a la entrada de mercancías de pedido.
Si el artículo que se solicitó originalmente nunca se enviará, debe cerrar el pedido original para que ese artículo que no se entregará no continúe apareciendo en los informes de compras como artículo abierto.

<!-- Slide number: 10 -->

# Resumen
A continuación, se detallan algunos puntos clave:
Al crear una entrada de mercancías de pedido con referencia a un pedido, puede copiar todas o algunas de las líneas y ajustar las cantidades para cada línea.
Puede hacer referencia a un pedido pendiente tantas veces como sea necesario.
El sistema cierra automáticamente un pedido cuando todas las líneas tienen una referencia completa.
Si el documento se recibe parcialmente, puede cerrar el documento o cerrar las líneas individuales de forma manual.
Si nunca se recibirán los artículos en un pedido, puede cancelar el documento.
Un pedido cancelado no aparece en el informe del análisis de la compra, a diferencia de uno cerrado.

### Notes:
A continuación, se detallan algunos puntos clave:
Al crear una entrada de mercancías de pedido con referencia a un pedido, puede copiar todas o algunas de las líneas y ajustar las cantidades para cada línea.
Puede hacer referencia a un pedido pendiente tantas veces como sea necesario.
El sistema cierra automáticamente un pedido cuando todas las líneas tienen una referencia completa.
Si el documento se recibe parcialmente, puede cerrar el documento o cerrar las líneas individuales de forma manual.
Si nunca se recibirán los artículos en un pedido, puede cancelar el documento.
Un pedido cancelado no aparece en el informe del análisis de la compra, a diferencia de uno cerrado.
