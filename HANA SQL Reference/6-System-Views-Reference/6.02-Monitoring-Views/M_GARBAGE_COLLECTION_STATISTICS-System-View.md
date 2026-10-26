# 6.2.119 M_GARBAGE_COLLECTION_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1806–1808

Provides garbage collection and history manager statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| STORE_TYPE | VARCHAR(16) | Displays the type of storage handled: COLUMN STORE/LIVECACHE. |
| HISTORY_COUNT | INTEGER | Displays the current count of history files in the garbage collection. |
| WAITER_COUNT | INTEGER | Displays the current count of garbage collection waiters. |
| MIN_READ_TID | BIGINT | Displays the last known minimum transaction ID (TID) of a reading trans action at end of transaction (EOT). |
| LAST_STARTED_TID | BIGINT | Displays the TID of the last started cleanup job. |
| LAST_STARTED_TID_POSTCOMMIT | BIGINT | Displays the TID of the last started postcommit job. |
| FIRST_WAITING_TID | BIGINT | Displays the TID of the first waiting cleanup job. |
| FIRST_WAITING_TID_POSTCOMMIT | BIGINT | Displays the TID of the first waiting postcommit job. |
| ENTERS | BIGINT | Displays the number of history files that entered the queue for cleanup. |
| ENTERS_POSTCOMMIT | BIGINT | Displays the number of history files that entered the queue for postcommit. |
| STARTED_JOBS | BIGINT | Displays the number of started garbage collection cleanup jobs. |
| STARTED_JOBS_POSTCOMMIT | BIGINT | Displays the number of started post commit jobs. |
| PROCESSED_JOBS | BIGINT | Displays the number of undo files processed for cleanup. |
| PROCESSED_JOBS_POSTCOMMIT | BIGINT | Displays the number of undo files processed for postcommit. |
| QUEUE_LOADS | BIGINT | Displays the number of all garbage collection queue loads. |
| QUEUE_LOADS_NONEMPTY | BIGINT | Displays the number of garbage collection queue loads which found elements. |
| QUEUE_EMPTY_COUNT | BIGINT | Displays the number of queue empty states after garbage collection finished. |
| SAVEPOINTS | BIGINT | Displays the number of savepoints. |
| LAST_HISTORY_SIZE_AT_SVP | BIGINT | Displays the lastest number of history files present at the savepoint. |
| MAX_HISTORY_SIZE_AT_SVP | BIGINT | Displays the maximum number of history files present at the savepoint. |
| MIN_HISTORY_SIZE_AT_SVP | BIGINT | Displays the minimum number of history files present at the savepoint. |
| SUM_HISTORY_SIZE_AT_SVP | BIGINT | Displays the total number of history files present at the savepoint. |
| AVG_HISTORY_SIZE_AT_SVP | DOUBLE | Displays the average number of history files present at the savepoint. |
| EMPTY_HISTORY_AT_SVP_COUNT | BIGINT | Displays the number of savepoints with an empty queue. |

## Additional Information

This view shows various statistics about garbage collection jobs.

Garbage collection is used to remove old versions of data objects from the system. Afterward, transactions cannot reference these old versions. References to these objects are kept in history (cleanup) files, which are processed by the garbage collector.

Normally, the system runs in statement consistency isolation level (that is, a consistent view is acquired when an SQL operation starts). Alternatively, the system can be run in transaction consistency isolation level, where the consistent view is acquired when the transaction starts and is held until the transaction terminates (snapshot isolation, similar to SERIALIZABLE isolation level). Each consistent view contains a reference to a minReadTID Transaction ID (TID), which is the minimum TID, from which the changes are "seen" by the transaction. Global minReadTID (minimum of minReadTIDs of all consistent views) is used by the garbage collector to determine which history files can be cleaned.

In cases where the history files accumulate and MIN_READ_TID does not advance, some transactions probably hold their consistent view for very long time (for example, a long-running transaction of a forgotten read transaction in a GUI). Query the M_TRANSACTIONS system view to see information about each running transaction.

This view has a resettable counterpart; you can see the values since the last reset in the M_GARBAGE_COLLECTION_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_GARBAGE_COLLECTION_STATISTICS_RESET;`.

## Related Information

M_GARBAGE_COLLECTION_STATISTICS_RESET System View [→](M_GARBAGE_COLLECTION_STATISTICS_RESET-System-View.md) M_TRANSACTIONS System View [→](M_TRANSACTIONS-System-View.md) ALTER SYSTEM RECLAIM VERSION SPACE Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RECLAIM-VERSION-SPACE-Statement-System.md) ALTER SYSTEM RESET MONITORING VIEW Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RESET-MONITORING-VIEW-Statement-System.md) ALTER SYSTEM RECLAIM FLEXIBLE TABLES Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RECLAIM-FLEXIBLE-TABLES-Statement-System.md)
