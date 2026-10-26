# 6.2.163 M_LOCK_WAITS_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1878–1879

Provides the accumulated lock wait count and duration for record locks, table locks, and metadata locks for all available services from database start up until the current time.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| LOCK_TYPE | VARCHAR(32) | Displays the lock type: RECORD/ TABLE. |
| TOTAL_LOCK_WAITS | BIGINT | Displays the total lock wait count. |
| TOTAL_LOCK_WAIT_TIME | BIGINT | Displays the total lock wait duration in microseconds. |

## Related Information

[LOCK TABLE Statement (Transaction Management)](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/LOCK-TABLE-Statement-Transaction-Management.md)
