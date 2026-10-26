# 6.1.185 VIRTUAL_COLUMN_PROPERTIES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1620–1621

Provides the properties set on virtual table columns.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the virtual table. |
| TABLE_NAME | NVARCHAR(256) | Displays the virtual table name. |
| COLUMN_NAME | NVARCHAR(256) | Displays the virtual table column name. |
| PROPERTY | NVARCHAR(256) | Displays the property name. |
| VALUE | NVARCHAR(512) | Displays the property value. |
| IS_READ_ONLY | VARCHAR(5) | Displays whether or not the property is read-only: TRUE/FALSE. |

## Related Information

VIRTUAL_COLUMNS System View [→](VIRTUAL_COLUMNS-System-View.md) VIRTUAL_TABLES System View [→](VIRTUAL_TABLES-System-View.md) CREATE VIRTUAL TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-VIRTUAL-TABLE-Statement-Data-Definition.md) ALTER VIRTUAL TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-VIRTUAL-TABLE-Statement-Data-Definition.md)
