# 6.2.206 M_PERSISTENT_MEMORY_VOLUME_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1932–1934

Reports the statistics of physical lifecycle events of blocks managed by SAP HANA services on the persistent memory volumes.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays an ID for the persistence volume. |
| NUMA_NODE_INDEX | SMALLINT | Displays the logical NUMA node index as in the M_NUMA_NODES view. |
| TOTAL_ACTIVE_COUNT | BIGINT | Displays the total number of active blocks from persistent memory volume. This counter is computed as a sum of loaded or created blocks but excludes deleted blocks. |
| TOTAL_ACTIVE_SIZE | BIGINT | Displays the total size, in bytes, of active blocks from persistent memory volume. This counter is computed as a sum of loaded or created blocks but excludes deleted blocks. |
| TOTAL_CREATE_COUNT | BIGINT | Displays the total number of newly created (that is, temporary) blocks from the persistent memory volume. |
| TOTAL_CREATE_SIZE | BIGINT | Displays the total size, in bytes, of the newly created temporary blocks from the persistent memory volume. |
| TOTAL_COMMIT_COUNT | BIGINT | Displays the total number of the permanently persisted blocks from the persistent memory volume. |
| TOTAL_COMMIT_SIZE | BIGINT | Displays the total size, in bytes, of the permanently persisted blocks from the persistent memory volume. |
| TOTAL_DELETE_COUNT | BIGINT | Displays the total number of deleted blocks from the persistent memory volume. |
| TOTAL_DELETE_SIZE | BIGINT | Displays the total size, in bytes, of the deleted blocks from the persistent memory volume. |
| TOTAL_DESTROY_COUNT | BIGINT | Displays the total number of destroyed blocks (no refcount) from the persistent memory volume. |
| TOTAL_DESTROY_SIZE | BIGINT | Displays the total size, in bytes, of the destroyed blocks (no refcount) from the persistent memory volume. |
| TOTAL_LOAD_COUNT | BIGINT | Displays the total number of loaded/ initialized blocks from the persistent memory volume upon service restart. |
| TOTAL_LOAD_SIZE | BIGINT | Displays the total size, in bytes, of loaded/initialized blocks from the persistent memory volume upon service restart. |
| TOTAL_MAPPED_COUNT | BIGINT | Displays the total number of blocks mapped into virtual memory from the persistent memory volume. |
| TOTAL_MAPPED_SIZE | BIGINT | Displays the total size, in bytes, of blocks mapped into virtual memory from the persistent memory volume. |

## Related Information

M_PERSISTENT_MEMORY_VOLUME_DATA_FILES System View [→](M_PERSISTENT_MEMORY_VOLUME_DATA_FILES-System-View.md) M_PERSISTENT_MEMORY_VOLUMES System View [→](M_PERSISTENT_MEMORY_VOLUMES-System-View.md) M_PERSISTENT_MEMORY_VOLUME_STATISTICS_RESET System View [→](M_PERSISTENT_MEMORY_VOLUME_STATISTICS_RESET-System-View.md) ALTER SYSTEM PERSISTENCE ENCRYPTION Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-PERSISTENCE-ENCRYPTION-Statement-System.md) UNLOAD Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/UNLOAD-Statement-Data-Manipulation.md) M_CATALOG_MEMORY System View [→](M_CATALOG_MEMORY-System-View.md)
