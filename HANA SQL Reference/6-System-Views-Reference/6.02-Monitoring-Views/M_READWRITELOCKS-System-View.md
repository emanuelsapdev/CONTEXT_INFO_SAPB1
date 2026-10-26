# 6.2.214 M_READWRITELOCKS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1942–1945

Provides read and write lock statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| STATISTICS_NAME | VARCHAR(128) | Displays the statistics object name. |
| STATISTICS_ID | BIGINT | Displays the statistics object unique ID. |
| OWNER_ID | BIGINT | Displays the context ID of the owner context (for exclusive/intent locks). |
| EXCLUSIVE_LOCK_COUNT | BIGINT | Displays the number of exclusive lock calls. |
| EXCLUSIVE_WAIT_COUNT | BIGINT | Displays the number of blocking exclusive lock calls. |
| EXCLUSIVE_CAS_COLLISION_COUNT | BIGINT | Displays the collision count on atomic operations on exclusive locks. |
| EXCLUSIVE_COLLISION_RATE | DOUBLE | Displays the collision rate on exclusive locks percentage. |
| LAST_EXCLUSIVE_WAIT_TIME | BIGINT | Displays the last time of blocking exclusive lock calls in microseconds. |
| MAX_EXCLUSIVE_WAIT_TIME | BIGINT | Displays the maximum time of blocking exclusive lock calls in microseconds. |
| MIN_EXCLUSIVE_WAIT_TIME | BIGINT | Displays the minimum time of blocking exclusive lock calls in microseconds. |
| SUM_EXCLUSIVE_WAIT_TIME | BIGINT | Displays the total time of blocking exclusive lock calls in microseconds. |
| AVG_EXCLUSIVE_WAIT_TIME | BIGINT | Displays the average time of blocking exclusive lock calls in microseconds. |
| INTENT_LOCK_COUNT | BIGINT | Displays the number of intent lock calls. |
| INTENT_WAIT_COUNT | BIGINT | Displays the number of blocking intent lock calls. |
| INTENT_CAS_COLLISION_COUNT | BIGINT | Displays the collision count on atomic operation on intent lock. |
| INTENT_TIMEOUT_COUNT | BIGINT | Displays the number of timed out intent lock calls. |
| INTENT_COLLISION_RATE | DOUBLE | Displays the collision rate on intent locks percentage. |
| LAST_INTENT_WAIT_TIME | BIGINT | Displays the last time of blocking intent lock calls in microseconds. |
| MAX_INTENT_WAIT_TIME | BIGINT | Displays the maximum time of blocking intent lock calls in microseconds. |
| MIN_INTENT_WAIT_TIME | BIGINT | Displays the minimum time of blocking intent lock calls in microseconds. |
| SUM_INTENT_WAIT_TIME | BIGINT | Displays the total time of blocking intent lock calls in microseconds. |
| AVG_INTENT_WAIT_TIME | BIGINT | Displays the average time of blocking intent lock calls in microseconds. |
| SHARED_LOCK_COUNT | BIGINT | Displays the number of shared lock calls. |
| SHARED_WAIT_COUNT | BIGINT | Displays the number of blocking shared lock calls. |
| SHARED_CAS_COLLISION_COUNT | BIGINT | Displays the collision count on atomic operation on shared lock. |
| SHARED_TIMEOUT_COUNT | BIGINT | Displays the number of timed out shared lock calls. |
| SHARED_COLLISION_RATE | DOUBLE | Displays the collision rate on shared lock percentage. |
| LAST_SHARED_WAIT_TIME | BIGINT | Displays the last time of blocking shared lock calls in microseconds. |
| MAX_SHARED_WAIT_TIME | BIGINT | Displays the maximum time of blocking shared lock calls in microseconds. |
| MIN_SHARED_WAIT_TIME | BIGINT | Displays the minimum time of blocking shared lock calls in microseconds. |
| SUM_SHARED_WAIT_TIME | BIGINT | Displays the total time of blocking shared lock calls in microseconds. |
| AVG_SHARED_WAIT_TIME | BIGINT | Displays the average time of blocking shared lock calls in microseconds. |
| COLLISION_RATE | DOUBLE | Displays the global collision rate percentage. |
| CREATE_COUNT | BIGINT | Displays the number of read and write lock creation (for shared statistics only). |
| DESTROY_COUNT | BIGINT | Displays the number of read/write lock destructions (for shared statistics only). |
| COMPONENT | VARCHAR(32) | Displays the component. |

## Additional Information

This view contains information about single, or groups, of reader and writer lock objects. It does not contain information about all reader and writer lock. Information like LOCK_COUNT, WAIT_COUNT, and WAIT_TIMES can be used to analyze performance bottlenecks.

This view has a resettable counterpart; you can see the values since the last reset in the M_READWRITELOCKS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_READWRITELOCKS_RESET;`.

## Related Information

[M_READWRITELOCKS_RESET System View](M_READWRITELOCKS_RESET-System-View.md)

[LOCK TABLE Statement (Transaction Management)](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/LOCK-TABLE-Statement-Transaction-Management.md)
