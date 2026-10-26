# 6.2.1 M_ABSTRACT_SQL_PLAN_OVERVIEW System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1635–1637

Provides the status of each Plan Stability Manager on every index server in SAP HANA.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| STATE | VARCHAR(16) | Displays the Plan Stability Manager state:<br>• READY: plan stability is enabled.<br>• CAPTURE: the abstract SQL plans are being captured.<br>• APPLY: the captured abstract SQL plans are being applied for execution plan generation.<br>• IMPORT: the abstract SQL plans are being imported.<br>• MIGRATION: the abstract SQL plans are being migrated.<br>• UPDATE LOCATION: the location information of the captured abstract SQL plans is being updated. |
| TOTAL_PLAN_COUNT | BIGINT | Displays the total number of enabled and disabled loaded plans. |
| ENABLED_PLAN_COUNT | BIGINT | Displays the total number of enabled plans. |
| DISABLED_PLAN_COUNT | BIGINT | Displays the total number of disabled plans. |
| ALLOCATED_MEMORY_SIZE | BIGINT | Displays the allocated memory size, in bytes, being used by plan stability. |
| LAST_APPLY_START_TIME | TIMESTAMP | Displays the last APPLY start time. |
| LAST_APPLY_STOP_TIME | TIMESTAMP | Displays the last APPLY stop time. |
| LAST_CAPTURE_START_TIME | TIMESTAMP | Displays the last CAPTURE start time. |
| LAST_CAPTURE_STOP_TIME | TIMESTAMP | Displays the last CAPTURE stop time. |
| FILTERS | NCLOB | Displays the application filters of the abstract SQL plan. |

## Related Information

ABSTRACT_SQL_PLANS System View [→](../6.01-System-Views/ABSTRACT_SQL_PLANS-System-View.md) ALTER SYSTEM {ENABLE | DISABLE | REMOVE} ABSTRACT SQL PLAN (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ENABLE-DISABLE-REMOVE-ABSTRACT-SQL-PLAN-System.md) ALTER SYSTEM MIGRATE ABSTRACT SQL PLAN (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-MIGRATE-ABSTRACT-SQL-PLAN-System-Management.md) ALTER SYSTEM {START | STOP} CAPTURE ABSTRACT SQL PLAN (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-START-STOP-CAPTURE-ABSTRACT-SQL-PLAN-System.md) ALTER SYSTEM {START | STOP} APPLY ABSTRACT SQL PLAN (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-START-STOP-APPLY-ABSTRACT-SQL-PLAN-System.md) ALTER SYSTEM UPDATE ABSTRACT SQL PLAN Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-UPDATE-ABSTRACT-SQL-PLAN-Statement-System.md) M_ABSTRACT_SQL_PLAN_STATISTICS System View [→](M_ABSTRACT_SQL_PLAN_STATISTICS-System-View.md)
