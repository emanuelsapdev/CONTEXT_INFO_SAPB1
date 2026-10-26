# 6.1.8 AFL_FUNCTION_PARAMETERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1407–1409

Provides information about parameters of AFL functions.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the AFL function. |
| AREA_NAME | NVARCHAR(256) | Displays the area name of the AFL function. |
| FUNCTION_NAME | NVARCHAR(256) | Displays the function name of the AFL function. |
| PARAMETER_NAME | NVARCHAR(256) | Displays the parameter name. |
| POSITION | INTEGER | Displays the ordinal position of the parameter. |
| IO_TYPE | NVARCHAR(8) | Displays the direction of the parameter. |
| DATA_TYPE | VARCHAR(22) | Displays the data type. |
| CS_DATA_TYPE | VARCHAR(13) | Displays the column store data type. |
| CS_DATA_TYPE_EXPRESSION | NVARCHAR(256) | Displays the regular expression of column store data type. |
| SQL_NAME | NVARCHAR(256) | Displays the SQL name. |
| SQL_DATA_TYPE | VARCHAR(14) | Displays the SQL data type. |
| LENGTH | INTEGER | Displays the parameter length in bytes. |
| RAW_SIZE | INTEGER | Displays the parameter raw size in bytes. |
| SCALE | INTEGER | Displays the scale of the parameter. |
| USAGE | NVARCHAR(32) | Displays the usage. |
| BUSINESS_TEXT_ID | INTEGER | Displays the business text ID of the parameter. |

## Related Information

AFL_FUNCTIONS System View [→](AFL_FUNCTIONS-System-View.md) AFL_PACKAGES System View [→](AFL_PACKAGES-System-View.md) AFL_FUNCTION_PROPERTIES System View [→](AFL_FUNCTION_PROPERTIES-System-View.md) AFL_TEXTS System View [→](AFL_TEXTS-System-View.md) M_AFL_STATES System View [→](../6.02-Monitoring-Views/M_AFL_STATES-System-View.md)
