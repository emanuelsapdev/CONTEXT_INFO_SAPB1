# 6.2.100 M_ES_DELTA_MERGE_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1776–1777

Provides extended storage delta merge statistics information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| START_TIME | TIMESTAMP | Displays the time that the merge started. |
| END_TIME | TIMESTAMP | Displays the time that the merge ended. |
| STATUS | VARCHAR(16) | Displays the status of the merge operation: STARTED, COMPLETED, or FAILED. |
| ERROR_CODE | INTEGER | Displays the SQL code of the merge once completed. |
| ERROR_TEXT | NVARCHAR(256) | Displays any additional error information. |
| MOTIVATION | VARCHAR(16) | Displays the cause of the merge trigger: DML, DDL, SHUTDOWN, or USER. |
| IS_BLOCKING | VARCHAR(5) | Indicates whether or not the merge was blocking: TRUE/FALSE. |
| INSERT_RECORD_COUNT | BIGINT | Displays the number of rows that were inserted as a result of the merge. |
| UPDATE_RECORD_COUNT | BIGINT | Displays the number of rows that were updated as a result of the merge. |
| DELETE_RECORD_COUNT | BIGINT | Displays the number of rows that were deleted as a result of the merge. |
| UNCOMMITTED_RECORD_COUNT | BIGINT | Displays the number of rows that were uncommitted at the time of the merge. |

## Related Information

M_ES_DELTA_MEMORY System View [→](M_ES_DELTA_MEMORY-System-View.md) MERGE DELTA Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/MERGE-DELTA-Statement-Data-Manipulation.md) M_DELTA_MERGE_STATISTICS System View [→](M_DELTA_MERGE_STATISTICS-System-View.md)
