# 6.2.312 M_TABLE_PERSISTENCE_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2085–2087

Provides persistence virtual file summary statistics for tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| DISK_SIZE | BIGINT | Displays the total disk size, in bytes, of all of the table parts. |
| PAGE_COUNT | BIGINT | Displays the total number of pages of all of the table parts. |
| BYTES_WRITTEN | BIGINT | Displays the number of bytes that are written to the table. |
| BYTES_APPENDED | BIGINT | Displays the number of bytes that are appended to the table. |
| BYTES_READ | BIGINT | Displays the number of bytes that are read from the table. |
| BYTESTREAM_WRITTEN | BIGINT | Displays the number of bytes that are written to the table via a streaming interface. |
| APPEND_COUNT | BIGINT | Displays the number of times that the table was appended to. |
| WRITE_COUNT | BIGINT | Displays the number of times that the table was written to. |
| OPTIMIZE_COUNT | BIGINT | Displays the number of times that the table was optimized. |
| READ_COUNT | BIGINT | Displays the number of times that the table was read from. |
| TRUNCATE_COUNT | BIGINT | Displays the number of times that the table was truncated. |
| COPY_COUNT | BIGINT | Displays the number of times that the table was copied. |

## Related Information

CREATE STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-STATISTICS-Statement-Data-Definition.md) ALTER STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-STATISTICS-Statement-Data-Definition.md) REFRESH STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/REFRESH-STATISTICS-Statement-Data-Definition.md) DROP STATISTICS Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-STATISTICS-Statement-Data-Definition.md)
