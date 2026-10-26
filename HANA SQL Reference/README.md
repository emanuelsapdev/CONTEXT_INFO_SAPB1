# SAP HANA SQL Reference Guide (Markdown)

Conversión completa a Markdown de la guía oficial **SAP HANA SQL Reference Guide for SAP HANA Platform** (PDF de 2206 páginas). Sirve como base de conocimiento para un agente de IA que tenga que escribir o revisar SQL / SQLScript sobre HANA (por ejemplo, consultas, vistas o la `SP_TransactionNotification` de SAP Business One sobre HANA).

- El contenido está en **inglés**, tal cual el original. Los índices y esta guía están en español.
- Hay **un archivo por sección** del índice del PDF (1184 archivos). Cada archivo arranca con su título numerado, un link a la sección padre y las **páginas del PDF** de donde sale.

## Por dónde empezar

| Necesito… | Ir a |
| --- | --- |
| Buscar una **función** (SUBSTRING, ADD_DAYS, STRING_AGG, ROW_NUMBER, …) | [_INDICE-Funciones.md](_INDICE-Funciones.md) |
| Buscar una **sentencia** (SELECT, CREATE PROCEDURE, ALTER SYSTEM …, GRANT, …) | [_INDICE-Sentencias.md](_INDICE-Sentencias.md) |
| Buscar una **vista de sistema o de monitoreo** (TABLES, M_CS_TABLES, M_EXPENSIVE_STATEMENTS, …) | [_INDICE-Vistas-Sistema.md](_INDICE-Vistas-Sistema.md) |
| Dynamic Tiering, Streaming Analytics, Text Mining, Accelerator for SAP ASE | [_INDICE-Dynamic-Tiering-Streaming.md](_INDICE-Dynamic-Tiering-Streaming.md) |
| Ver el árbol completo de secciones | [_INDICE.md](_INDICE.md) |

## Estructura

| Carpeta / archivo | Contenido |
| --- | --- |
| `1-…`, `2-…`, `3-Introduction.md` | Presentación, novedades de la versión e introducción |
| `4-SQL-Reference/` | Núcleo del lenguaje: tipos de datos (4.3), palabras reservadas (4.4), operadores, expresiones, predicados, variables de sesión, **funciones (4.9)**, **sentencias (4.10)**, límites del sistema (4.11), **códigos de error (4.12)** y cumplimiento ANSI |
| `4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/` | Un archivo por función; los archivos `4.09.02` a `4.09.14` agrupan las funciones por categoría |
| `4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/` | Un archivo por sentencia. Las sentencias largas (CREATE TABLE, ALTER TABLE, SELECT, ALTER SYSTEM) son carpetas con un `README.md` y subarchivos |
| `5-Additional-SAP-HANA-Contexts/` | SQL de Accelerator for SAP ASE, Dynamic Tiering, Streaming Analytics y Text Mining |
| `6-System-Views-Reference/` | `6.01-System-Views` (metadatos, esquema SYS) y `6.02-Monitoring-Views` (vistas `M_*` con datos en tiempo de ejecución). Un archivo por vista, con la tabla de columnas |
| `7-System-Views-Additional-Contexts/` | Vistas de Dynamic Tiering y Streaming Analytics |

Cada carpeta tiene un `README.md` con el texto propio de esa sección y la lista de sus subsecciones.

## Convenciones del formato

- La **sintaxis** y los **ejemplos** van en bloques ` ```sql ` respetando la indentación original. Las reglas de sintaxis usan la notación BNF de la guía (`::=`, `[ ]` opcional, `{ | }` alternativas): ver `4-SQL-Reference/4.02-SQL-Notation-Conventions.md`.
- Las **tablas** del PDF (columnas de vistas, parámetros, códigos de error) son tablas Markdown. Dentro de una celda, `<br>` separa párrafos y `•` marca viñetas. Cuando una tabla sigue en varias páginas, queda unida en una sola.
- Los avisos *Note*, *Caution*, *Tip* y *Restriction* son citas (`> **Note**`).
- Las referencias cruzadas del PDF (`[page N]`) son links relativos al archivo correspondiente, con la forma `[→](…)`, o el título entero como link en las secciones *Related Information*.
- Los términos en `código` son los que el PDF muestra en fuente monoespaciada (parámetros como `<string>`, nombres de objetos, valores).

## Qué quedó fuera

- La tabla de contenidos (páginas 2–19) y el índice alfabético final (páginas 2194–2204): `_INDICE*.md` los reemplazan.
- La portada y las páginas de avisos legales y copyright.
- Íconos decorativos del PDF. Las tablas anidadas dentro de una celda (muy pocas) quedan como texto corrido dentro de esa celda.

## Relación con el resto de la base de conocimiento

- `../Tablas SAP B1/`: tablas de SAP Business One (OINV, OCRD, …), útiles para armar consultas HANA sobre la base de la compañía.
- `../Service Layer/`: API REST de SAP B1. La consulta SQL por Service Layer (`SQLQueries`) acepta solo un subconjunto de este SQL: ver `Service Layer/Guia/04-SQL-Query.md`.
