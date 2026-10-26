# 6.2.356 M_WORKLOAD System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2148–2150

Provides information about the database workload collected every minute.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| EXECUTION_COUNT | BIGINT | Displays the total count of all executed statements for data manipulation, data definition, and system control. |
| COMPILATION_COUNT | BIGINT | Displays the number of statement preparation. |
| UPDATE_TRANSACTION_COUNT | BIGINT | Displays the number of update transactions. |
| COMMIT_COUNT | BIGINT | Displays the number of transaction commits. |
| ROLLBACK_COUNT | BIGINT | Displays the number of transaction rollbacks. |
| CURRENT_EXECUTION_RATE | DOUBLE | Displays the current statement execution count per minute. |
| PEAK_EXECUTION_RATE | DOUBLE | Displays the peak statement execution count per minute. |
| CURRENT_COMPILATION_RATE | DOUBLE | Displays the current statement preparation count per minute. |
| PEAK_COMPILATION_RATE | DOUBLE | Displays the peak statement preparation count per minute. |
| CURRENT_UPDATE_TRANSACTION_RATE | DOUBLE | Displays the current update transaction count per minute. |
| PEAK_UPDATE_TRANSACTION_RATE | DOUBLE | Displays the peak update transaction count per minute. |
| CURRENT_TRANSACTION_RATE | DOUBLE | Displays the current transaction count per minute. |
| PEAK_TRANSACTION_RATE | DOUBLE | Displays the peak transaction count per minute. |
| CURRENT_COMMIT_RATE | DOUBLE | Displays the total number of commits per minute. |
| PEAK_COMMIT_RATE | DOUBLE | Displays the peak commit counts per minute. |
| CURRENT_ROLLBACK_RATE | DOUBLE | Displays the total number of rollbacks per minute. |
| PEAK_ROLLBACK_RATE | DOUBLE | Displays the peak rollback count per minute. |
| CURRENT_MEMORY_USAGE_RATE | DOUBLE | Displays the total size of used memory per minute in bytes. |
| PEAK_MEMORY_USAGE_RATE | DOUBLE | Displays the peak size of used memory per minute in bytes. |

## Related Information

M_WORKLOAD_CAPTURES System View [→](M_WORKLOAD_CAPTURES-System-View.md) M_WORKLOAD_REPLAYS System View [→](M_WORKLOAD_REPLAYS-System-View.md) M_WORKLOAD_REPLAY_PREPROCESSES System View [→](M_WORKLOAD_REPLAY_PREPROCESSES-System-View.md) CREATE WORKLOAD CLASS Statement (Workload Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-WORKLOAD-CLASS-Statement-Workload-Management.md) ALTER WORKLOAD CLASS Statement (Workload Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-WORKLOAD-CLASS-Statement-Workload-Management.md) ALTER WORKLOAD MAPPING Statement (Workload Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-WORKLOAD-MAPPING-Statement-Workload-Management.md) CREATE WORKLOAD MAPPING Statement (Workload Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-WORKLOAD-MAPPING-Statement-Workload-Management.md) DROP WORKLOAD CLASS Statement (Workload Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-WORKLOAD-CLASS-Statement-Workload-Management.md) DROP WORKLOAD MAPPING Statement (Workload Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-WORKLOAD-MAPPING-Statement-Workload-Management.md)
