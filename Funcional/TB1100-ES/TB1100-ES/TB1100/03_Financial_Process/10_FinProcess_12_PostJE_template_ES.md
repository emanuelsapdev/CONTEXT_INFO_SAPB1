<!-- Slide number: 1 -->

# Proceso financiero: Modelos de contabilización y contabilizaciones periódicas

SAP Business One
Versión 10.0

### Notes:
Bienvenido al tema sobre modelos de contabilización y contabilizaciones periódicas.

<!-- Slide number: 2 -->

# Objetivos
Al finalizar este tema, podrá:
- Definir y utilizar modelos de contabilización
- Definir una contabilización periódica

### Notes:
Al finalizar este tema, podrá:
- Definir y utilizar un modelo de contabilización
- Definir una contabilización periódica

<!-- Slide number: 3 -->

# Escenario empresarial
Implementará SAP Business One en un nuevo cliente.
La responsable de contabilidad le comunica que cada mes graba manualmente dos tipos de asiento.
El primero es una transacción de alquiler con un importe fijo.
El segundo es un pago de complemento salarial para los empleados del departamento de ventas. Cada empleado recibe un porcentaje fijo de los ingresos mensuales.
Le muestra las herramientas Contabilización periódica y Modelo de contabilización que pueden hacer que el proceso sea más eficaz.

### Notes:
Imagine que está implementando SAP Business One a un nuevo cliente.
La responsable de contabilidad le comunica que cada mes graba manualmente dos tipos de asiento.
El primero es una transacción de alquiler con un importe fijo.
El segundo es un pago de complemento salarial para los empleados del departamento de ventas. Cada empleado recibe un porcentaje fijo de los ingresos mensuales.
Le muestra las herramientas Contabilización periódica y Modelo de contabilización que pueden hacer que el proceso sea más eficaz.

<!-- Slide number: 4 -->
# Contabilizaciones periódicas


Código: Alquiler			Descripción: Pago de alquiler
Cuenta de mayor/ Nº IC
Cuenta de mayor/
Nombre IC
Haber

Debe
620000
Alquiler de propiedad
1000

1000
161000
Cuenta de giro bancario


Fin de validez
Frecuencia:
Mensual
El 10
Siguiente ejecución:
01/10/2016
12/10/2021

### Notes:
SAP Business One incluye una función de contabilizaciones periódicas para asientos de importe fijo similares que se crean regularmente.
Las contabilizaciones periódicas utilizan un modelo que se almacena con un código y una descripción. En este modelo debe definir, entre otras cosas, la frecuencia con la que se creará el asiento y una fecha de validez que indique hasta cuándo será válida la contabilización periódica.
Para definir un tipo de modelo de contabilización periódica, utilice la ventana Contabilizaciones periódicas del módulo Finanzas.
El sistema duplica la contabilización periódica original (instancia 0) cada vez que se acerca la fecha de ejecución, y presenta un informe que recomienda contabilizar las operaciones que vencen. Cuando utilice esta instancia y la añada al sistema, esta se borrará.
Puede configurar el sistema para que muestre todas las transacciones periódicas disponibles para su procesamiento en la fecha actual al iniciar sesión. Esta parametrización se realiza en la ventana Parametrizaciones generales en Inicialización del sistema  en el módulo Gestión. En la ficha Servicios, marque la casilla de selección Visualizar contabilizaciones periódicas durante la Ejecución.
Recuerde que puede añadir contabilizaciones periódicas al flujo de caja, que se visualizan en color verde en el informe.

<!-- Slide number: 5 -->
# Opciones para contabilizaciones periódicas


Fin validez
Frecuencia:
Mensual
El 10
Siguiente ejecución:
01/10/2020
12/10/2025

Diaria
Semanal
Mensual
Trimestral
Semestral
Anual
Una vez
Plantilla
Aún no ejecutada
Lista de frecuencia
Para asientos manuales
Tipo de modelo: Contabilización periódica
Inactivo

### Notes:
Tiene pocas opciones al definir una contabilización periódica.
Puede definir la frecuencia con la que ocurrirá la contabilización.
Puede elegir la frecuencia desde la lista de frecuencias.
También puede definir la fecha de validez para la contabilización que especifica la última fecha posible en la que puede realizarse una contabilización.
Si no desea realizar la contabilización regularmente, también tiene la opción de definir una contabilización periódica como un modelo que se utilizará cuando sea necesario.
Puede crear estas contabilizaciones periódicas de antemano.  Fije el estatus en Aún no ejecutada hasta que deba iniciar las contabilizaciones.  Este estatus también puede utilizarse para desactivar una contabilización frecuente.

<!-- Slide number: 6 -->
# Modelo de contabilización con porcentajes


Código: Servicio			Descripción: Facturas de servicios
Cuenta de mayor/
Nº IC
Cuenta de mayor/
Nombre IC
% del Haber

% del Debe
6320
Servicios
25

6321
Electricidad
75
V550
Servicio público

100

### Notes:
Puede crear modelos de contabilización para asientos que cuentan con una estructura muy similar.
Para definir un tipo de modelo de porcentaje, utilice la ventana Modelos de contabilización del módulo Finanzas.
Estos modelos pueden contener números de cuenta, pero también puede limitarse a especificar la descripción de la cuenta en una partida individual si no sabe todavía qué cuenta se va a utilizar para ella.
En lugar de importes fijos, aquí solo se introducen porcentajes. Estos porcentajes indican cómo se distribuye el importe total entre las partidas individuales.
En la figura, se muestra un ejemplo de cómo puede asignar los gastos de servicios, como facturas de electricidad, a sus gastos componentes según un porcentaje específico.
El modelo de contabilización se almacena con un código y una descripción.
Luego, al registrar un asiento manual, puede elegir el tipo de modelo Porcentaje y el modelo relevante e indicar un importe en una de las partidas individuales, y el modelo asignará los importes a las otras partidas según el porcentaje que haya definido.
Utilice la opción Cancelar modelo para indicar los importes sin el cálculo automático.

<!-- Slide number: 7 -->

# Resumen
A continuación, se detallan algunos puntos clave:
| Existen dos tipos de modelo de asiento manual: |  |
| --- | --- |
| Se crea un modelo de contabilización con porcentajes para: | Asientos que tienen una estructura similar. Seleccionándolo en un asiento que introduce manualmente. |
| Se crea una contabilización periódica para: | Asientos similares, con importes fijos creados con regularidad. Cómo establecer la frecuencia con la que ocurrirá la contabilización. Se presenta un informe que le recomienda contabilizar la transacción que vence cuando ingresa al sistema. |

### Notes:
A continuación, se detallan algunos puntos clave para tener en cuenta:
Existen dos tipos de modelo de asiento manual.
Debe crear un modelo de contabilización con porcentajes para asientos que tienen una estructura muy similar. Entonces podrá seleccionar este modelo de contabilización en un asiento que se registra manualmente.
Debe crear una contabilización periódica para asientos de importe fijo similares que se crean regularmente. Puede definir la frecuencia con la que ocurrirá la contabilización. El sistema presenta un informe que recomienda contabilizar las operaciones que vencen cuando se inicia sesión en el sistema.

<!-- Slide number: 8 -->
# Thanks

You have completed the topic on journal entry templates.
Thank you for your time!

### Notes:
You have completed the topic on journal entry templates. Thank you for your time.
