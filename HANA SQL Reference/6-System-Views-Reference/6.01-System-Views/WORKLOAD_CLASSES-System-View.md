# 6.1.193 WORKLOAD_CLASSES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1628–1629

Provides information about available workload classes.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| WORKLOAD_CLASS_NAME | NVARCHAR(256) | Displays the name of the workload class. |
| PRIORITY | INTEGER | Displays the priority. Zero is the lowest while nine is the highest priority and multiple workload classes can have the same priority. Five is the default. |
| STATEMENT_MEMORY_LIMIT | INTEGER | Displays the maximum memory allocation per statement, in gigabytes. |
| STATEMENT_THREAD_LIMIT | INTEGER | Displays the maximum number of parallel threads per statement. |
| TOTAL_STATEMENT_MEMORY_LIMIT | INTEGER | Displays the aggregated memory limit, in gigabytes, that applies to all statements currently being executed within the workload class. |
| TOTAL_STATEMENT_THREAD_LIMIT | INTEGER | Displays the aggregated thread limit that applies to all statements currently being executed within the workload class. |
| STATEMENT_TIMEOUT | INTEGER | Displays the timeout, in seconds, of the statement execution. |
| WRITE_TRANSACTION_LIFETIME | INTEGER | Displays the lifetime, in minutes, of long-running, uncommitted write trans actions. |
| IDLE_CURSOR_LIFETIME | INTEGER | Displays the lifetime, in minutes, of long-lived cursors. |
| IS_ENABLED | VARCHAR(5) | Displays whether or not the workload class is enabled: TRUE/FALSE. |

## Related Information

CREATE WORKLOAD CLASS Statement (Workload Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-WORKLOAD-CLASS-Statement-Workload-Management.md) ALTER WORKLOAD CLASS Statement (Workload Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-WORKLOAD-CLASS-Statement-Workload-Management.md) DROP WORKLOAD CLASS Statement (Workload Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-WORKLOAD-CLASS-Statement-Workload-Management.md) M_WORKLOAD System View [→](../6.02-Monitoring-Views/M_WORKLOAD-System-View.md) WORKLOAD_MAPPINGS System View [→](WORKLOAD_MAPPINGS-System-View.md)
