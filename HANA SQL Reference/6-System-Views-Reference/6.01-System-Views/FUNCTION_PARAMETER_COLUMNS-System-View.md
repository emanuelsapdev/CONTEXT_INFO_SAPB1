# 6.1.78 FUNCTION_PARAMETER_COLUMNS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1498–1499

Provides information about columns that are available for function table parameters.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the function. |
| FUNCTION_NAME | NVARCHAR(256) | Displays the name of the function. |
| FUNCTION_OID | BIGINT | Displays the object ID of the function. |
| PARAMETER_NAME | NVARCHAR(256) | Displays the parameter name. |
| PARAMETER_POSITION | INTEGER | Displays the ordinal position of the parameter. |
| COLUMN_NAME | NVARCHAR(256) | Displays the name of the column in the table parameter. |
| POSITION | INTEGER | Displays the ordinal position of the column in the table parameter. |
| DATA_TYPE_NAME | VARCHAR(16) | Displays the SQL data type name of the column. |
| LENGTH | INTEGER | Depending on the data type:<br>• Displays the number of characters for characters types<br>• Displays the maximum number of digits for numeric types<br>• Displays the number of characters for datetime types<br>• Displays the number of bytes for LOB types |
| SCALE | INTEGER | For numeric data types, displays the maximum number of digits to the right of the decimal point. For time and time stamp data types, Displays the decimal digits, which are defined as the number of digits to the right of the decimal point in the second's component of the data. |
| IS_NULLABLE | VARCHAR(5) | Displays whether the column can accept NULL values: TRUE/FALSE. |

## Related Information

FUNCTION_PARAMETERS System View [→](FUNCTION_PARAMETERS-System-View.md) FUNCTIONS System View [→](FUNCTIONS-System-View.md)
