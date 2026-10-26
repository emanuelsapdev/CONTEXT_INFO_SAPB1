# 6.2.345 M_VOLUME_IO_DETAILED_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2124–2127

Provides detailed statistics about file access.

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
| MAX_IO_BUFFER_SIZE | BIGINT | Displays the maximum I/O buffer size in bytes. |
| APPEND_COUNT | BIGINT | Displays the number of appends. |
| ACTIVE_APPEND_COUNT | BIGINT | Displays the number of active appends. |
| MIN_APPEND_SIZE | BIGINT | Displays the minimum size of the appended data in bytes. |
| AVG_APPEND_SIZE | BIGINT | Displays the average size of the appended data in bytes. |
| MAX_APPEND_SIZE | BIGINT | Displays the maximum size of the appended data in bytes. |
| SUM_APPEND_SIZE | BIGINT | Displays the total size of the appended data in bytes. |
| MIN_APPEND_TIME | BIGINT | Displays the minimum time for appends. |
| AVG_APPEND_TIME | BIGINT | Displays the average time for appends. |
| MAX_APPEND_TIME | BIGINT | Displays the maximum time for appends. |
| SUM_APPEND_TIME | BIGINT | Displays the total size of the appended data. |
| WRITE_COUNT | BIGINT | Displays the number of writes. |
| ACTIVE_WRITE_COUNT | BIGINT | Displays the number of active writes. |
| MIN_WRITE_SIZE | BIGINT | Displays the minimum size of the written data in bytes. |
| AVG_WRITE_SIZE | BIGINT | Displays the average size of the written data in bytes. |
| MAX_WRITE_SIZE | BIGINT | Displays the maximum size of the written data in bytes. |
| SUM_WRITE_SIZE | BIGINT | Displays the total size of written data. |
| MIN_WRITE_TIME | BIGINT | Displays the minimum time for writes. |
| AVG_WRITE_TIME | BIGINT | Displays the average time for writes. |
| MAX_WRITE_TIME | BIGINT | Displays the maximum time for writes. |
| SUM_WRITE_TIME | BIGINT | Displays the total time for writes. |
| TRIGGER_ASYNC_WRITE_COUNT | BIGINT | Displays the number of trigger asynchronous writes. |
| ACTIVE_TRIGGER_ASYNC_WRITE_COUNT | BIGINT | Displays the number of active trigger asynchronous writes. |
| MIN_TRIGGER_ASYNC_WRITE_SIZE | BIGINT | Displays the minimum size of the trigger asynchronous write data in bytes. |
| AVG_TRIGGER_ASYNC_WRITE_SIZE | BIGINT | Displays the average size of the trigger asynchronous write data in bytes. |
| MAX_TRIGGER_ASYNC_WRITE_SIZE | BIGINT | Displays the maximum size of the trigger asynchronous write data in bytes. |
| SUM_TRIGGER_ASYNC_WRITE_SIZE | BIGINT | Displays the total size of the trigger asynchronous write data in bytes. |
| MIN_TRIGGER_ASYNC_WRITE_TIME | BIGINT | Displays the minimum time for trigger asynchronous writes. |
| AVG_TRIGGER_ASYNC_WRITE_TIME | BIGINT | Displays the average time for trigger asynchronous writes. |
| MAX_TRIGGER_ASYNC_WRITE_TIME | BIGINT | Displays the maximum time for trigger asynchronous writes. |
| SUM_TRIGGER_ASYNC_WRITE_TIME | BIGINT | Displays the total time for trigger asynchronous writes. |
| READ_COUNT | BIGINT | Displays the number of reads. |
| ACTIVE_READ_COUNT | BIGINT | Displays the number of active reads. |
| MIN_READ_SIZE | BIGINT | Displays the minimum size of the read data in bytes. |
| AVG_READ_SIZE | BIGINT | Displays the average size of the read data in bytes. |
| MAX_READ_SIZE | BIGINT | Displays the maximum size of the read data in bytes. |
| SUM_READ_SIZE | BIGINT | Displays the total size of the read data in bytes. |
| MIN_READ_TIME | BIGINT | Displays the minimum time for reads. |
| AVG_READ_TIME | BIGINT | Displays the average time for reads. |
| MAX_READ_TIME | BIGINT | Displays the maximum time for reads. |
| SUM_READ_TIME | BIGINT | Displays the total time for reads. |
| TRIGGER_ASYNC_READ_COUNT | BIGINT | Displays the number of trigger asynchronous reads. |
| ACTIVE_TRIGGER_ASYNC_READ_COUNT | BIGINT | Displays the number of active trigger asynchronous reads. |
| MIN_TRIGGER_ASYNC_READ_SIZE | BIGINT | Displays the minimum size of the trigger asynchronous read data. |
| AVG_TRIGGER_ASYNC_READ_SIZE | BIGINT | Displays the average size of the trigger asynchronous read data. |
| MAX_TRIGGER_ASYNC_READ_SIZE | BIGINT | Displays the maximum size of the trigger asynchronous read data. |
| SUM_TRIGGER_ASYNC_READ_SIZE | BIGINT | Displays the total size of the trigger asynchronous read data. |
| MIN_TRIGGER_ASYNC_READ_TIME | BIGINT | Displays the minimum time for trigger asynchronous reads. |
| AVG_TRIGGER_ASYNC_READ_TIME | BIGINT | Displays the average time for trigger asynchronous reads. |
| MAX_TRIGGER_ASYNC_READ_TIME | BIGINT | Displays the maximum time for trigger asynchronous reads. |
| SUM_TRIGGER_ASYNC_READ_TIME | BIGINT | Displays the total time for trigger asynchronous reads. |

## Additional Information

This view shows detailed I/O statistics for various buffer sizes. Each buffer size is a maximum value. That is, a buffer of the size 4k actually means <= 4k and a buffer size o f16k means 4k < buffer size <= 16k. The I/O time is the total time from starting a request until it finishes, including enqueue time. All measured times are periods of time between enqueueing and finishing a request. The reported times contain wait times if the request cannot be started immediately. Enqueue time is measured separately to see how many requests are executed asynchronously and how many are synchronous or blocking. For overall I/O performance, see TOTAL_READ/ WRITE_SIZE and TOTAL_IO_TIME in the M_VOLUME_IO_TOTAL_STATISTICS system view.

This view has a resettable counterpart; you can see the values since the last reset in the M_VOLUME_IO_DETAILED_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_VOLUME_IO_DETAILED_STATISTICS_RESET;`

## Related Information

M_VOLUME_IO_DETAILED_STATISTICS_RESET System View [→](M_VOLUME_IO_DETAILED_STATISTICS_RESET-System-View.md) M_VOLUME_IO_TOTAL_STATISTICS System View [→](M_VOLUME_IO_TOTAL_STATISTICS-System-View.md)
