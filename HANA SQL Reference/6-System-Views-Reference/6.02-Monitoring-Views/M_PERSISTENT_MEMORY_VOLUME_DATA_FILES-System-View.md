# 6.2.205 M_PERSISTENT_MEMORY_VOLUME_DATA_FILES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1931–1932

Reports metadata statistics about files created by SAP HANA services for data storage on the persistent memory volumes.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays an ID for the persistence volume. |
| NUMA_NODE_INDEX | SMALLINT | Displays the logical NUMA node index as in the M_NUMA_NODES view. |
| FILE_NAME | VARCHAR(256) | Displays the file name of data block file located on persistent memory volume on Numa node of host (for example, `000000fe0000018a-00000051- 000001c2-00000001_159.file` `block`). |
| IS_MAPPED | VARCHAR(5) | Indicates whether the data block file is memory mapped into virtual address space: TRUE or FALSE. |
| SIZE | BIGINT | Displays the size of the data block file in bytes. |

## Related Information

M_PERSISTENT_MEMORY_VOLUMES System View [→](M_PERSISTENT_MEMORY_VOLUMES-System-View.md) M_PERSISTENT_MEMORY_VOLUME_STATISTICS System View [→](M_PERSISTENT_MEMORY_VOLUME_STATISTICS-System-View.md) M_PERSISTENT_MEMORY_VOLUME_STATISTICS_RESET System View [→](M_PERSISTENT_MEMORY_VOLUME_STATISTICS_RESET-System-View.md) ALTER SYSTEM PERSISTENCE ENCRYPTION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-PERSISTENCE-ENCRYPTION-Statement-System.md) UNLOAD Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/UNLOAD-Statement-Data-Manipulation.md) M_CATALOG_MEMORY System View [→](M_CATALOG_MEMORY-System-View.md)
