# 6.2.81 M_DATA_VOLUME_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1751–1752

Provides information on data volume statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| PARTITION_COUNT | INTEGER | Displays the number of partitions. |
| PATH_COUNT | INTEGER | Displays the number of partition paths. |
| USED_SIZE | BIGINT | Displays the used size of the data volume in bytes. |
| TOTAL_SIZE | BIGINT | Displays the total size of the data volume in bytes. |
| FILL_RATIO | DOUBLE | Displays the fill ratio of the data volume. |

## Related Information

M_DATA_STATISTICS System View [→](M_DATA_STATISTICS-System-View.md) M_DATA_VOLUMES System View [→](M_DATA_VOLUMES-System-View.md) M_DATA_VOLUME_PAGE_STATISTICS System View [→](M_DATA_VOLUME_PAGE_STATISTICS-System-View.md) M_DATA_VOLUME_PARTITION_STATISTICS System View [→](M_DATA_VOLUME_PARTITION_STATISTICS-System-View.md) M_DATA_VOLUME_SUPERBLOCK_STATISTICS System View [→](M_DATA_VOLUME_SUPERBLOCK_STATISTICS-System-View.md) ALTER SYSTEM ALTER DATAVOLUME ADD PARTITION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ALTER-DATAVOLUME-ADD-PARTITION-Statement.md) ALTER SYSTEM ALTER DATAVOLUME DROP PARTITION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ALTER-DATAVOLUME-DROP-PARTITION-Statement.md) ALTER SYSTEM RECLAIM DATAVOLUME Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RECLAIM-DATAVOLUME-Statement-System-Management.md) M_VOLUME_SIZES System View [→](M_VOLUME_SIZES-System-View.md)
