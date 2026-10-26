# 6.1.162 TABLE_COLUMNS_ODBC System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1589–1591

Provides information about available table columns.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| TABLE_OID | BIGINT | Displays the object ID of the table. |
| COLUMN_NAME | NVARCHAR(256) | Displays the name of the column. |
| DATA_TYPE_ID | SMALLINT | Displays the SQL data type ID of the column. |
| DATA_TYPE_NAME | VARCHAR(16) | Displays the SQL data type name of the column. |
| COLUMN_SIZE | INTEGER | Displays the total number of characters required to display the value when it is converted to characters. |
| BUFFER_LENGTH | INTEGER | Displays the length, in bytes, required to transfer the value. |
| DECIMAL_DIGITS | INTEGER | Displays the total number of significant digits to the right of the decimal point. |
| NUM_PREC_RADIX | INTEGER | Displays how to interpret columns COLUMN_SIZE and DECIMAL_DIGITS. For numeric data types either 10 or 2. |
| NULLABLE | VARCHAR(5) | Displays whether the column is allowed to accept null value: TRUE/FALSE. |
| COLUMN_DEF | NVARCHAR(5000) | Displays the default value of the column. |
| SQL_DATA_TYPE | SMALLINT | Displays the SQL data type ID of the column. |
| SQL_DATETIME_SUB | SMALLINT | Displays the subtype code for datetime data types. |
| CHAR_OCTET_LENGTH | INTEGER | Displays the maximum length, in bytes, of a character or binary data type column. |
| POSITION | INTEGER | Displays the ordinal position of the column in a record. |
| COMMENTS | NVARCHAR(5000) | Displays the description for the column. |

## Related Information

TABLES System View [→](TABLES-System-View.md) TABLE_COLUMNS System View [→](TABLE_COLUMNS-System-View.md) COLUMNS System View - Deprecated [→](COLUMNS-System-View-Deprecated.md)
