# 6.2.351 M_VOLUME_IO_STATISTICS System View - Deprecated

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2140–2144

Deprecated. Use M_VOLUME_IO_TOTAL_STATISTICS instead.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| PATH | VARCHAR(512) | Displays the file system path. |
| FILESYSTEM_TYPE | VARCHAR(32) | Displays the file system type. |
| TYPE | VARCHAR(16) | Displays the type of contained files. |
| CONFIGURATION | VARCHAR(128) | Displays the configuration parameters. |
| OPEN_CALL_COUNT | BIGINT | Displays the number of open calls. |
| CLOSE_CALL_COUNT | BIGINT | Displays the number of close calls. |
| EXISTS_CALL_COUNT | BIGINT | Displays the number of exists calls. |
| REMOVE_CALL_COUNT | BIGINT | Displays the number of remove calls. |
| RESIZE_CALL_COUNT | BIGINT | Displays the number of resize calls. |
| SYNC_CALL_COUNT | BIGINT | Displays the number of sync calls. |
| GETSIZE_CALL_COUNT | BIGINT | Displays the number of get size calls. |
| GETMODIFICATIONTIME_CALL_COUNT | BIGINT | Displays the number of get modification time calls. |
| GETDEVICEID_CALL_COUNT | BIGINT | Displays the number of get DeviceID calls. |
| ENQUEUED_WRITE_REQUESTS | BIGINT | Deprecated. |
| BLOCKED_WRITE_REQUESTS | BIGINT | Displays the number of blocked write requests. |
| MAX_BLOCKED_WRITE_REQUESTS | BIGINT | Displays the maximum number of blocked write requests. |
| EOF_READS | BIGINT | Displays the number of EOF reads. |
| TOTAL_SYNC_READS | BIGINT | Displays the number of synchronous reads. |
| TOTAL_ASYNC_READS | BIGINT | Displays the number of asynchronous reads with waiting. |
| TOTAL_TRIGGER_ASYNC_READS | BIGINT | Displays the number of triggered asynchronous reads. |
| TRIGGER_ASYNC_READ_RATIO | DOUBLE | Displays the trigger-ratio of asynchronous reads. |
| TOTAL_SHORT_READS | BIGINT | Displays the number of reads that read less bytes than requested. |
| TOTAL_FULL_RETRY_READS | BIGINT | Displays the number of full retry reads. |
| TOTAL_FAILED_READS | BIGINT | Displays the number of failed reads. |
| TOTAL_READ_SIZE | BIGINT | Displays the size of read data in bytes. |
| TOTAL_READ_TIME | BIGINT | Displays the total read time. |
| TOTAL_APPENDS | BIGINT | Displays the number of appends. |
| TOTAL_SYNC_WRITES | BIGINT | Displays the number of synchronous writes. |
| TOTAL_ASYNC_WRITES | BIGINT | Displays the number of asynchronous writes with waiting. |
| TOTAL_TRIGGER_ASYNC_WRITES | BIGINT | Displays the number of triggered asynchronous writes. |
| TRIGGER_ASYNC_WRITE_RATIO | DOUBLE | Displays the trigger-ratio of asynchronous writes. |
| TOTAL_SHORT_WRITES | BIGINT | Displays the number of writes that wrote less bytes than requested. |
| TOTAL_FULL_RETRY_WRITES | BIGINT | Displays the number of full retry writes. |
| TOTAL_FAILED_WRITES | BIGINT | Displays the number of failed writes. |
| TOTAL_WRITE_SIZE | BIGINT | Displays the amount of written data in bytes. |
| TOTAL_WRITE_TIME | BIGINT | Displays the total write time. |
| TOTAL_IO_TIME | BIGINT | Displays the total I/O time. |

## Additional Information

This view shows information about basic I/O operations on I/O subsystems (paths).

TOTAL_READ/WRITE _SIZE is aggregated from M_VOLUME_IO_PERFORMANCE_STATISTICS. The column TOTAL_IO_TIME is only an approximation of real I/O times and should not be used to compute exact throughput ratios.

Refer to the M_VOLUME_IO_PERFORMANCE_STATISTICS system view for detailed information about read/ write performance on various buffer sizes.

The following table shows the differences between M_VOLUME_IO_STATISTICS and M_VOLUME_IO_TOTAL_STATISTICS. Columns that are only valid in M_VOLUME_IO_TOTAL_STATISTICS are not shown.

| **M_VOLUME_IO_STATISTICS** | **M_VOLUME_IO_TOTAL_STATISTICS** | **Change** |
| --- | --- | --- |
| HOST | HOST | None |
| PORT | PORT | None |
| PATH | PATH | None |
| FILESYSTEM_TYPE | FILESYSTEM_TYPE | None |
| TYPE | TYPE | None |
| CONFIGURATION | CONFIGURATION | None |
| OPEN_CALL_COUNT |   | Removed |
| CLOSE_CALL_COUNT |   | Removed |
| EXISTS_CALL_COUNT |   | Removed |
| REMOVE_CALL_COUNT |   | Removed |
| RESIZE_CALL_COUNT |   | Removed |
| SYNC_CALL_COUNT |   | Removed |
| GETSIZE_CALL_COUNT |   | Removed |
| GETMODIFICATIONTIME_CALL_COUNT |   | Removed |
| GETDEVICEID_CALL_COUNT |   | Removed |
| ENQUEUED_WRITE_REQUESTS |   | Removed |
| BLOCKED_WRITE_REQUESTS | BLOCKED_WRITE_REQUESTS | None |
| MAX_BLOCKED_WRITE_REQUESTS | MAX_BLOCKED_WRITE_REQUESTS | None |
| EOF_READS |   | Removed |
| TOTAL_SYNC_READS | TOTAL_READS | Renamed |
| TOTAL_ASYNC_READS |   | Removed |
| TOTAL_TRIGGER_ASYNC_READS | TOTAL_TRIGGER_ASYNC_READS | None |
| TRIGGER_ASYNC_READ_RATIO | TRIGGER_READ_RATIO | Renamed |
| TOTAL_SHORT_READS | TOTAL_SHORT_READS | None |
| TOTAL_FULL_RETRY_READS | TOTAL_FULL_RETRY_READS | None |
| TOTAL_FAILED_READS | TOTAL_FAILED_READS | None |
| TOTAL_READ_SIZE | TOTAL_READ_SIZE | None |
| TOTAL_READ_TIME | TOTAL_READ_TIME | None |
| TOTAL_APPENDS | TOTAL_APPENDS | None |
| TOTAL_SYNC_WRITES | TOTAL_WRITES | Renamed |
| TOTAL_ASYNC_WRITES |   | Removed |
| TOTAL_TRIGGER_ASYNC_WRITES | TOTAL_TRIGGER_ASYNC_WRITES | None |
| TRIGGER_ASYNC_WRITE_RATIO | TRIGGER_WRITE_RATIO | Renamed |
| TOTAL_SHORT_WRITES | TOTAL_SHORT_WRITES | None |
| TOTAL_FULL_RETRY_WRITES | TOTAL_FULL_RETRY_WRITES | None |
| TOTAL_FAILED_WRITES | TOTAL_FAILED_WRITES | None |
| TOTAL_WRITE_SIZE | TOTAL_WRITE_SIZE | None |
| TOTAL_WRITE_TIME | TOTAL_WRITE_TIME | None |
| TOTAL_IO_TIME | TOTAL_IO_TIME | None |

This view has a resettable counterpart; you can see the values since the last reset in the M_VOLUME_IO_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_VOLUME_IO_STATISTICS_RESET;`.

Resetting this view implicitly resets the dependent child views M_VOLUME_IO_DETAILED_STATISTICS and M_VOLUME_IO_RETRY_STATISTICS.

## Related Information

ALTER SYSTEM RESET MONITORING VIEW Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RESET-MONITORING-VIEW-Statement-System.md) M_VOLUME_IO_STATISTICS_RESET System View - Deprecated [→](M_VOLUME_IO_STATISTICS_RESET-System-View-Deprecated.md) M_VOLUME_IO_DETAILED_STATISTICS System View [→](M_VOLUME_IO_DETAILED_STATISTICS-System-View.md) M_VOLUME_IO_TOTAL_STATISTICS System View [→](M_VOLUME_IO_TOTAL_STATISTICS-System-View.md) M_VOLUME_IO_STATISTICS System View - Deprecated [→](M_VOLUME_IO_STATISTICS-System-View-Deprecated.md)
