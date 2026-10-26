# 6.1.187 VIRTUAL_FUNCTION_PACKAGES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1622–1623

Provides information about virtual function packages.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR (256) | Displays the schema name of the virtual function package. |
| PACKAGE_NAME | NVARCHAR (256) | Displays the name of the virtual function package. |
| ADAPTER_NAME | NVARCHAR (256) | Displays the name of the remote source adapter. |
| CREATE_TIMESTAMP | TIMESTAMP | Displays the timestamp when the virtual function package is created. |
| CONTENT | BLOB | Displays the content of the virtual function package. |

## Related Information

VIRTUAL_FUNCTIONS System View [→](VIRTUAL_FUNCTIONS-System-View.md) CREATE VIRTUAL FUNCTION Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-VIRTUAL-FUNCTION-Statement-Procedural.md) SQL Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/README.md)
