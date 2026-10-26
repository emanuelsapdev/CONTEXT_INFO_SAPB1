# 6.2.47 M_CONSISTENCY_CHECK_HISTORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1695–1697

Provides table check run information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| CHECK_EXECUTION_ID | BIGINT | Displays the unique identifier for a run. |
| CONNECTION_ID | BIGINT | Displays the connection ID of the last check execution. |
| USER_NAME | NVARCHAR(256) | Displays the ID of the user performing the consistency check. |
| CHECK_PROCEDURE_NAME | NVARCHAR(256) | Displays the name of the check procedure, for example CHECK_TABLE_CONSISTENCY. |
| CHECK_ACTION | VARCHAR(256) | Displays the single check action or a comma-separated list of check actions. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. NULL is used if all schemas were checked. |
| OBJECT_NAME | NVARCHAR(256) | Displays the name of the object. |
| OBJECT_TYPE | NVARCHAR(32) | Displays the type of the object. |
| CHECK_EXECUTION_COUNT | BIGINT | Displays the number of executions related to the aggregated entry. |
| FIRST_START_TIME | TIMESTAMP | Displays the first start time of an aggregated entry. For an aggregated entry without any errors, this value defines the interval in which all checks were error-free. |
| LAST_START_TIME | TIMESTAMP | Displays the last invocation start time of an aggregated entry. For an aggregated entry without any errors, this value defines the interval in which all checks were error-free. |
| LAST_DURATION | BIGINT | Displays the total duration of the last check in milliseconds. |
| MIN_DURATION | BIGINT | Displays the minimum duration of the check runs in milliseconds. |
| MAX_DURATION | BIGINT | Displays the maximum duration of the check runs in milliseconds. |
| AVG_DURATION | BIGINT | Displays the average duration of the check runs milliseconds. |
| LAST_SCHEDULED_TABLE_COUNT | INTEGER | Displays the number of tables scheduled for checking. |
| MIN_SCHEDULED_TABLE_COUNT | INTEGER | Displays the minimum number of scheduled table counts for the checks runs. |
| MAX_SCHEDULED_TABLE_COUNT | INTEGER | Displays the maximum number of scheduled table counts for the checks runs. |
| AVG_SCHEDULED_TABLE_COUNT | INTEGER | Displays the average number of scheduled table counts for the checks runs. |
| EXECUTED_TABLE_COUNT | INTEGER | Displays the number of tables that have been checked. |
| ERROR_TABLE_COUNT | INTEGER | Displays the number of tables with errors. |
| ERROR_CODE | INTEGER | Displays the error code returned by the check. |
| ERROR_MESSAGE | NVARCHAR(5000) | Displays the error message returned by the check. |

## Additional Information

Further information about errors found during check runs can be found in the M_CONSISTENCY_CHECK_HISTORY_ERRORS system view.

Entries are aggregated, meaning that an existing entry is updated if the same checks were executed by the same user producing the same result.

## Related Information

M_CONSISTENCY_CHECK_HISTORY_ERRORS System View [→](M_CONSISTENCY_CHECK_HISTORY_ERRORS-System-View.md) HISTORY COLUMN Option (Time Travel) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/4.10.01.68.03-HISTORY-COLUMN-Option-Time-Travel.md) SET HISTORY SESSION Statement (Session Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/SET-HISTORY-SESSION-Statement-Session-Management.md)
