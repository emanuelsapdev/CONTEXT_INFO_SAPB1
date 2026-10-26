# 6.1.115 PROCEDURE_PARAMETER_COLUMNS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1534–1535

Lists available columns of table parameters of stored procedures.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the stored procedure. |
| PROCEDURE_NAME | NVARCHAR(256) | Displays the same of the stored procedure. |
| PROCEDURE_OID | BIGINT | Displays the object ID of the stored procedure. |
| PARAMETER_NAME | NVARCHAR(256) | Displays the parameter name. |
| PARAMETER_POSITION | INTEGER | Displays the ordinal position of the parameter. |
| COLUMN_NAME | NVARCHAR(256) | Displays the name of the column in the table parameter. |
| POSITION | INTEGER | Displays the ordinal position of the column in the table parameter. |
| DATA_TYPE_NAME | VARCHAR(16) | Displays the SQL data type name of the column. |
| LENGTH | INTEGER | Displays the number of characters for character types, the number of max digits for numeric types, the number of charactesr for datetime types, or the number of bytes for LOB types, |
| SCALE | INTEGER | For numeric types, displays the maximum number of digits to the right of the decimal point. For time and time stamp types, displays the decimal digits defined as the number of digits to the right of the decimal point in the second's component of the data. |
| IS_NULLABLE | VARCHAR(5) | Displays whether the column is allowed to accept NULL values: TRUE/FALSE. |

## Related Information

PROCEDURES System View [→](PROCEDURES-System-View.md) PROCEDURE_OBJECTS System View [→](PROCEDURE_OBJECTS-System-View.md) PROCEDURE_PARAMETERS System View [→](PROCEDURE_PARAMETERS-System-View.md) PROCEDURE_ROUTES System View [→](PROCEDURE_ROUTES-System-View.md)
