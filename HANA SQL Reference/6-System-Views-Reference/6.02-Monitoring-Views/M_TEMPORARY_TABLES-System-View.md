# 6.2.327 M_TEMPORARY_TABLES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2102–2104

Provides information about temporary tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| TABLE_OID | BIGINT | Displays the object ID of the table. |
| COMMENTS | NVARCHAR(5000) | Displays the comment on the table. |
| FIXED_PART_SIZE | SMALLINT | Displays the fixedsize part of the record in bytes. |
| CONNECTION_ID | INTEGER | Displays the anchor global session ID (anchor connection ID). |
| STATEMENT_ID | VARCHAR(20) | Displays the statement ID of the CRE ATE statement. |
| RECORD_COUNT | INTEGER | Displays the record count. |
| TABLE_SIZE | BIGINT | Displays the memory consumed by the table in bytes. |
| IS_LOGGED | VARCHAR(5) | Displays whether logging is enabled for the table: TRUE/FALSE. |
| IS_SYSTEM_TABLE | VARCHAR(5) | Displays whether the table is a system table: TRUE/FALSE. |
| IS_COLUMN_TABLE | VARCHAR(5) | Displays whether the table is a column table: TRUE/FALSE. |
| IS_INSERT_ONLY | VARCHAR(5) | Displays whether the table is an insert only table: TRUE/FALSE. |
| IS_TENANT_SHARED_DATA | VARCHAR(5) | Displays whether the table can be shared among other instances: TRUE/ FALSE. |
| IS_TENANT_SHARED_METADATA | VARCHAR(5) | Displays whether the table is a global table: TRUE/FALSE. |
| SESSION_TYPE | VARCHAR(16) | Displays the session type: NONE, SIM PLE, or HISTORY. For HISTORY, time travel is possible. |
| IS_TEMPORARY | VARCHAR(5) | Displays whether the table is a temporary table: TRUE/FALSE. |
| TEMPORARY_TABLE_TYPE | VARCHAR(8) | Displays the temporary table type. |
| IS_USER_DEFINED_TYPE | VARCHAR(5) | Displays whether the user defined a table type: TRUE/FALSE. |
| PRELOAD | VARCHAR(5) | Displays whether the table uses pre loading: TRUE/FALSE. This is only valid for column store tables. |

## Related Information

CREATE TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/README.md) M_TEMPORARY_TABLE_COLUMNS System View [→](M_TEMPORARY_TABLE_COLUMNS-System-View.md) TABLES System View [→](../6.01-System-Views/TABLES-System-View.md) ALTER TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.20-ALTER-TABLE/README.md)
