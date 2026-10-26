# 6.2.48 M_CONSISTENCY_CHECK_HISTORY_ERRORS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1697–1698

Lists the errors that were found within a specified check run.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| CHECK_EXECUTION_ID | BIGINT | Displays the execution ID of the consistency check run that produced the error. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| OBJECT_NAME | NVARCHAR(256) | Displays the name of the object. |
| OBJECT_TYPE | NVARCHAR(32) | Displays the type of the object. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| PART_ID | INTEGER | Displays the partition ID. Contains 0 for an unpartitioned table. |
| ERROR_CODE | INTEGER | Displays the error code. |
| ERROR_MESSAGE | NVARCHAR(5000) | Displays the error message. |
| SEVERITY | VARCHAR(8) | Displays the error severity: LOW, INFO, HIGH, or ERROR. |
| CHECK_ACTION | VARCHAR(64) | Displays the check action that produced the error. Contains NULL for errors not related to a specific check action. |
| AFFECTED_COUNT | BIGINT | Displays the number of rows affected by the error (optional).<br>This column does not always contain a value, even in the case of an error. For some errors, this column may contain a NULL value. |
| DETAILS | NCLOB (JSON) | Displays the detailed information related to the error (optional).<br>This column does not always contain a value, even in the case of an error. For some errors, this column may contain a NULL value. |

## Related Information

M_CONSISTENCY_CHECK_HISTORY System View [→](M_CONSISTENCY_CHECK_HISTORY-System-View.md) SQL Error Codes [→](../../4-SQL-Reference/4.12-SQL-Error-Codes.md) HISTORY COLUMN Option (Time Travel) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/4.10.01.68.03-HISTORY-COLUMN-Option-Time-Travel.md) SET HISTORY SESSION Statement (Session Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/SET-HISTORY-SESSION-Statement-Session-Management.md)
