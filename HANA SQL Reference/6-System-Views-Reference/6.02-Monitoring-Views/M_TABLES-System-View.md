# 6.2.303 M_TABLES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2072–2073

Provides information on row and column tables, as well as collection tables (JSON Document Store).

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| RECORD_COUNT | BIGINT | Displays the number of records in this table. |
| TABLE_SIZE | BIGINT | Displays the allocated memory size for fixedsize and variable-size part in bytes. |
| IS_COLUMN_TABLE | VARCHAR(5) | Displays whether the table is a column table: TRUE/FALSE. |
| TABLE_TYPE | VARCHAR(16) | Displays the type of the table: ROW, COLUMN, or COLLECTION. |
| IS_PARTITIONED | VARCHAR(5) | Displays whether the table is partitioned: TRUE/FALSE. |
| IS_REPLICATED | VARCHAR(5) | Displays whether the table is replicated: TRUE/FALSE. |
| HAS_RECORD_COMMIT_TIMESTAMP | VARCHAR(5) | Displays whether table is tracking commit timestamps: TRUE/FALSE. |

## Related Information

TABLES System View [→](../6.01-System-Views/TABLES-System-View.md) CREATE TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/README.md) LOCK TABLE Statement (Transaction Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/LOCK-TABLE-Statement-Transaction-Management.md) RENAME TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RENAME-TABLE-Statement-Data-Definition.md) ALTER TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.20-ALTER-TABLE/README.md) TRUNCATE TABLE Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/TRUNCATE-TABLE-Statement-Data-Manipulation.md) DROP TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-TABLE-Statement-Data-Definition.md)
