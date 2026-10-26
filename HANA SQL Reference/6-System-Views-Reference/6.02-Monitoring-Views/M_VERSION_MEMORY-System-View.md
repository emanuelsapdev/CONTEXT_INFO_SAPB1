# 6.2.342 M_VERSION_MEMORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2121–2122

Provides information about memory use of the row-store Multiversion Concurrency Control (MVCC) manager.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| ALLOCATED_MEMORY_SIZE | BIGINT | Displays the size of memory allocated for row-store version space in bytes. |
| USED_MEMORY_SIZE | BIGINT | Displays the size of memory actually used by row-store versions in bytes. |
| RECLAIMED_VERSION_SIZE | BIGINT | Displays the size of memory reclaimed by row-store version garbage collection in bytes. |
| FREE_MEMORY_SIZE | BIGINT | Displays the size of memory freed and reusable in row-store version space in bytes. |

## Related Information

M_SYSTEM_REPLICATION_MVCC_HISTORY System View [→](M_SYSTEM_REPLICATION_MVCC_HISTORY-System-View.md) CURRENT_MVCC_SNAPSHOT_TIMESTAMP Function (Datetime) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_MVCC_SNAPSHOT_TIMESTAMP-Function-Datetime.md) M_CS_MVCC System View [→](M_CS_MVCC-System-View.md)

M_MVCC_SNAPSHOTS System View [→](M_MVCC_SNAPSHOTS-System-View.md) M_MVCC_OVERVIEW System View [→](M_MVCC_OVERVIEW-System-View.md) M_MVCC_TABLES System View [→](M_MVCC_TABLES-System-View.md)
