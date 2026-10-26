# 6.2.85 M_DELTA_MERGE_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1755–1759

Provides information on table delta merge statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| TYPE | VARCHAR(8) | Displays the type of the statistic:<br>**MERGE**<br>The table delta merge. **HINT**<br>The application merge hint. **SPARSE**<br>Optimizes compression. **FACT**<br>The fact table compression. **RECLAIM**<br>The table delta garbage collection. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| TABLE_OID | BIGINT | Displays the object ID of the table. |
| PART_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| PHYSICAL_PART_ID | INTEGER | Displays the physical partition ID. |
| HISTORY | VARCHAR(5) | Displays a flag, which indicates that the history part was merged: TRUE/FALSE. |
| MEMORY_MERGE | VARCHAR(5) | Deprecated: Displays a flag, which indicates that the table was merged in memory only: TRUE/FALSE. |
| PASSPORT | VARCHAR(256) | Displays the external identifier for the table merge called by an application. |
| LOG_REPLAY_QUEUE_ID | INTEGER | Displays the ID of the log replay queue where the job was started. During log replay, only delta merge and optimize compression operations are possible. |
| START_TIME | TIMESTAMP | Displays the execution start time. |
| WAIT_TIME_FREE_RESOURCES | BIGINT | Displays the time to wait for memory and CPU resources when too many merges or optimized compressions have been started in parallel. |
| WAIT_TIME_HESITANT_LOCK_PHASE_1 | BIGINT | Displays the total wait time for acquiring exclusive lock in first exclusive merge phase with configured timeout and subsequent retries. |
| WAIT_TIME_EXCLUSIVE_LOCK_PHASE_1 | BIGINT | Displays the time it takes to acquire exclusive lock in first exclusive merge phase in case the hesitant acquire was not successful. New readers and writers are already blocked. |
| DURATION_EXCLUSIVE_LOCK_PHASE_1 | BIGINT | Displays the time spent under exclusive lock in first exclusive merge phase. |
| WAIT_TIME_HESITANT_LOCK_PHASE_2 | BIGINT | Displays the total wait time for acquiring exclusive lock in second exclusive merge respectively exclusive optimize compression phase with configured timeout and subsequent retries. |
| WAIT_TIME_EXCLUSIVE_LOCK_PHASE_2 | BIGINT | Displays the time it takes to acquire exclusive lock in second exclusive merge respectively exclusive optimize compression phase in case the hesitant acquire was not successful. New readers and writers are already blocked. |
| DURATION_EXCLUSIVE_LOCK_PHASE_2 | BIGINT | Displays the time spent under exclusive lock in second exclusive merge respectively exclusive optimize compression phase. |
| EXECUTION_TIME | BIGINT | Displays the execution duration in milliseconds. |
| MOTIVATION | VARCHAR(9) | Displays the motivation of the statistics:<br>**AUTO**<br>Triggered based on an automatic decision function. **SMART**<br>Triggered by a HINT from the user based on a smart decision function. **CRITICAL**<br>Triggered based on a critical decision function. **HARD**<br>Triggered via SQL based on a hard decision function. **FORCED**<br>A merge triggered via SQL, circum venting resource availability checks, based on a forced decision function. |
| SUCCESS | VARCHAR(5) | Displays a call success flag, which depends on the field TYPE.<br>**HINT**<br>Displays whether the application merge hint was accepted or rejected. **MERGE/SPARSE**<br>Displays whether the delta merge/ optimize compression was completed with or without success: TRUE/FALSE. For example, a table delta merge call which did not result in a delta merge because the delta was empty, is indicated with FALSE. |
| MERGED_DELTA_RECORDS | INTEGER | Displays the number of rows merged from old delta1 to new main. Number of rows evicted from delta during reclaim delta operation. -1 for other operation types. |
| OLD_MAIN_STILL_IN_USE | VARCHAR(5) | Displays the flag whether the old main is still in use by old readers at the end of the merge or optimize compression and will only be deleted after the last reader has finished. FALSE for other operation types. |
| OLD_DELTA_STILL_IN_USE | VARCHAR(5) | Displays the flag whether the old delta1 is still in use by old readers at the end of the merge and will only be deleted after the last reader has finished. FALSE for other operation types. |
| LAST_ERROR | INTEGER | Displays the error code of the last error that occurred. This explains why a merge did not succeed. See ERROR_DESCRIPTION for details. |
| CS_ERROR | INTEGER | Displays the column store specific error code. See ERROR_DESCRIPTION for details |
| ERROR_DESCRIPTION | NVARCHAR(2000) | Displays the description of the last error that occurred during the merge. A failing merge does not necessarily indicate a problem. |

## Additional Information

Table delta merges, optimize compression runs, and application merge hints are listed separately.

## Related Information

MERGE DELTA Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/MERGE-DELTA-Statement-Data-Manipulation.md) MERGE INTO Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/MERGE-INTO-Statement-Data-Manipulation.md) M_ES_DELTA_MERGE_STATISTICS System View [→](M_ES_DELTA_MERGE_STATISTICS-System-View.md)
