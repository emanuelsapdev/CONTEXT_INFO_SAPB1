# 6.2.170 M_LOG_SEGMENTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1887–1889

Provides log segment statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| PARTITION_ID | BIGINT | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| SEGMENT_ID | BIGINT | Displays the log segment ID within the partition. |
| FILE_NAME | VARCHAR(512) | Displays the log segment file name. |
| FILE_OFFSET | BIGINT | Displays the start position of the log segment in the file. |
| STATE | VARCHAR(16) | Displays the log segment state:<br>**Formatting**<br>The log segment is being formatted and not yet used. **Preallocated**<br>The log segment has been preallo cated, but never used. **Writing**<br>The log segment is currently being written. **Closed**<br>The log segment is closed, not backed up and is still required for restart. **Truncated**<br>The log segment is not required for restart, but has not been backed up. **BackedUp**<br>The log segment has been backed up, but is still required for restart. **RetainedFree**<br>The log segment has been backed up and is not required for restart, but is required to resync the system replication sites. **Free**<br>The log segment has been backed up, it is not required for restart and can be reused. |
| MIN_POSITION | BIGINT | Displays the first position contained in the log segment. |
| MAX_POSITION | BIGINT | Displays the position behind the last log record in the log segment. This value is for closed log segments only. |
| HOLE_POSITION | BIGINT | Displays the start position of the log hole before the log segment. This value is equal to MIN_POSITION if there is no hole. |
| USED_SIZE | BIGINT | Displays the used log segment size in bytes. |
| TOTAL_SIZE | BIGINT | Displays the total log segment size in bytes. |
| IN_BACKUP | VARCHAR(5) | Indicates whether or not the flag for the log segment is in the backup: TRUE/ FALSE |
| LAST_COMMIT_TIME | TIMESTAMP | Displays the timestamp of the last commit in the log segment. |
| ENCRYPTION_KEY_HASH | VARCHAR(64) | Displays the hash of the key used for the log segment encryption. |

## Additional Information description

This view describes each allocated log segment and shows its current state and log position range that is currently contained in the segment.

This view has a resettable counterpart; you can see the values since the last reset in the M_LOG_SEGMENTS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_LOG_SEGMENTS_RESET;`.

## Related Information

M_LOG_SEGMENTS_RESET System View [→](M_LOG_SEGMENTS_RESET-System-View.md) M_LOG_BUFFERS System View [→](M_LOG_BUFFERS-System-View.md) M_LOG_PARTITIONS System View [→](M_LOG_PARTITIONS-System-View.md) M_VOLUME_IO_TOTAL_STATISTICS System View [→](M_VOLUME_IO_TOTAL_STATISTICS-System-View.md)
