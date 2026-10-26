# 6.2.248 M_SEMAPHORES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1983–1984

Provides semaphore statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| STATISTICS_NAME | VARCHAR(128) | Displays the statistics object name. |
| STATISTICS_ID | BIGINT | Displays the statistics object unique ID. |
| WAIT_COUNT | BIGINT | Displays the number of wait calls. |
| BLOCKING_COUNT | BIGINT | Displays the number of blocking wait calls. |
| TIMEOUT_COUNT | BIGINT | Displays the number of timeouts. |
| WAIT_RATE | DOUBLE | Displays the wait rate percentage. |
| LAST_BLOCKING_TIME | BIGINT | Displays the last time of blocking wait calls in microseconds. |
| MAX_BLOCKING_TIME | BIGINT | Displays the maximum time of blocking wait calls in microseconds. |
| MIN_BLOCKING_TIME | BIGINT | Displays the minimum time of blocking wait calls in microseconds. |
| SUM_BLOCKING_TIME | BIGINT | Displays the total time of blocking wait calls in microseconds. |
| AVG_BLOCKING_TIME | BIGINT | Displays the average time of blocking wait calls in microseconds. |
| CREATE_COUNT | BIGINT | Displays the number of semaphore creations (for shared statistics only). |
| DESTROY_COUNT | BIGINT | Displays the number of semaphore de structions (for shared statistics only). |
| COMPONENT | VARCHAR(32) | Displays the component. |

## Additional Information

This view contains information about single semaphore objects or groups of semaphore objects. It does not contain information about all semaphores.

This view has a resettable counterpart; you can see the values since the last reset in the M_SEMAPHORES_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_SEMAPHORES_RESET;`.

## Related Information

[M_SEMAPHORES_RESET System View](M_SEMAPHORES_RESET-System-View.md)
