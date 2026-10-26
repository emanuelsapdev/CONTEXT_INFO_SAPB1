# 6.1.186 VIRTUAL_FUNCTIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1621–1622

Provides information about virtual functions.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR (256) | Displays the schema name of the function. |
| FUNCTION_NAME | NVARCHAR (256) | Displays the name of the function. |
| FUNCTION_OID | BIGINT | Displays the object ID of the function. |
| REMOTE_SOURCE_NAME | NVARCHAR (256) | Displays the remote source name used in the function. |
| ADAPTER_NAME | NVARCHAR (32) | Displays the name of the remote source adapter. |
| FUNCTION_CONFIGURATION | NVARCHAR (5000) | Displays the virtual function configuration. |
| PACKAGE_SCHEMA_NAME | NVARCHAR (256) | Displays the package schema name. |
| PACKAGE_NAME | NVARCHAR (256) | Displays the package name used by virtual functions |
| IS_VALID | NVARCHAR (5) | Displays whether the function is valid or not: TRUE/FALSE. This value becomes FALSE when its base objects are changed or dropped. |

## Related Information

VIRTUAL_FUNCTION_PACKAGES System View [→](VIRTUAL_FUNCTION_PACKAGES-System-View.md) CREATE VIRTUAL FUNCTION Statement (Procedural) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-VIRTUAL-FUNCTION-Statement-Procedural.md) SQL Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/README.md)
