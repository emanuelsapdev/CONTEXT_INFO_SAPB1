# 6.2.166 M_LOG_PARTITIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1881–1885

Provides log partition statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| PARTITION_ID | BIGINT | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| PATH | VARCHAR(512) | Displays the log partition root path. |
| LAST_BUFFER_PREPARE_SIZE | BIGINT | Displays the size in bytes of the last log buffer at prepare time (actual log data size). |
| MAX_BUFFER_PREPARE_SIZE | BIGINT | Displays the size of the largest log buffer in bytes at prepare time (actual log data size). |
| MIN_BUFFER_PREPARE_SIZE | BIGINT | Displays the size in bytes of the small est log buffer at prepare time (actual log data size). |
| SUM_BUFFER_PREPARE_SIZE | BIGINT | Displays the total size in bytes of the log buffer at prepare time (actual log data size). |
| AVG_BUFFER_PREPARE_SIZE | BIGINT | Displays the average size in bytes of the log buffer at prepare time (actual log data size). |
| LAST_BUFFER_OVERHEAD_SIZE | BIGINT | Displays the size in bytes of the last log buffer alignment overhead at I/O time. |
| MAX_BUFFER_OVERHEAD_SIZE | BIGINT | Displays the largest size in bytes of the log buffer alignment overhead at I/O time. |
| MIN_BUFFER_OVERHEAD_SIZE | BIGINT | Displays the smallest size in bytes of the log buffer alignment overhead at I/O time. |
| SUM_BUFFER_OVERHEAD_SIZE | BIGINT | Displays the total size in bytes of the log buffer alignment overhead at I/O time (total). |
| AVG_BUFFER_OVERHEAD_SIZE | BIGINT | Displays the average size in bytes of the log buffer alignment overhead at I/O time. |
| LAST_BUFFER_IO_SIZE | BIGINT | Displays the size in bytes of the last log buffer at I/O time (actual data plus alignment overhead). |
| MAX_BUFFER_IO_SIZE | BIGINT | Displays the largest size in bytes of the log buffer at I/O time (actual data plus alignment overhead). |
| MIN_BUFFER_IO_SIZE | BIGINT | Displays the smallest size in bytes of the log buffer at I/O time (actual data plus alignment overhead). |
| SUM_BUFFER_IO_SIZE | BIGINT | Displays the total size in bytes of log buffer at I/O time (actual data plus alignment overhead). |
| AVG_BUFFER_IO_SIZE | BIGINT | Displays the average size in bytes of log buffer at I/O time (actual data plus alignment overhead). |
| LAST_GROUP_COMMIT_FREQUENCY | BIGINT | Displays the count of the last group commit frequency (callback count per buffer with sync callback). |
| MAX_GROUP_COMMIT_FREQUENCY | BIGINT | Displays the count of the largest group commit frequency (callback count per buffer with sync callback). |
| MIN_GROUP_COMMIT_FREQUENCY | BIGINT | Displays the count of the smallest group commit frequency (callback count per buffer with sync callback). |
| SUM_GROUP_COMMIT_FREQUENCY | BIGINT | Displays the total count of the group commit frequency (callback count per buffer with sync callback). |
| AVG_GROUP_COMMIT_FREQUENCY | BIGINT | Displays the average count of the group commit frequency (callback count per buffer with sync callback). |
| LAST_CALLBACK_TIME | BIGINT | Displays the last callback time per buffer with sync callback in microseconds. |
| MAX_CALLBACK_TIME | BIGINT | Displays the longest callback time per buffer with sync callback in microseconds. |
| MIN_CALLBACK_TIME | BIGINT | Displays the shortest callback time per buffer with sync callback in microseconds. |
| SUM_CALLBACK_TIME | BIGINT | Displays the total callback time per buffer with sync callback in microseconds. |
| AVG_CALLBACK_TIME | BIGINT | Displays the average callback time per buffer with sync callback in microseconds. |
| PREPARED_BUFFERS | BIGINT | Displays the number of buffers prepared for I/O. |
| WRITTEN_BUFFERS | BIGINT | Displays the number of completed and written buffers. |
| WRITTEN_BUFFERS_OOO | BIGINT | Displays the number of buffers written out-of-order. |
| NEW_SEGMENT_REQUEST_COUNT | BIGINT | Displays the number of of new log segment requests. |
| FREE_SEGMENTS | BIGINT | Displays the number of log segments currently free. |
| IN_BACKUP_SEGMENTS | BIGINT | Displays the number of current in-backup log segments. |
| IN_BACKUP_TRUNCATED_SEGMENTS | BIGINT | Displays the number of current in-backup truncated log segments. |
| BACKED_UP_SEGMENTS | BIGINT | Displays the number of log segments backed up so far. |
| TOTAL_SEGMENTS | BIGINT | Displays the total number of log segment count in the partition. |
| RECOVERY_SEGMENTS_IN_LOAD | BIGINT | Displays the number of in-load segments during recovery. |
| RECOVERY_SEGMENTS_WAITING_FOR_LOAD | BIGINT | Displays the number of segments waiting for load during recovery. |
| RECOVERY_SEGMENTS_IN_PROCESS | BIGINT | Displays the number of segments in process during recovery. |
| RECOVERY_SEGMENTS_PROCESSED | BIGINT | Count of segments processed during recovery. |
| COMMIT_COUNT | BIGINT | Displays the number of commits. |
| LAST_COMMIT_IO_LATENCY | BIGINT | Displays the last time in microseconds needed to synchronize the flush of commit log. |
| MAX_COMMIT_IO_LATENCY | BIGINT | Displays the longest time in microseconds needed to synchronize the flush of commit log entries. |
| MIN_COMMIT_IO_LATENCY | BIGINT | Displays the shortest time in microseconds needed in synchronize the flush of commit log entries. |
| SUM_COMMIT_IO_LATENCY | BIGINT | Displays the total time in microseconds needed to synchronize the flush of commit log entries. |
| AVG_COMMIT_IO_LATENCY | BIGINT | Displays the average time in microseconds needed to synchronize the flush of commit log entries. |

## Additional Information

This view collects various performance statistics for each log partition. The collected statistics can be used to optimize workload.

This view has a resettable counterpart; you can see the values since the last reset in the M_LOG_PARTITIONS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_LOG_PARTITIONS_RESET;`.

## Related Information

M_LOG_PARTITIONS_RESET System View [→](M_LOG_PARTITIONS_RESET-System-View.md) M_LOG_BUFFERS System View [→](M_LOG_BUFFERS-System-View.md) M_LOG_SEGMENTS System View [→](M_LOG_SEGMENTS-System-View.md) M_VOLUME_IO_TOTAL_STATISTICS System View [→](M_VOLUME_IO_TOTAL_STATISTICS-System-View.md)
