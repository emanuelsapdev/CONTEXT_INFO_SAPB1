# 6.2.328 M_TEMPORARY_TABLE_COLUMNS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2104–2106

Provides information about temporary table columns.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| TABLE_OID | BIGINT | Displays the object ID of the table. |
| COLUMN_NAME | NVARCHAR(256) | Displays the name of the column. |
| POSITION | INTEGER | Displays the ordinal position of the table column. |
| DATA_TYPE_ID | SMALLINT | Displays the SQL data type ID of the column. |
| DATA_TYPE_NAME | VARCHAR(16) | Displays the SQL data type name of the column. |
| OFFSET | SMALLINT | Displays the offset of the column in the record in bytes. |
| LENGTH | INTEGER | Displays the number of characters for character types. This value is the number of max digits for numeric types, the number of characters for datetime types, or the number of bytes for LOB types. |
| SCALE | INTEGER | Displays the maximum number of digits to the right of the decimal point: TIME or TIMESTAMP. The decimal digits are defined as the number of digits to the right of the decimal point in the second's component of the data. |
| IS_NULLABLE | VARCHAR(5) | Displays whether the column is allowed to accept a null value: TRUE/FALSE. |
| DEFAULT_VALUE | NVARCHAR(5000) | Displays the default value of the column in bytes. |
| COLLATION | NVARCHAR(5000) | Displays the collation of the column. |
| COMMENTS | NVARCHAR(5000) | Displays the comments on the column. |
| MAX_VALUE | NVARCHAR(5000) | Displays the maximum value in bytes. |
| MIN_VALUE | NVARCHAR(5000) | Displays the minimum value in bytes. |
| CS_DATA_TYPE_ID | INTEGER | Displays the column store data type ID. |
| CS_DATA_TYPE_NAME | VARCHAR(16) | Displays the column store data type name. |
| DDIC_DATA_TYPE_ID | INTEGER | Displays the DDIC data type ID. |
| DDIC_DATA_TYPE_NAME | VARCHAR(7) | Displays the DDIC data type name. |
| COMPRESSION_TYPE | VARCHAR(9) | Displays the type of compression: DE FAULT, PREFIXED, SPARSE, CLUS TERED, INDIRECT, or RLE. |
| INDEX_TYPE | VARCHAR(4) | Displays the type of index: NONE/ FULL. |
| COLUMN_ID | BIGINT | Displays the ID of the column. |
| PRELOAD | VARCHAR(5) | Displays if a column is preloaded: TRUE/FALSE. |

## Related Information

M_TEMPORARY_TABLES System View [→](M_TEMPORARY_TABLES-System-View.md) CREATE TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/README.md) TABLES System View [→](../6.01-System-Views/TABLES-System-View.md) TRUNCATE TABLE Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/TRUNCATE-TABLE-Statement-Data-Manipulation.md)
