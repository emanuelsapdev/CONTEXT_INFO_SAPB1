# 6.1.7 AFL_FUNCTIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1406–1407

Provides information about available AFL functions.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| FUNCTION_OID | BIGINT | Displays the object ID of the AFL function. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the AFL function. |
| AREA_NAME | NVARCHAR(256) | Displays the name of the AFL area that the AFL function belongs to. |
| PACKAGE_NAME | NVARCHAR(256) | Displays the name of the AFL package that the AFL function belongs to. |
| FUNCTION_NAME | NVARCHAR(256) | Displays the name of the AFL function. |
| CREATE_TIMESTAMP | TIMESTAMP | Displays the timestamp when the AFL function was created. |
| INPUT_PARAMETER_COUNT | INTEGER | Displays the number of the input parameters of the AFL function. |
| RETURN_VALUE_COUNT | INTEGER | Displays the umber of the out parameters of the AFL function. |
| FUNCTION_TYPE | VARCHAR(7) | Displays the type of the AFL function. |
| TECHNICAL_CATEGORY | VARCHAR(11) | Displays the technical category of the AFL function. |

## Related Information

AFL_AREAS System View [→](AFL_AREAS-System-View.md) AFL_FUNCTION_PARAMETERS System View [→](AFL_FUNCTION_PARAMETERS-System-View.md) AFL_FUNCTION_PROPERTIES System View [→](AFL_FUNCTION_PROPERTIES-System-View.md) AFL_PACKAGES System View [→](AFL_PACKAGES-System-View.md) AFL_TEXTS System View [→](AFL_TEXTS-System-View.md) M_AFL_STATES System View [→](../6.02-Monitoring-Views/M_AFL_STATES-System-View.md)
