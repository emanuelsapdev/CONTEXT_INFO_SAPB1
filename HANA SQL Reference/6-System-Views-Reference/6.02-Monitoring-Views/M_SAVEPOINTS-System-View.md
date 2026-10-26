# 6.2.244 M_SAVEPOINTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1974–1978

Displays current and historical savepoint statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| START_TIME | TIMESTAMP | Displays the savepoint start time. |
| INITIATION | VARCHAR(24) | Displays the reason why the savepoint was executed. |
| PURPOSE | VARCHAR(24) | Displays the purpose of the savepoint. |
| STATE | VARCHAR(16) | Displays the savepoint state. A save point is triggered periodically, but it can be also triggered on demand using the ALTER SYSTEM SAVEPOINT statement or by a data backup. The savepoint then runs through the following various states:<br>• `INITIAL` - Displays the empty statistics record (just allocated); immediately goes to the `PREPARE` state.<br>• `PREPARE` - Displays that the save point is preparing to run.<br>• `PAGEFLUSH` - flushes dirty pages asynchronously. `PAGES` and `SIZE` counters are updated to reflect the savepoint progress.<br>• `PRECRITICAL` - runs any pre-critical-phase callbacks and waits for I/O of the rest of the flushed pages.<br>• `ENTERCRITICAL` - entering critical phase: stops updaters and waits for the critical phase lock.<br>• `CRITICAL` - critical phase: copies and triggers the write of any pages that are still dirty, records various information in the restart record (log position, transaction manager state, and so on), and increments the savepoint version. `PAGES_IN_CRITICAL_PHASE` and `SIZE_IN_CRITICAL_PHASE` counters are updated appropri ately.<br>• `EXITCRITICAL` - exit critical phase: releases critical phase locks and restarts updaters.<br>• `POSTCRITICAL` - calls any post-critical phase callbacks, finalizes the savepoint record, and cleans up unneeded RTT entries. |
|   |   | • `FINISHING` - waits for the flush of pages written in the critical phase and writes out the restart record and anchor page.<br>• `DONE` - Displays that the savepoint has been completed successfully.<br>• `ABORTED` - Displays that the save point has been aborted (for example, due to a timeout during the synchronization of the global save point). |
| VERSION | INTEGER | Displays the savepoint version. |
| REQUESTED_FREQUENCY | BIGINT | Displays the frequency of the savepoint. |
| TIME_SINCE_PREVIOUS | BIGINT | Displays the time in seconds between the current and previous current save points. |
| DURATION | BIGINT | Displays the total time in microseconds to create the savepoint. |
| PREPARE_FLUSH_RETRY_COUNT | BIGINT | Displays the number of times the pages were flushed in the non-critical phase before entering the critical phase. |
| BLOCKING_PHASE_START_TIME | TIMESTAMP | Displays the start time of the last blocking phase. |
| BLOCKING_PHASE_DURATION | BIGINT | Displays the phase duration in microseconds. |
| CRITICAL_PHASE_START_TIME | TIMESTAMP | Displays the start time of the last critical phase. |
| CRITICAL_PHASE_DURATION | BIGINT | Displays the time in microseconds spent in the critical phase, during which updates are blocked. |
| CRITICAL_PHASE_WAIT_TIME | BIGINT | Displays the wait time in microseconds for the critical phase. |
| TOTAL_SIZE | BIGINT | Displays the number of bytes that have been prompted to be written to the disk. |
| FLUSHED_PAGES | BIGINT | Displays the number of asynchronously flushed pages. |
| FLUSHED_PAGES_IN_CRITICAL_PHASE | BIGINT | Displays the number of pages flushed in the critical phase. |
| FLUSHED_ROWSTORE_PAGES | BIGINT | Displays the number of asynchronously flushed row store pages. |
| FLUSHED_ROWSTORE_PAGES_IN_CRITICAL_PHASE | BIGINT | Displays the number of row store pages flushed in the critical phase. |
| FLUSHED_SIZE | BIGINT | Displays the size of asynchronously flushed pages in bytes. |
| FLUSHED_SIZE_IN_CRITICAL_PHASE | BIGINT | Displays the size in bytes of pages flushed in the critical phase. |
| FLUSHED_ROWSTORE_SIZE | BIGINT | Displays the size in bytes of the asynchronously flushed row store pages. |
| FLUSHED_ROWSTORE_SIZE_IN_CRITICAL_PHASE | BIGINT | Displays the size of the row store pages flushed in the critical phase . |
| RTT_SIZE | BIGINT | Displays the total size in bytes of the rollback transaction table at the save point. |

## Additional Information

This monitor view contains information about the current and some past savepoints. Information is kept on the last 128 savepoints per persistence manager.

> **Note**
>
> Only savepoint information since the startup is kept. The information in this monitor view does not persist. The statistics server collects some information about savepoints that persists.

This view is associated with the ALTER SYSTEM SAVEPOINT statement.

The following information can be extracted from the numbers in this view:

- `CRITICAL_PHASE_DURATION` shows the period of time during which the updaters were blocked in a savepoint. Normally, this should be in the millisecond range, except for global savepoints for data backup, which may take longer due to global synchronization across all nodes. If the critical phase duration is too long, there may be a problem (for example, the I/O load is too high).
- `DURATION` shows the total time taken by a savepoint. This should be significantly less than the configured savepoint frequency `REQUESTED_FREQUENCY` (in the range 0-10%, depending on the load). Higher ratios indicate an I/O overload.
- `TIME_SINCE_PREVIOUS` should be close to `REQUESTED_FREQUENCY`. If it is significantly higher, this indicates that the savepoint is encountering a block, such as a very long column merge operation.
- A ratio of `FLUSHED_PAGES*` vs. `FLUSHED_ROWSTORE_PAGES*` or a ratio of `FLUSHED_SIZE*` vs. `FLUSHED_ROWSTORE_SIZE*` shows the respective load of column store vs. row store. The row store is only flushed during the savepoint, and the column store also flushes the data between savepoints to balance the load.
- A high ratio of `FLUSHED_*PAGES_IN_CRITICAL_PHASE` vs. `FLUSHED_*PAGES` or a ratio of `FLUSHED_*SIZE_IN_CRITICAL_PHASE` vs. `FLUSHED_*SIZE` indicates a potential I/O overload. Normally, zero or only a few pages should be written in the critical phase, except for special situations like a global savepoint for data backups (but in this case, the number of pages written in the critical phase should be in the order of the magnitude, 1% or less, of asynchronously flushed pages). High amounts of data written in the critical phase indicates an overload of the I/O subsystem and can lead to increased blocking times of update transactions due to an increased `CRITICAL_PHASE_DURATION`.
- A big `RTT_SIZE` (more than a few entries) indicates a problem in distributed transaction handling. RTT (rollback transaction table) holds rollback entries for distributed transactions that are currently in rollback. Normally, these entries are eliminated quickly after the respective rollback is finished. In cases where a slave node fails, entries for the slave node are held persistently until the slave node restarts. This number goes to zero or close to zero shortly after the restart of a failed slave node (or after the restart of the whole system).

Aggregated values for individual counters can be queried from the M_SAVEPOINT_STATISTICS system view.

## Related Information

M_SAVEPOINT_STATISTICS System View [→](M_SAVEPOINT_STATISTICS-System-View.md) ALTER SYSTEM SAVEPOINT Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-SAVEPOINT-Statement-System-Management.md)
