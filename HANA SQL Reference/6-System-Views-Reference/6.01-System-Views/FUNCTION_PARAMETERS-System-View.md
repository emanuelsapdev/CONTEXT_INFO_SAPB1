# 6.1.77 FUNCTION_PARAMETERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1497–1498

Provides information about parameters for functions.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the function. |
| FUNCTION_NAME | NVARCHAR(256) | Displays the name of the function. |
| FUNCTION_OID | BIGINT | Displays the object ID of the function. |
| PARAMETER_NAME | NVARCHAR(256) | Displays the parameter name. |
| DATA_TYPE_ID | INTEGER | Displays the data type ID. |
| DATA_TYPE_NAME | VARCHAR(16) | Displays the data type name. |
| LENGTH | INTEGER | Displays the parameter length. |
| SCALE | INTEGER | Displays the scale of the parameter. |
| POSITION | INTEGER | Displays the ordinal position of the parameter. |
| TABLE_TYPE_SCHEMA | NVARCHAR(256) | Displays the schema name of the table type if the DATA_TYPE_NAME is TABLE_TYPE. |
| TABLE_TYPE_NAME | NVARCHAR(256) | Displays the name of the table type if the DATA_TYPE_NAME is TABLE_TYPE. |
| IS_INPLACE_TYPE | VARCHAR(5) | Displays whether the parameter type is an inplace type: TRUE/FALSE. |
| PARAMETER_TYPE | VARCHAR(7) | Displays the parameter mode: IN, OUT, or INOUT. |
| HAS_DEFAULT_VALUE | VARCHAR(5) | Displays whether the parameter has a default value: TRUE/FALSE. |
| IS_NULLABLE | VARCHAR(5) | Displays whether the parameter accepts a NULL value: TRUE/FALSE. |

## Related Information

FUNCTION_PARAMETER_COLUMNS System View [→](FUNCTION_PARAMETER_COLUMNS-System-View.md) FUNCTIONS System View [→](FUNCTIONS-System-View.md)
