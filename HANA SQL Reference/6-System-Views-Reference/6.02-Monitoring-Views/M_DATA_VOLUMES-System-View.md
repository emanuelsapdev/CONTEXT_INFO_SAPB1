# 6.2.77 M_DATA_VOLUMES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1746–1747

Provides data volume statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| PARTITION_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| FILE_NAME | VARCHAR(512) | Displays the filename of the data volume. |
| FILE_ID | BIGINT | Displays the file ID of data volume. |
| STATE | VARCHAR(16) | Displays the data volume state: ACTI VATING, ACTIVE, or DEACTIVATING. |
| SIZE | BIGINT | Displays the size of the data volume in bytes. |
| MAX_SIZE | BIGINT | Displays the maximum size of the data volume in bytes. |

## Related Information

[M_DATA_VOLUME_PAGE_STATISTICS System View](M_DATA_VOLUME_PAGE_STATISTICS-System-View.md)

M_DATA_VOLUME_PAGE_STATISTICS_RESET System View [→](M_DATA_VOLUME_PAGE_STATISTICS_RESET-System-View.md) M_DATA_VOLUME_PARTITION_STATISTICS System View [→](M_DATA_VOLUME_PARTITION_STATISTICS-System-View.md) M_DATA_VOLUME_STATISTICS System View [→](M_DATA_VOLUME_STATISTICS-System-View.md) M_DATA_VOLUME_SUPERBLOCK_STATISTICS System View [→](M_DATA_VOLUME_SUPERBLOCK_STATISTICS-System-View.md) ALTER SYSTEM ALTER DATAVOLUME ADD PARTITION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ALTER-DATAVOLUME-ADD-PARTITION-Statement.md) ALTER SYSTEM ALTER DATAVOLUME DROP PARTITION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ALTER-DATAVOLUME-DROP-PARTITION-Statement.md) ALTER SYSTEM RECLAIM DATAVOLUME Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RECLAIM-DATAVOLUME-Statement-System-Management.md) M_VOLUME_SIZES System View [→](M_VOLUME_SIZES-System-View.md)
