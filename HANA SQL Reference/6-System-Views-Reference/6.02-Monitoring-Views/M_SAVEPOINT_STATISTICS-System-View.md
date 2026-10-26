# 6.2.245 M_SAVEPOINT_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1978–1982

Provides information about executed savepoints.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence Volume ID. |
| SAVEPOINTS | BIGINT | Displays the number of executed save points. |
| START_TIME | TIMESTAMP | Displays the start time of the last save point. |
| INITIATION | VARCHAR(24) | Displays the reason why the last save point was executed. |
| PURPOSE | VARCHAR(24) | Displays the reason why the last save point was executed. |
| STATE | VARCHAR(16) | Displays the last savepoint state. |
| VERSION | INTEGER | Displays the last savepoint version. |
| REQUESTED_FREQUENCY | BIGINT | Displays the currently active configured savepoint frequency in seconds. |
| LAST_FREQUENCY | BIGINT | Displays the actual frequency in seconds between the last two savepoints. |
| AVG_FREQUENCY | BIGINT | Displays the actual average frequency in seconds between last two save points. |
| LAST_DURATION | BIGINT | Displays the total time spent in microseconds creating the last savepoint. |
| AVG_DURATION | BIGINT | Displays the average time spent in microseconds creating the last two save points. |
| LAST_BLOCKING_PHASE_START_TIME | TIMESTAMP | Displays the start time of the last blocking phase. |
| LAST_BLOCKING_PHASE_DURATION | BIGINT | Displays the duration in seconds of the last blocking phase. |
| LAST_CRITICAL_PHASE_START_TIME | TIMESTAMP | Displays the start time of the last critical phase. |
| LAST_CRITICAL_PHASE_DURATION | BIGINT | Displays the time spent in microseconds in the last critical phase, during which updates are blocked. |
| AVG_CRITICAL_PHASE_DURATION | BIGINT | Displays the average time spent in microseconds for the last two critical phases, during which updates are blocked. |
| LAST_TOTAL_SIZE | BIGINT | Displays the total number of bytes written for the last savepoint. |
| AVG_TOTAL_SIZE | BIGINT | Displays the average number of bytes written for a savepoint. |
| LAST_FLUSHED_PAGES | BIGINT | Displays the last number of asynchronously flushed pages. |
| AVG_FLUSHED_PAGES | DOUBLE | Displays the average number of asynchronously flushed pages. |
| LAST_FLUSHED_PAGES_IN_CRITICAL_PHASE | BIGINT | Displays the last number of pages flushed in the critical phase. |
| AVG_FLUSHED_PAGES_IN_CRITICAL_PHASE | DOUBLE | Displays the average number of pages flushed in the critical phase. |
| LAST_FLUSHED_ROWSTORE_PAGES | BIGINT | Displays the last number of asynchronously flushed row store pages. |
| AVG_FLUSHED_ROWSTORE_PAGES | DOUBLE | Displays the average number of asynchronously flushed row store pages. |
| LAST_FLUSHED_ROWSTORE_PAGES_IN_CRITICAL_PHASE | BIGINT | Displays the last number of row store pages flushed in the critical phase. |
| AVG_FLUSHED_ROWSTORE_PAGES_IN_CRITICAL_PHASE | DOUBLE | Displays the average number of row store pages flushed in the critical phase. |
| LAST_FLUSHED_SIZE | BIGINT | Displays the size in bytes of the last asynchronously flushed pages. |
| AVG_FLUSHED_SIZE | BIGINT | Displays the average size in bytes of asynchronously flushed pages. |
| LAST_FLUSHED_SIZE_IN_CRITICAL_PHASE | BIGINT | Displays the size in bytes of the last pages flushed in the critical phase. |
| AVG_FLUSHED_SIZE_IN_CRITICAL_PHASE | BIGINT | Displays the average size of pages flushed in the critical phase. |
| LAST_FLUSHED_ROWSTORE_SIZE | BIGINT | Displays the size in bytes of the last asynchronously flushed row store pages. |
| AVG_FLUSHED_ROWSTORE_SIZE | BIGINT | Displays the average size in bytes of the asynchronously flushed row store pages. |
| LAST_FLUSHED_ROWSTORE_SIZE_IN_CRITICAL_PHASE | BIGINT | Displays the size in bytes of the last row store pages flushed in the critical phase. |
| AVG_FLUSHED_ROWSTORE_SIZE_IN_CRITICAL_PHASE | BIGINT | Displays the average size in bytes of the row store pages flushed in the critical phase. |
| LAST_RTT_SIZE | BIGINT | Displays the total size in bytes of the rollback transaction table at last save point. This may be less than the sum of components if there are duplicate TIDs. |

## Additional Information

This view shows information about executed savepoints, and is associated with the ALTER SYSTEM SAVEPOINT statement.

The `START_TIME`, `STATE`, `VERSION`, and `LAST_*` columns relate to the last executed or currently executing savepoint. Other columns contain aggregated values. Refer to the M_SAVEPOINTS system view for further information about various counters.

This view has a resettable counterpart; you can see the values since the last reset in the M_SAVEPOINT_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_SAVEPOINT_STATISTICS_RESET;`.

## Related Information

M_SAVEPOINT_STATISTICS_RESET System View [→](M_SAVEPOINT_STATISTICS_RESET-System-View.md) M_SAVEPOINTS System View [→](M_SAVEPOINTS-System-View.md) ALTER SYSTEM SAVEPOINT Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-SAVEPOINT-Statement-System-Management.md)
