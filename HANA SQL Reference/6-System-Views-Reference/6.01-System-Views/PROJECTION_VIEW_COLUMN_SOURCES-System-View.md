# 6.1.117 PROJECTION_VIEW_COLUMN_SOURCES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1536–1537

Provides information about available projection view columns.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| VIEW_NAME | NVARCHAR(256) | Displays the view name. |
| COLUMN_NAME | NVARCHAR(256) | Displays the view column name. |
| SOURCE_SCHEMA_NAME | NVARCHAR(256) | Displays the source table schema name. |
| SOURCE_TABLE_NAME | NVARCHAR(256) | Displays the source table name. |
| SOURCE_COLUMN_NAME | NVARCHAR(256) | Displays the source column name. |

## Related Information

CREATE PROJECTION VIEW Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-PROJECTION-VIEW-Statement-Data-Definition.md) VIEW_COLUMNS System View [→](VIEW_COLUMNS-System-View.md)
