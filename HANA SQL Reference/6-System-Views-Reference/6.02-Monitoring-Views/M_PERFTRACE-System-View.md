# 6.2.199 M_PERFTRACE System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1924–1925

Displays the state of the current performance trace. The performance trace provides detailed information about query execution.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| STATUS | VARCHAR(16) | Displays the status of the performance trace: STOPPED, STARTED, or SAVING. |
| START_TIME | TIMESTAMP | Displays when the performance trace started. |
| STOP_TIME | TIMESTAMP | Displays when the performance trace stopped. |
| FILE_SIZE | BIGINT | Displays the size of the collected trace files in bytes. This value is only valid if tracing is stopped and not saved. |
| REMAINING_SECONDS | INTEGER | Displays the remaining number of seconds until tracing stops automatically. |
| USER_NAME | NVARCHAR(256) | Displays the SQL user name filter. |
| APPLICATION_USER_NAME | NVARCHAR(256) | Displays the application user name filter. |
| APPLICATION_NAME | NVARCHAR(256) | Displays the application name filter. |
| PASSPORT_TRACELEVEL | VARCHAR(8) | Displays the passport filter: MEDIUM/ HIGH. |
| PLAN_EXECUTION | VARCHAR(5) | Indicates whether plan execution details are recorded. |
| FUNCTION_PROFILER | VARCHAR(5) | Displays whether or not the function profiler details are recorded: TRUE/ FALSE. |
| ROOT_STATEMENT_HASH | VARCHAR(32) | Displays the root statement hash filter. |

## Related Information

ALTER SYSTEM {START | STOP} PERFTRACE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-START-STOP-PERFTRACE-Statement-System.md) ALTER SYSTEM SAVE PERFTRACE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-SAVE-PERFTRACE-Statement-System-Management.md)
