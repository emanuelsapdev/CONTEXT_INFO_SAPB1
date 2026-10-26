# 6.2.164 M_LOG_BUFFERS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1879–1880

Provides information about log buffer statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| LOG_MODE | VARCHAR(16) | Displays the log mode. |
| BUFFER_SIZE | BIGINT | Displays the size of one log buffer in memory in kilobytes. |
| BUFFER_COUNT | BIGINT | Displays the count of log buffers in memory. |
| SEGMENT_SIZE | BIGINT | Displays the maximum size of one log segment in megabytes. |
| BACKUP_ENABLED | VARCHAR(5) | Displays whether the log segment backup is enabled: TRUE, FALSE (FALSE on log backup history broken). |
| BACKUP_TIMEOUT | BIGINT | Displays the log segment backup time out in seconds. |
| SWITCH_NOWAIT_COUNT | BIGINT | Displays the count of buffer switches without blocking on buffer semaphore. |
| SWITCH_WAIT_COUNT | BIGINT | Displays the count of buffer switches with blocking on buffer semaphore. |
| SWITCH_OPEN_COUNT | BIGINT | Displays the count of ignored still-open buffer switches (resolved races). |

## Additional Information

The current configuration of in-memory log buffers is shown in the BUFFER_SIZE and BUFFER_COUNT columns. This defines how much log information can be collected transiently in memory, before the log queue becomes full.

Counters for buffer switches indicate performance of the in-memory log buffers. Normally, buffer switching happens without any waits. In the case of buffer full, however, a wait is necessary. Then, SWITCH_WAIT_COUNT is incremented, otherwise SWITCH_NOWAIT_COUNT is incremented. If the wait ratio is higher than one percent, this indicates a possible misconfiguration of the system. In this case:

- Check if regular peaks exceed current log buffer configuration and if so, increase log buffer size and/or count
- Check if the I/O subsystem is performing poorly (see the M_VOLUME_IO_TOTAL_STATISTICS system view).

Due to the lock-free nature of the algorithm used, some race conditions can happen. These are properly detected and resolved. Additionally, a count of such races is recorded in SWITCH_OPEN_COUNT. Normally, the ratio of races to buffer switches should also be under one percent even for high workloads.

This view has a resettable counterpart; you can see the values since the last reset in the M_LOG_BUFFERS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_LOG_BUFFERS_RESET;`.

## Related Information

M_LOG_BUFFERS_RESET System View [→](M_LOG_BUFFERS_RESET-System-View.md) M_VOLUME_IO_TOTAL_STATISTICS System View [→](M_VOLUME_IO_TOTAL_STATISTICS-System-View.md) M_LOG_PARTITIONS System View [→](M_LOG_PARTITIONS-System-View.md) M_LOG_SEGMENTS System View [→](M_LOG_SEGMENTS-System-View.md) M_VOLUME_IO_TOTAL_STATISTICS System View [→](M_VOLUME_IO_TOTAL_STATISTICS-System-View.md)
