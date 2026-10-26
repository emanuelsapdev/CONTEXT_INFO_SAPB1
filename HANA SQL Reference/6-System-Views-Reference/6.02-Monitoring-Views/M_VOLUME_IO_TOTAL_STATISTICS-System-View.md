# 6.2.353 M_VOLUME_IO_TOTAL_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2145–2147

Shows information about basic I/O operations on I/O subsystems (paths).

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| PATH | VARCHAR(512) | Displays the file system path. |
| FILESYSTEM_TYPE | VARCHAR(32) | Displays the file system type. |
| TYPE | VARCHAR(16) | Displays the type of contained files. |
| CONFIGURATION | VARCHAR(256) | Displays the configuration parameters. |
| BLOCKED_WRITE_REQUESTS | BIGINT | Displays the number of blocked write requests. |

| MAX_BLOCKED_WRITE_REQUESTS | BIGINT |
| --- | --- |

Displays the maximum number of blocked write requests.

| TOTAL_READS | BIGINT | Displays the number of synchronous reads. |
| --- | --- | --- |
| TOTAL_TRIGGER_ASYNC_READS | BIGINT | Displays the number of triggered asynchronous reads. |
| ACTIVE_ASYNC_READS_COUNT | BIGINT | Displays the number of active asynchronous reads |
| TRIGGER_READ_RATIO | DOUBLE | Displays the trigger-ratio of asynchronous reads. |
| TOTAL_SHORT_READS | BIGINT | Displays the number of reads that read fewer bytes than requested. |
| TOTAL_FULL_RETRY_READS | BIGINT | Displays the number of full retry reads. |
| TOTAL_FAILED_READS | BIGINT | Displays the number of failed reads. |
| TOTAL_READ_SIZE | BIGINT | Displays the size of read data in bytes. |

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| TOTAL_READ_TIME | BIGINT | Displays the total read time in microseconds. |
| TOTAL_APPENDS | BIGINT | Displays the number of appends. |
| TOTAL_WRITES | BIGINT | Displays the number of synchronous writes. |
| TOTAL_TRIGGER_ASYNC_WRITES | BIGINT | Displays the number of triggered asynchronous writes. |
| ACTIVE_ASYNC_WRITES_COUNT | BIGINT | Displays the number of active asynchronous writes |
| TRIGGER_WRITE_RATIO | DOUBLE | Displays the trigger-ratio of asynchronous writes. |
| TOTAL_SHORT_WRITES | BIGINT | Displays the number of writes that wrote less bytes than requested. |
| TOTAL_FULL_RETRY_WRITES | BIGINT | Displays the number of full retry writes. |
| TOTAL_FAILED_WRITES | BIGINT | Displays the number of failed writes. |
| TOTAL_WRITE_SIZE | BIGINT | Displays the size of written data in bytes. |
| TOTAL_WRITE_TIME | BIGINT | Displays the total write time in microseconds. |
| TOTAL_IO_TIME | BIGINT | Displays the total IO time in microseconds. |

## Additional Information

Throughput of file I/O can generally be calculated by (TOTAL_READ_SIZE + TOTAL_WRITE_SIZE) / TOTAL_IO_TIME.

For TOTAL_IO_TIME, note that reads and writes can happen in parallel. For example, assume there is a 20 MB read operation and, in parallel, a 20 MB write operation. The read operation starts at 0.0 sec, the write operation starts at 0.5 sec, and both operations last exactly 2 seconds. TOTAL_IO_TIME is calculated as:

```sql
TOTAL_READ_SIZE  = 20,971,520 Bytes
TOTAL_WRITE_SIZE = 20,971,520 Bytes
TOTAL_READ_TIME  =  2,000,000 Microsecond (timeframe: 0.0 – 2.0 sec)
TOTAL_WRITE_TIME =  2,000,000 Microsecond (timeframe: 0.5 – 2.5 sec)
TOTAL_IO_TIME    =  2,500,000 Microsecond (timeframe: 0.0 – 2.5 sec)
```

Refer to the M_VOLUME_IO_DETAILED_STATISTICS and M_VOLUME_IO_RETRY_STATISTICS system views for detailed information about read/write performance on various buffer sizes.

This view has a resettable counterpart; you can see the values since the last reset in the M_VOLUME_IO_TOTAL_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_VOLUME_IO_TOTAL_STATISTICS_RESET;`.

Resetting this view implicitly resets the dependent child views M_VOLUME_IO_DETAILED_STATISTICS and M_VOLUME_IO_RETRY_STATISTICS.

## Related Information

M_VOLUME_IO_DETAILED_STATISTICS System View [→](M_VOLUME_IO_DETAILED_STATISTICS-System-View.md) M_VOLUME_IO_RETRY_STATISTICS System View [→](M_VOLUME_IO_RETRY_STATISTICS-System-View.md) M_VOLUME_IO_DETAILED_STATISTICS System View [→](M_VOLUME_IO_DETAILED_STATISTICS-System-View.md)
