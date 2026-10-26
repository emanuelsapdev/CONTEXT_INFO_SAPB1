# 6.2.323 M_TEMPORARY_JOIN_CONDITIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2098–2099

Provides information about temporary join conditions.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| VIEW_NAME | NVARCHAR(256) | Displays the join view name. |
| JOIN_CONDITION_NAME | NVARCHAR(256) | Displays the join condition name. |
| JOIN_ORDER | BIGINT | Displays the join order number. |
| TABLE_SCHEMA_NAME1 | NVARCHAR(256) | Displays the schema name of column1. |
| TABLE_NAME1 | NVARCHAR(256) | Displays the table name of column1. |
| COLUMN_NAME1 | NVARCHAR(256) | Displays the name of column1. |
| ALIAS_NUMBER1 | INTEGER | Displays the alias number of table name1. |
| TABLE_SCHEMA_NAME2 | NVARCHAR(256) | Displays the schema name of column2. |
| TABLE_NAME2 | NVARCHAR(256) | Displays the table name of column2. |
| COLUMN_NAME2 | NVARCHAR(256) | Displays the name of column2. |
| ALIAS_NUMBER2 | INTEGER | Displays the alias number of table name2. |
| CONSTRAINTS | NVARCHAR(256) | Displays the join constraint name. |
| JOIN_TYPE | VARCHAR(5) | Displays the join type. |
| CARDINALITY | VARCHAR(3) | Displays the join cardinality. |

## Related Information

M_TEMPORARY_JOIN_CONSTRAINTS System View [→](M_TEMPORARY_JOIN_CONSTRAINTS-System-View.md) ALTER SYSTEM CLEAR COLUMN JOIN DATA STATISTICS (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-CLEAR-COLUMN-JOIN-DATA-STATISTICS-System.md)
