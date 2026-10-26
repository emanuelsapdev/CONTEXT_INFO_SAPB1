# 6.2.204 M_PERSISTENT_MEMORY_VOLUMES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1930–1931

Reports the capacity, usage and metadata of persistent memory volumes.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays an ID for the persistence volume. |
| NUMA_NODE_INDEX | SMALLINT | Displays the logical NUMA node index as in the M_NUMA_NODES view. |
| PATH | VARCHAR(512) | Displays the absolute directory base path of persistent memory volume configured for NUMA node |
| FILESYSTEM_TYPE | VARCHAR(32) | Displays the filesystem type, for example, ext3, ext4, xfs. |
| IS_DIRECT_ACCESS_SUPPORTED | VARCHAR(5) | Displays whether Direct Access semantics are supported by the volume. |
| TOTAL_SIZE | BIGINT | Displays the total physical memory size, in bytes, of the persistent memory volume. |
| USED_SIZE | BIGINT | Displays the used physical memory size, in bytes, of persistent memory volume. |

## Related Information

M_PERSISTENT_MEMORY_VOLUME_DATA_FILES System View [→](M_PERSISTENT_MEMORY_VOLUME_DATA_FILES-System-View.md) M_PERSISTENT_MEMORY_VOLUME_STATISTICS System View [→](M_PERSISTENT_MEMORY_VOLUME_STATISTICS-System-View.md) M_PERSISTENT_MEMORY_VOLUME_STATISTICS_RESET System View [→](M_PERSISTENT_MEMORY_VOLUME_STATISTICS_RESET-System-View.md) ALTER SYSTEM PERSISTENCE ENCRYPTION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-PERSISTENCE-ENCRYPTION-Statement-System.md) UNLOAD Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/UNLOAD-Statement-Data-Manipulation.md) M_CATALOG_MEMORY System View [→](M_CATALOG_MEMORY-System-View.md)
