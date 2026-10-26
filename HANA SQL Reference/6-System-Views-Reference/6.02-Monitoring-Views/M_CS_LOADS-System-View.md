# 6.2.60 M_CS_LOADS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1719–1721

Provides a history of column loads.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| LOAD_TIME | TIMESTAMP | Displays the timestamp of the load event. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. This is left empty if the whole table is loaded. |
| PART_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| TABLE_OID | BIGINT | Displays the object ID of the table. |
| IS_HISTORY | VARCHAR(5) | Displays the flag to indicate whether the history part is loaded (this is only relevant for history tables). This is left empty if the whole table is loaded. |
| LOAD_DURATION | BIGINT | Displays the load duration, in milliseconds. |
| ERROR_CODE | INTEGER | Displays the error code. |
| ERROR_TEXT | NVARCHAR(5000) | Displays the error text. |
| STATEMENT_ID | BIGINT | Displays the statement ID. |
| STATEMENT_HASH | VARCHAR(32) | Displays the unique identifier for an SQL string. |

## Related Information

[LOAD Statement (Data Manipulation)](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/LOAD-Statement-Data-Manipulation.md)
