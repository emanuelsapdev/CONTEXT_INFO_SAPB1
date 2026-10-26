# 6.1.188 VIRTUAL_PACKAGES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1623–1624

Provides the list of virtual packages.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the virtual package. |
| PACKAGE_NAME | NVARCHAR(256) | Displays the name of the virtual package. |
| ADAPTER_NAME | NVARCHAR(256) | Displays the name of the remote source adapter. |
| CREATE_TIMESTAMP | TIMESTAMP | Displays the timestamp when the virtual package was created. |
| CONTENT | BLOB | Displays the content of the virtual package. |

## Related Information

VIRTUAL_FUNCTION_PACKAGES System View [→](VIRTUAL_FUNCTION_PACKAGES-System-View.md) CREATE VIRTUAL FUNCTION Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-VIRTUAL-FUNCTION-Statement-Procedural.md)
