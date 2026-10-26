# 6.2.184 M_MUTEXES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1908–1910

Provides information about single mutex (mutual exclusion) objects or groups of mutex objects.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID |
| STATISTICS_NAME | VARCHAR(128) | Displays the statistics object name. |
| STATISTICS_ID | BIGINT | Displays the statistics object unique ID. |
| LOCK_COUNT | BIGINT | Displays the number of lock calls. |
| WAIT_COUNT | BIGINT | Displays the number of blocking lock calls. |
| SPURIOUS_WAKEUP_COUNT | BIGINT | Displays the number of spurious wake ups (collisions on futex). |
| COLLISION_RATE | DOUBLE | Displays the collision rate percentage. |
| OWNER_ID | BIGINT | Displays the context ID of the owner context. |
| LAST_WAIT_TIME | BIGINT | Displays the last time of the blocking lock calls in microseconds. |
| MAX_WAIT_TIME | BIGINT | Displays the maximum time of the blocking lock calls in microseconds. |
| MIN_WAIT_TIME | BIGINT | Displays the minimum time of the blocking lock calls in microseconds. |
| SUM_WAIT_TIME | BIGINT | Displays the total time of the blocking lock calls in microseconds. |
| AVG_WAIT_TIME | BIGINT | Displays the average time of the blocking lock calls in microseconds. |
| CREATE_COUNT | BIGINT | Displays the number of mutex creations (for shared statistics only). |
| DESTROY_COUNT | BIGINT | Displays the number of mutex destructions (for shared statistics only). |
| COMPONENT | VARCHAR(32) | Displays the component. |

## Additional Information

M_MUTEXES does not contain information about all mutex objects. Information like LOCK_COUNT, WAIT_COUNT and WAIT_TIMES can be used to analyze performance bottlenecks. You can find possible deadlocks using the OWNER_ID column.

This view has a resettable counterpart; you can see the values since the last reset in the M_MUTEXES_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_MUTEXES_RESET;`.

## Related Information

M_MUTEXES_RESET System View [→](M_MUTEXES_RESET-System-View.md) M_LOAD_HISTORY_SERVICE System View [→](M_LOAD_HISTORY_SERVICE-System-View.md)
