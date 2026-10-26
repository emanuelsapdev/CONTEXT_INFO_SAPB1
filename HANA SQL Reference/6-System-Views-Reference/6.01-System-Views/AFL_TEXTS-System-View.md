# 6.1.11 AFL_TEXTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1411

Provides information about available AFL texts.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the AFL text. |
| AREA_NAME | NVARCHAR(256) | Displays the area name of the AFL text. |
| TEXT_ID | INTEGER | Displays the text ID. |
| LANGUAGE_CODE | NVARCHAR(5) | Displays the language code of the AFL text. |
| TEXT | NVARCHAR(512) | Displays the text. |

## Related Information

AFL_AREAS System View [→](AFL_AREAS-System-View.md) AFL_FUNCTIONS System View [→](AFL_FUNCTIONS-System-View.md) AFL_FUNCTION_PARAMETERS System View [→](AFL_FUNCTION_PARAMETERS-System-View.md) AFL_FUNCTION_PROPERTIES System View [→](AFL_FUNCTION_PROPERTIES-System-View.md) AFL_PACKAGES System View [→](AFL_PACKAGES-System-View.md)
