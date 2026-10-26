# 6.2.78 M_DATA_VOLUME_PAGE_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1747–1749

Provides page usage statistics on data volumes.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| PARTITION_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| DATA_VOLUME_NAME | VARCHAR(512) | Displays the data volume name. |
| STATE | VARCHAR(16) | Displays the data volume state: ACTI VATING, ACTIVE, or DEACTIVATING. |
| PAGE_SIZECLASS | VARCHAR(16) | Displays the page size class. |
| PAGE_SIZE | BIGINT | Displays the page size in bytes. |
| SUPERBLOCK_SIZE | BIGINT | Displays the superblock size in bytes. |
| INITIAL_BLOCK_COUNT | BIGINT | Displays the number of init pages. |
| TOTAL_ALLOCATE_BLOCK_COUNT | BIGINT | Displays the number of single and group allocated blocks. |
| TOTAL_SET_BLOCK_FREE_COUNT | BIGINT | Displays the number of single and group freed blocks. |
| TOTAL_SET_BLOCK_FREE_AFTER_SAVEPOINT_COUNT | BIGINT | Displays the number of single and group freed-after-savepoint blocks. |
| SUPERBLOCK_COUNT | BIGINT | Displays the number of used superblocks. |
| USED_BLOCK_COUNT | BIGINT | Displays the number of used blocks. |
| SHADOW_BLOCK_COUNT | BIGINT | Displays the number of shadow blocks. |
| FILL_RATIO | DOUBLE | Displays the fill ratio. |

## Additional Information

This view contains information about the number and distribution of free, used, and shadow pages inside data volumes:

- INITIAL_BLOCK_COUNT is the number of pages the database was started with.
- TOTAL_\*_COUNT specifies the numbers of blocks allocated, freed or set to status FreeAfterSavepoint since the start of the database.
- SUPERBLOCK_COUNT, USED_BLOCK_COUNT, and SHADOW_BLOCK_COUNT columns contain the number of blocks or superblocks currently in use by the database.
- FILL_RATIO specifies the ratio of the minimum number of needed superblocks versus the actual number of used superblocks. Unused superblocks are not part of this formula.

This view has a resettable counterpart; you can see the values since the last reset in the M_DATA_VOLUME_PAGE_STATISTICS_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_DATA_VOLUME_PAGE_STATISTICS_RESET;`.

## Related Information

M_DATA_VOLUME_PAGE_STATISTICS_RESET System View [→](M_DATA_VOLUME_PAGE_STATISTICS_RESET-System-View.md) M_DATA_VOLUMES System View [→](M_DATA_VOLUMES-System-View.md)

M_DATA_VOLUME_PARTITION_STATISTICS System View [→](M_DATA_VOLUME_PARTITION_STATISTICS-System-View.md) M_DATA_VOLUME_STATISTICS System View [→](M_DATA_VOLUME_STATISTICS-System-View.md) M_DATA_VOLUME_SUPERBLOCK_STATISTICS System View [→](M_DATA_VOLUME_SUPERBLOCK_STATISTICS-System-View.md)
