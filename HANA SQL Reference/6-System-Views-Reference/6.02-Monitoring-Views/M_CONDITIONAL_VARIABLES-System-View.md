# 6.2.42 M_CONDITIONAL_VARIABLES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1683–1684

Provides semaphore statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| STATISTICS_NAME | VARCHAR(128) | Displays the statistics object name. |
| STATISTICS_ID | BIGINT | Displays the statistics object unique ID. |
| WAIT_COUNT | BIGINT | Displays the count of wait calls. |
| BLOCKING_COUNT | BIGINT | Displays the count of blocking wait calls. |
| TIMEOUT_COUNT | BIGINT | Displays the count of timeouts. |
| WAIT_RATE | DOUBLE | Displays the wait rate percentage. |
| LAST_BLOCKING_TIME | BIGINT | Displays the latest time of blocking wait calls in microseconds. |
| MAX_BLOCKING_TIME | BIGINT | Displays the maximum time of blocking wait calls in microseconds. |
| MIN_BLOCKING_TIME | BIGINT | Displays the minimum time of blocking wait calls in microseconds. |
| SUM_BLOCKING_TIME | BIGINT | Displays the total time of blocking wait calls in microseconds. |
| AVG_BLOCKING_TIME | BIGINT | Displays the average time of blocking wait calls in microseconds. |
| CREATE_COUNT | BIGINT | Displays the count of semaphore creations (for shared statistics only). |
| DESTROY_COUNT | BIGINT | Displays the count of semaphore de structions (for shared statistics only). |
| COMPONENT | VARCHAR(32) | Displays the component. |

## Additional Information

This view contains information about single conditional variable objects or groups of conditional variable objects. It does not contain information about all conditional variables.

## Related Information

M_CONDITIONAL_VARIABLES_RESET System View [→](M_CONDITIONAL_VARIABLES_RESET-System-View.md) Session Variables [→](../../4-SQL-Reference/4.08-Session-Variables.md) Redirect Results to a File
