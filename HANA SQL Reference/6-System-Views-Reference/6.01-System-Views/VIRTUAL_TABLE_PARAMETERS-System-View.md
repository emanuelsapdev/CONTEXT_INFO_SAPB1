# 6.1.191 VIRTUAL_TABLE_PARAMETERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1626–1627

Provides a list of parameters of the virtual tables that refer to column views in a remote SAP HANA database.

## Structure

| **Column name** | **Data type** | **Unit** | **Description** |
| --- | --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) |   | Displays the schema of the virtual table. |
| OBJECT_NAME | NVARCHAR(256) |   | Displays the name of the virtual table. |
| PARAMETER_NAME | NVARCHAR(256) |   | Displays the name of the parameter. |
| IS_MANDATORY | VARCHAR(5) |   | Displays whether a parameter is mandatory or not: TRUE/FALSE. If TRUE, the value of the parameter should be provided either by setting the default value or through the SQL query. If FALSE, setting the value of the parameter is optional. |
| DEFAULT_VALUE | NVARCHAR(256) |   | Displays the default value of the parameter. This column is set to an empty string when the parameter has no default value. |

## Related Information

VIRTUAL_TABLES System View [→](VIRTUAL_TABLES-System-View.md) CREATE VIRTUAL TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-VIRTUAL-TABLE-Statement-Data-Definition.md) ALTER VIRTUAL TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-VIRTUAL-TABLE-Statement-Data-Definition.md) VIRTUAL_TABLE_PROPERTIES System View [→](VIRTUAL_TABLE_PROPERTIES-System-View.md)
