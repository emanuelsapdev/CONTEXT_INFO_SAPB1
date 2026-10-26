# 6.1.149 SERIES_KEY_COLUMNS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1568

Provides information about series key columns for series tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the series table name. |
| COLUMN_NAME | NVARCHAR(256) | Displays the series key column name. |
| POSITION | INTEGER | Displays the ordinal position of the series key column. |

## Related Information

SERIES_TABLES System View [→](SERIES_TABLES-System-View.md) Series Data Functions [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.12-Series-Data-Functions.md)
