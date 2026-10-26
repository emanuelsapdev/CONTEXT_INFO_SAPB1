# 6.2.347 M_VOLUME_IO_PERFORMANCE_STATISTICS System View - Deprecated

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2128–2136

Deprecated. Use M_VOLUME_IO_TOTAL_STATISTICS instead.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| PATH | VARCHAR(512) | Displays the filesystem path. |
| FILESYSTEM_TYPE | VARCHAR(32) | Displays the filesystem type. |
| TYPE | VARCHAR(16) | Displays the type of contained files. |
| MAX_IO_BUFFER | BIGINT | Displays the maximum I/O buffer size in bytes. |
| READ_SYNC | BIGINT | Displays the number of synchronous reads. |
| WRITE_SYNC | BIGINT | Displays the number of synchronous writes. |
| READ_REQUESTS | BIGINT | Displays the number of read requests. |
| WRITE_REQUESTS | BIGINT | Displays the number of write requests. |
| READ_COMPLETIONS | BIGINT | Displays the number of read completions. |
| FAILED_READS | BIGINT | Displays the number of failed reads. |
| WRITE_COMPLETIONS | BIGINT | Displays the number of write completions. |
| FAILED_WRITES | BIGINT | Displays the number of failed writes. |
| FULL_RETRY_READS | BIGINT | Displays the number of full retry reads. |
| FULL_RETRY_WRITES | BIGINT | Displays the number of full retry writes. |
| SHORT_READS | BIGINT | Displays the number of short reads. |
| SHORT_WRITES | BIGINT | Displays the number of short writes. |
| DELAYED_READ_REQUESTS | BIGINT | Displays the number of delayed read requests. |
| DELAYED_WRITE_REQUESTS | BIGINT | Displays the number of delayed write requests. |
| DEQUEUED_DELAYED_REQUESTS | BIGINT | Displays the number of dequeued delayed requests. |
| RESUBMITTED_DELAYED_REQUESTS | BIGINT | Displays the number of resubmitted delayed requests. |
| RESUBMITTED_DELAYED_REQUESTS_DELAYED_AGAIN | BIGINT | Displays the number of resubmitted delayed requests delayed. |
| ITEMS_IN_DELAY_QUEUE | BIGINT | Displays the number of items in the delay queue. |
| MAX_ITEMS_IN_DELAY_QUEUE | BIGINT | Displays the maximum size of the delay queue in bytes. |
| LAST_READ_SYNC_TIME | BIGINT | Displays the last time for synchronous reads. |
| MAX_READ_SYNC_TIME | BIGINT | Displays the maximum time for synchronous reads. |
| MIN_READ_SYNC_TIME | BIGINT | Displays the minimum time for synchronous reads. |
| SUM_READ_SYNC_TIME | BIGINT | Displays the total time for synchronous reads. |
| AVG_READ_SYNC_TIME | BIGINT | Displays the average time for synchronous reads. |
| LAST_WRITE_SYNC_TIME | BIGINT | Displays the last time for synchronous writes. |
| MAX_WRITE_SYNC_TIME | BIGINT | Displays the minimum time for synchronous writes. |
| MIN_WRITE_SYNC_TIME | BIGINT | Displays the minimum time for synchronous writes. |
| SUM_WRITE_SYNC_TIME | BIGINT | Displays the total time for synchronous writes. |
| AVG_WRITE_SYNC_TIME | BIGINT | Displays the average time for synchronous writes. |
| LAST_READ_TIME | BIGINT | Displays the last time for read events. |
| MAX_READ_TIME | BIGINT | Displays the maximum time for read events. |
| MIN_READ_TIME | BIGINT | Displays the minimum time for read events. |
| SUM_READ_TIME | BIGINT | Displays the total time for read events. |
| AVG_READ_TIME | BIGINT | Displays the average time for read events. |
| LAST_WRITE_TIME | BIGINT | Displays the last time for write events. |
| MAX_WRITE_TIME | BIGINT | Displays the maximum time for write events. |
| MIN_WRITE_TIME | BIGINT | Displays the minimum time for write events. |
| SUM_WRITE_TIME | BIGINT | Displays the total time for write events. |
| AVG_WRITE_TIME | BIGINT | Displays the average time for write events. |
| LAST_READ_ENQUEUE_TIME | BIGINT | Displays the last time for enqueuing read I/O events. |
| MAX_READ_ENQUEUE_TIME | BIGINT | Displays the maximum time for en queuing read I/O events. |
| MIN_READ_ENQUEUE_TIME | BIGINT | Displays the minimum time for enqueuing read I/O events. |
| SUM_READ_ENQUEUE_TIME | BIGINT | Displays the total time for enqueuing read I/O events. |
| AVG_READ_ENQUEUE_TIME | BIGINT | Displays the average time for enqueuing read I/O events. |
| LAST_WRITE_ENQUEUE_TIME | BIGINT | Displays the last time for enqueuing write I/O events. |
| MAX_WRITE_ENQUEUE_TIME | BIGINT | Displays the maximum time for en queuing write I/O events. |
| MIN_WRITE_ENQUEUE_TIME | BIGINT | Displays the minimum time for enqueuing write I/O events. |
| SUM_WRITE_ENQUEUE_TIME | BIGINT | Displays the total time for enqueuing write I/O events. |
| AVG_WRITE_ENQUEUE_TIME | BIGINT | Displays the average time for enqueuing write I/O events. |
| LAST_READ_SIZE | BIGINT | Displays the last size of read data in bytes. |
| MAX_READ_SIZE | BIGINT | Displays the maximum size of read data in bytes. |
| MIN_READ_SIZE | BIGINT | Displays the minimum size of read data in bytes. |
| SUM_READ_SIZE | BIGINT | Displays the total size of read data in bytes. |
| AVG_READ_SIZE | BIGINT | Displays the average size of read data in bytes. |

| LAST_WRITE_SIZE | BIGINT |
| --- | --- |

Displays the last size of written data in bytes.

| MAX_WRITE_SIZE | BIGINT | Displays the maximum size of written data in bytes. |
| --- | --- | --- |
| MIN_WRITE_SIZE | BIGINT | Displays the minimum size of written data in bytes. |
| SUM_WRITE_SIZE | BIGINT | Displays the total size of written data in bytes. |
| AVG_WRITE_SIZE | BIGINT | Displays the average size of written data in bytes. |

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| LAST_READ_SYNC_SIZE | BIGINT | Displays the last size of synchronously read data in bytes. |
| MAX_READ_SYNC_SIZE | BIGINT | Displays the maximum size of synchronously read data in bytes. |
| MIN_READ_SYNC_SIZE | BIGINT | Displays the minimum size of synchronously read data in bytes. |
| SUM_READ_SYNC_SIZE | BIGINT | Displays the total size of synchronously read data size. |
| AVG_READ_SYNC_SIZE | BIGINT | Displays the average size of synchronously read data in bytes. |
| LAST_WRITE_SYNC_SIZE | BIGINT | Displays the last size of synchronously written data in bytes. |
| MAX_WRITE_SYNC_SIZE | BIGINT | Displays the maximum size of synchronously written data in bytes. |
| MIN_WRITE_SYNC_SIZE | BIGINT | Displays the minimum size of synchronously written data in bytes. |
| SUM_WRITE_SYNC_SIZE | BIGINT | Displays the total size of synchronously written data in bytes. |
| AVG_WRITE_SYNC_SIZE | BIGINT | Displays the average size of synchronously written data in bytes. |

## Additional Information

This view has a resettable counterpart; you can see the values since the last reset in the M_VOLUME_IO_PERFORMANCE_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_VOLUME_IO_PERFORMANCE_STATISTICS_RESET;`

Resetting this view implicitly resets M_VOLUME_IO_DETAILED_STATISTICS and M_VOLUME_IO_DETAILED/ RETRY_STATISTICS.

The following table shows the differences between M_VOLUME_IO_PERFORMANCE_STATISTICS and M_VOLUME_IO_DETAILED/RETRY_STATISTICS. Columns that are only valid in M_VOLUME_IO_DETAILED/ RETRY_STATISTICS are not shown.

| **M_VOLUME_IO_PERFORMANCE_STATISTICS** | **M_VOLUME_IO_DETAILED_STATISTICS** | **M_VOLUME_IO_RETRY_STATISTICS** | **Change** |
| --- | --- | --- | --- |
| HOST | HOST | HOST | none |
| PORT | PORT | PORT | none |
| VOLUME_ID | VOLUME_ID | VOLUME_ID | none |
| PATH | PATH | PATH | none |
| FILESYSTEM_TYPE | FILESYSTEM_TYPE | FILESYSTEM_TYPE | none |
| TYPE | TYPE | TYPE | none |
| MAX_IO_BUFFER | MAX_IO_BUFFER | MAX_IO_BUFFER | none |
| READ_SYNC | READ_COUNT + ACTIVE_READ_COUNT |   | derived |
| WRITE_SYNC | WRITE_COUNT + ACTIVE_WRITE_COUNT |   | derived |
| READ_REQUESTS | TRIGGER_ASYNC_READ_COUNT + ACTIVE_TRIGGER_ASYNC_READ_COUNT |   | derived |
| WRITE_REQUESTS | TRIGGER_ASYNC_WRITE_COUNT + ACTIVE_TRIGGER_ASYNC_WRITE_COUNT |   | derived |
| READ_COMPLETIONS | TRIGGER_ASYNC_READ_COUNT |   | renamed |
| FAILED_READS |   | FAILED_READS | none |
| WRITE_COMPLETIONS | TRIGGER_ASYNC_WRITE_COUNT |   | renamed |
| FAILED_WRITES |   | FAILED_WRITES | none |
| FULL_RETRY_READS |   | FULL_RETRY_READS | none |
| FULL_RETRY_WRITES |   | FULL_RETRY_WRITES | none |
| SHORT_READS |   | SHORT_READS | none |
| SHORT_WRITES |   | SHORT_WRITES | none |
| DELAYED_READ_REQUESTS |   |   | removed |
| DELAYED_WRITE_REQUESTS |   |   | removed |
| DEQUEUED_DELAYED_REQUESTS |   |   | removed |
| RESUBMITTED_DELAYED_REQUESTS |   |   | removed |
| RESUBMITTED_DELAYED_REQUESTS_DELAYED_AGAIN |   |   | removed |
| ITEMS_IN_DELAY_QUEUE |   |   | removed |
| MAX_ITEMS_IN_DELAY_QUEUE |   |   | removed |
| LAST_READ_SYNC_TIME |   |   | removed |
| MAX_READ_SYNC_TIME | MAX_READ_TIME |   | renamed |
| MIN_READ_SYNC_TIME | MIN_READ_TIME |   | renamed |
| SUM_READ_SYNC_TIME |   |   | removed |
| AVG_READ_SYNC_TIME | AVG_READ_TIME |   | renamed |
| LAST_WRITE_SYNC_TIME |   |   | removed |
| MAX_WRITE_SYNC_TIME | MAX_WRITE_TIME |   | renamed |
| MIN_WRITE_SYNC_TIME | MIN_WRITE_TIME |   | renamed |
| SUM_WRITE_SYNC_TIME |   |   | removed |
| AVG_WRITE_SYNC_TIME | AVG_WRITE_TIME |   | renamed |
| LAST_READ_TIME |   |   | removed |
| MAX_READ_TIME | MAX_READ_TIME |   | none |
| MIN_READ_TIME | MIN_READ_TIME |   | none |
| SUM_READ_TIME |   |   | removed |
| AVG_READ_TIME | AVG_READ_TIME |   | renamed |
| LAST_WRITE_TIME |   |   | removed |
| MAX_WRITE_TIME | MAX_WRITE_TIME |   | none |
| MIN_WRITE_TIME | MIN_WRITE_TIME |   | none |
| SUM_WRITE_TIME |   |   | removed |
| AVG_WRITE_TIME | AVG_WRITE_TIME |   | none |
| LAST_READ_ENQUEUE_TIME |   |   | removed |
| MAX_READ_ENQUEUE_TIME |   |   | removed |
| MIN_READ_ENQUEUE_TIME |   |   | removed |
| SUM_READ_ENQUEUE_TIME |   |   | removed |
| AVG_READ_ENQUEUE_TIME |   |   | removed |
| LAST_WRITE_ENQUEUE_TIME |   |   | removed |
| MAX_WRITE_ENQUEUE_TIME |   |   | removed |
| MIN_WRITE_ENQUEUE_TIME |   |   | removed |
| SUM_WRITE_ENQUEUE_TIME |   |   | removed |
| AVG_WRITE_ENQUEUE_TIME |   |   | removed |
| LAST_READ_SIZE |   |   | removed |
| MAX_READ_SIZE | MAX_READ_SIZE |   | none |
| MIN_READ_SIZE | MIN_READ_SIZE |   | none |
| SUM_READ_SIZE |   |   | removed |
| AVG_READ_SIZE | AVG_READ_SIZE |   | none |
| LAST_WRITE_SIZE |   |   | removed |
| MAX_WRITE_SIZE | MAX_WRITE_SIZE |   | none |
| MIN_WRITE_SIZE | MIN_WRITE_SIZE |   | none |
| SUM_WRITE_SIZE |   |   | removed |
| AVG_WRITE_SIZE | AVG_WRITE_SIZE |   | none |
| LAST_READ_SYNC_SIZE |   |   | removed |
| MAX_READ_SYNC_SIZE | MAX_READ_SIZE |   | renamed |
| MIN_READ_SYNC_SIZE | MIN_READ_SIZE |   | renamed |
| SUM_READ_SYNC_SIZE |   |   | removed |
| AVG_READ_SYNC_SIZE | AVG_READ_SIZE |   | renamed |
| LAST_WRITE_SYNC_SIZE |   |   | removed |
| MAX_WRITE_SYNC_SIZE | MAX_WRITE_SIZE |   | renamed |
| MIN_WRITE_SYNC_SIZE | MIN_WRITE_SIZE |   | renamed |
| SUM_WRITE_SYNC_SIZE |   |   | removed |
| AVG_WRITE_SYNC_SIZE | AVG_WRITE_SIZE |   | renamed |

## Related Information

ALTER SYSTEM RESET MONITORING VIEW Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RESET-MONITORING-VIEW-Statement-System.md) M_VOLUME_IO_PERFORMANCE_STATISTICS_RESET System View - Deprecated [→](M_VOLUME_IO_PERFORMANCE_STATISTICS_RESET-System-View.md) M_VOLUME_IO_DETAILED_STATISTICS System View [→](M_VOLUME_IO_DETAILED_STATISTICS-System-View.md) M_VOLUME_IO_TOTAL_STATISTICS System View [→](M_VOLUME_IO_TOTAL_STATISTICS-System-View.md)
