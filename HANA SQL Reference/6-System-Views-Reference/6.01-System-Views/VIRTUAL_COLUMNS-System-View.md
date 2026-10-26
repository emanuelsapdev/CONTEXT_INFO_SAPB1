# 6.1.184 VIRTUAL_COLUMNS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1619–1620

Provides information about virtual columns.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| DATA_TYPE_NAME | VARCHAR(16) | Displays the SQL data type name of the column. |
| LENGTH | INTEGER | Displays the number of characterss for character types, the number of maximum digits for numeric types, the number of characters for datetime types, or the number of bytes for LOB types. |
| SCALE | INTEGER | For numeric types: displays the maximum number of digits to the right of the decimal point. For time, TIME STAMP types: displays the decimal digits to the right of the decimal point in the second's component of the data. |
| REMOTE_DATA_TYPE_NAME | VARCHAR(32) | Displays the remote data type name. |
| REMOTE_LENGTH | INTEGER | Displays the remote column length. |
| REMOTE_SCALE | INTEGER | Displays the remote scale. |
| IS_INSERTABLE | VARCHAR(5) | Displays whether or not INSERT is supported: TRUE/FALSE. |
| IS_UPDATABLE | VARCHAR(5) | Displays whether or not UPDATE is supported: TRUE/FALSE. |
| IS_UPSERTABLE | VARCHAR(5) | Displays whether or not UPSERT is supported: TRUE/FALSE. |
| IS_SELECTABLE | VARCHAR(5) | Displays whether or not SELECT is supported: TRUE/FALSE. |

## Related Information

VIRTUAL_COLUMN_PROPERTIES System View [→](VIRTUAL_COLUMN_PROPERTIES-System-View.md) VIRTUAL_TABLES System View [→](VIRTUAL_TABLES-System-View.md) CREATE VIRTUAL TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-VIRTUAL-TABLE-Statement-Data-Definition.md) ALTER VIRTUAL TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-VIRTUAL-TABLE-Statement-Data-Definition.md)
