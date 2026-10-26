# 6.1.76 FUNCTIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1495–1497

Provides information about available functions.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the function. |
| FUNCTION_NAME | NVARCHAR(256) | Displays the name of the function. |
| FUNCTION_OID | BIGINT | Displays the object ID of the function. |
| SQL_SECURITY | VARCHAR(7) | Displays the SQL security setting of the function: DEFINER/INVOKER. |
| DEFAULT_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the un qualified objects in the function. |
| INPUT_PARAMETER_COUNT | INTEGER | Displays the input type parameter count. |
| RETURN_VALUE_COUNT | INTEGER | Displays the return value type parameter count. |
| IS_UNICODE | VARCHAR(5) | Displays whether the function contains Unicode: TRUE/FALSE. |
| IS_ENCRYPTED | VARCHAR(5) | Displays whether the function is encrypted: TRUE/FALSE. |
| DEFINITION | NCLOB | Displays the query string of the function. |
| FUNCTION_TYPE | VARCHAR(10) | Displays the type of function. |
| FUNCTION_USAGE_TYPE | VARCHAR(9) | Displays the usage type of the function: SCALAR, TABLE, AGGREGATE, or WIN DOW. |
| IS_VALID | VARCHAR(5) | Displays whether the function is valid or not. This value becomes FALSE when its base objects are changed or dropped: TRUE/FALSE. |
| IS_HEADER_ONLY. | VARCHAR(5). | Displays whether the function is a header-only function: TRUE/FALSE. |
| IS_DETERMINISTIC | VARCHAR(5) | Displays whether the function is deterministic: TRUE/FALSE. |
| OWNER_NAME | NVARCHAR(256) | Displays the name of the owner of the function. |
| CREATE_TIME | TIMESTAMP | Displays the creation time of the function. |

## Related Information

FUNCTION_PARAMETERS System View [→](FUNCTION_PARAMETERS-System-View.md) FUNCTION_PARAMETER_COLUMNS System View [→](FUNCTION_PARAMETER_COLUMNS-System-View.md) CREATE FUNCTION Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-FUNCTION-Statement-Procedural.md) ALTER FUNCTION Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-FUNCTION-Statement-Procedural.md) DROP FUNCTION Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-FUNCTION-Statement-Procedural.md) Aggregate Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.02-Aggregate-Functions.md) Array Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.03-Array-Functions.md) Data Type Conversion Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.04-Data-Type-Conversion-Functions.md) Datetime Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.05-Datetime-Functions.md) Fulltext Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.06-Fulltext-Functions.md) Hierarchy Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.07-Hierarchy-Functions.md)

JSON Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.08-JSON-Functions.md) Miscellaneous Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.09-Miscellaneous-Functions.md) Numeric Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.10-Numeric-Functions.md) Security Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.11-Security-Functions.md) Series Data Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.12-Series-Data-Functions.md) String Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.13-String-Functions.md) Window Functions and the Window Specification [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.14-Window-Functions/README.md)
