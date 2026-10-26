# 6.2.276 M_SQL_PLAN_CACHE_EXECUTION_LOCATION_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2028–2029

Provides statistics for hosts where plans were executed.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| PLAN_ID | BIGINT | Displays the logical plan ID as a non-negative value. |
| EXECUTION_HOST | VARCHAR(64) | Displays the host where the plan was executed. |
| EXECUTION_PORT | INTEGER | Displays the port where the plan was executed. |
| TOTAL_MEMORY_SIZE | BIGINT | Displays the total size of the tracked memory consumption in bytes. |
| AVG_MEMORY_SIZE | BIGINT | Displays the average size of the tracked memory consumption in bytes. |
| MIN_MEMORY_SIZE | BIGINT | Displays the minimum size of the tracked memory consumption in bytes. |
| MAX_MEMORY_SIZE | BIGINT | Displays the maximum size of the tracked memory consumption in bytes. |

## Additional Information

This view has a resettable counterpart; you can see the values since the last reset in the M_SQL_PLAN_CACHE_EXECUTION_LOCATION_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_SQL_PLAN_CACHE_EXECUTION_LOCATION_STATISTICS_RESET;`.

## Related Information

ALTER SYSTEM RESET MONITORING VIEW Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RESET-MONITORING-VIEW-Statement-System.md) M_SQL_PLAN_CACHE_EXECUTION_LOCATION_STATISTICS_RESET System View [→](M_SQL_PLAN_CACHE_EXECUTION_LOCATION_STATISTICS_RESET-System.md)
