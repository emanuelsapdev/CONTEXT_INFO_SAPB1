# 6.1.10 AFL_PACKAGES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1410–1411

Provides information about available AFL packages.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| PACKAGE_OID | BIGINT | Displays the object ID of the AFL package. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the AFL package. |
| AREA_NAME | NVARCHAR(256) | Displays the name of the AFL area that the AFL package belongs to. |
| PACKAGE_NAME | NVARCHAR(256) | Displays the name of the AFL package. |
| CREATE_TIMESTAMP | TIMESTAMP | Displays the timestamp when the AFL package was created. |

## Related Information

AFL_AREAS System View [→](AFL_AREAS-System-View.md) AFL_FUNCTIONS System View [→](AFL_FUNCTIONS-System-View.md) AFL_FUNCTION_PARAMETERS System View [→](AFL_FUNCTION_PARAMETERS-System-View.md) AFL_FUNCTION_PROPERTIES System View [→](AFL_FUNCTION_PROPERTIES-System-View.md) AFL_TEXTS System View [→](AFL_TEXTS-System-View.md)
