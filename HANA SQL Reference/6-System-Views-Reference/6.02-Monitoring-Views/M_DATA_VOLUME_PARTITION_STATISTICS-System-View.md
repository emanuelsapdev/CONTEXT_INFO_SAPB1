# 6.2.80 M_DATA_VOLUME_PARTITION_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1749–1751

Provides data volume partition statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| PARTITION_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| FILE_NAME_PATTERN | VARCHAR(512) | Displays the file name pattern for the data volume partition file. |
| STATE | VARCHAR(16) | Displays the data volume state. This can be specified as ACTIVATING or AC TIVE. When a data volume partition is added, it is in the ACTIVATING state and is not usable until the next save point, at which time it enters the AC TIVE state. |
| MAX_FILE_SIZE | BIGINT | Displays the maximum file size for the data volume files in bytes. A value of 0 means that there is no limitation for the file size. |
| USED_SIZE | BIGINT | Displays the used size of the data volume partition in bytes. |
| TOTAL_SIZE | BIGINT | Displays the total size of the data volume partition in bytes. |
| FILES_SIZE | INTEGER | Displays the size of the data volume files on the disk in bytes. |
| FILL_RATIO | DOUBLE | Displays the fill ratio of the data volume partition. |

## Related Information

ALTER SYSTEM ALTER DATAVOLUME ADD PARTITION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ALTER-DATAVOLUME-ADD-PARTITION-Statement.md) ALTER SYSTEM ALTER DATAVOLUME DROP PARTITION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ALTER-DATAVOLUME-DROP-PARTITION-Statement.md) M_DATA_VOLUME_PAGE_STATISTICS_RESET System View [→](M_DATA_VOLUME_PAGE_STATISTICS_RESET-System-View.md) M_DATA_VOLUMES System View [→](M_DATA_VOLUMES-System-View.md) M_DATA_VOLUME_STATISTICS System View [→](M_DATA_VOLUME_STATISTICS-System-View.md) M_DATA_VOLUME_SUPERBLOCK_STATISTICS System View [→](M_DATA_VOLUME_SUPERBLOCK_STATISTICS-System-View.md)
