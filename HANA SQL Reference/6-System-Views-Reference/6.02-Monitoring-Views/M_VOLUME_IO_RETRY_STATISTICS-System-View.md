# 6.2.349 M_VOLUME_IO_RETRY_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2137–2139

Provides file access retry statistics.

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
| TOTAL_APPEND_COUNT | BIGINT | Displays the number of all appends. |
| FAILED_APPEND_COUNT | BIGINT | Displays the number of failed appends. |
| TOTAL_WRITE_COUNT | BIGINT | Displays the number of all writes. |
| FAILED_WRITE_COUNT | BIGINT | Displays the number of failed writes. |
| SHORT_WRITE_COUNT | BIGINT | Displays the number of short writes. |
| REQUESTS_WITH_SHORT_WRITES_COUNT | BIGINT | Displays the number of requests with short writes. |
| AVG_SHORT_WRITES_PER_REQUEST_COUNT | BIGINT | Displays the average number of short writes per request with short writes. |
| MAX_SHORT_WRITES_PER_REQUEST_COUNT | BIGINT | Displays the maximum number of short writes per request. |
| FULL_RETRY_WRITE_COUNT | BIGINT | Displays the number of full retry writes. |
| REQUESTS_WITH_FULL_RETRY_WRITES_COUNT | BIGINT | Displays the number of requests with full retry writes. |
| AVG_FULL_RETRY_WRITES_PER_REQUEST_COUNT | BIGINT | Displays the average number of full re try writes per request with full retry writes. |
| MAX_FULL_RETRY_WRITES_PER_REQUEST_COUNT | BIGINT | Displays the maximum number of full retry writes per request. |
| TOTAL_READ_COUNT | BIGINT | Displays the number of all reads. |
| FAILED_READ_COUNT | BIGINT | Displays the number of failed reads. |
| SHORT_READ_COUNT | BIGINT | Displays the number of short reads. |
| REQUESTS_WITH_SHORT_READS_COUNT | BIGINT | Displays the number of requests with short reads. |
| AVG_SHORT_READS_PER_REQUEST_COUNT | BIGINT | Displays the average number of short reads per request with short reads. |
| MAX_SHORT_READS_PER_REQUEST_COUNT | BIGINT | Displays the maximum number of short reads per request. |
| FULL_RETRY_READ_COUNT | BIGINT | Displays the number of full retry reads. |
| REQUESTS_WITH_FULL_RETRY_READS_COUNT | BIGINT | Displays the number of requests with full retry reads. |
| AVG_FULL_RETRY_READS_PER_REQUEST_COUNT | BIGINT | Displays the average number of full re try reads per request with full retry reads. |
| MAX_FULL_RETRY_READS_PER_REQUEST_COUNT | BIGINT | Displays the maximum number of full retry reads per request. |

## Additional Information

This view shows retry and error I/O statistics for various buffer sizes. Each buffer size is a maximum value, so a buffer size of 4k actually means <= 4k and a buffer size of 16k means 4k < buffer size <= 16k. For overall I/O performance, see `TOTAL_READ/WRITE_SIZE` and `TOTAL_IO_TIME` in the M_VOLUME_IO_TOTAL_STATISTICS system view.

This view has a resettable counterpart; you can see the values since the last reset in the M_VOLUME_IO_RETRY_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_VOLUME_IO_RETRY_STATISTICS_RESET;`

## Related Information

ALTER SYSTEM RESET MONITORING VIEW Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RESET-MONITORING-VIEW-Statement-System.md) M_VOLUME_IO_RETRY_STATISTICS_RESET System View [→](M_VOLUME_IO_RETRY_STATISTICS_RESET-System-View.md) M_VOLUME_IO_TOTAL_STATISTICS System View [→](M_VOLUME_IO_TOTAL_STATISTICS-System-View.md)
