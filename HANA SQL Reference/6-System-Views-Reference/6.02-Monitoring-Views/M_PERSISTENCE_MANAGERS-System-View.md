# 6.2.202 M_PERSISTENCE_MANAGERS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1927–1929

Provides persistence manager statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| MAX_TID | BIGINT | Displays the maximum known TID. |
| CCH_COUNT | BIGINT | Displays the number of normal consistent changes in terminated sessions. |
| MASS_CCH_COUNT | BIGINT | Displays the number of consistent changes for mass operations in terminated sessions. |
| LAST_CCH_TIME | BIGINT | Displays the last time spent in normal consistent changes in terminated sessions in microseconds. |
| MAX_CCH_TIME | BIGINT | Displays the maximum time spent in normal consistent changes in terminated sessions in microseconds. |
| MIN_CCH_TIME | BIGINT | Displays the minimum time spent in normal consistent changes in terminated sessions in microseconds. |
| SUM_CCH_TIME | BIGINT | Displays the total time spent in normal consistent changes in terminated sessions in microseconds. |
| AVG_CCH_TIME | BIGINT | Displays the average time spent in normal consistent changes in terminated sessions in microseconds. |
| LAST_MASS_CCH_TIME | BIGINT | Displays the last time spent in consistent changes for mass operations in terminated sessions in microseconds. |
| MAX_MASS_CCH_TIME | BIGINT | Displays the maximum time spent in consistent changes for mass operations in terminated sessions in microseconds. |
| MIN_MASS_CCH_TIME | BIGINT | Displays the minimum time spent in consistent changes for mass operations in terminated sessions in microseconds. |
| SUM_MASS_CCH_TIME | BIGINT | Displays the total time spent in consistent changes for mass operations in terminated sessions in microseconds. |
| AVG_MASS_CCH_TIME | BIGINT | Displays the average time spent in consistent changes for mass operations in terminated sessions in microseconds. |
| PREPARE_COMMIT_POS | BIGINT | Displays the newest known log position of the prepare commit. This value is for the slave only. |
| MASTER_COMMIT_POS | BIGINT | Displays the newest known log position of the commit record on the transaction master from the point of view of this node. |
| INDOUBT_WAITERS | BIGINT | Displays the number of in-doubt waiters for the currently-running COMMIT. This value is for the master only. |
| INDOUBT_RESTART_COUNT | BIGINT | Displays the number of open in-doubt transactions before the restart. This value is for the master only. |
| INDOUBT_ONLINE_COUNT | BIGINT | Displays the number of open in-doubt transactions since the last restart. This value is for the master only. |
| SAVEPOINT_CONFIG_FREQUENCY | BIGINT | Displays the configured savepoint frequency in seconds. |
| SAVEPOINT_ACTIVE_FREQUENCY | BIGINT | Displays the currently active savepoint frequency in seconds. |
| CHECKSUM_ALGORITHM | VARCHAR(16) | Displays the currently used checksum algorithm for the modified pages and log buffers. |

## Additional Information

Persistence manager is the module responsible for low-level operations on the persistent data structures. This view shows various statistics counters, which are used to measure the performance of those operations.

This view has a resettable counterpart; you can see the values since the last reset in the M_PERSISTENCE_MANAGERS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_PERSISTENCE_MANAGERS_RESET;`.

## Related Information

M_PERSISTENCE_MANAGERS_RESET System View [→](M_PERSISTENCE_MANAGERS_RESET-System-View.md) M_GARBAGE_COLLECTION_STATISTICS System View [→](M_GARBAGE_COLLECTION_STATISTICS-System-View.md) ALTER SYSTEM PERSISTENCE ENCRYPTION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-PERSISTENCE-ENCRYPTION-Statement-System.md)
