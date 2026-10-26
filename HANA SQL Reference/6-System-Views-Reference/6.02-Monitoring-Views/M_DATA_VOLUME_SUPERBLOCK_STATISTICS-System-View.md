# 6.2.82 M_DATA_VOLUME_SUPERBLOCK_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1752–1753

Provides FreeBlockManager Superblock statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| PARTITION_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| DATA_VOLUME_NAME | VARCHAR(512) | Displays the data volume name. |
| STATE | VARCHAR(16) | Displays the data volume state: ACTI VATING, ACTIVE, or DEACTIVATING. |
| SUPERBLOCK_SIZE | BIGINT | Displays the superblock size in bytes. |
| USED_SUPERBLOCK_COUNT | BIGINT | Displays the number of used superblocks. |
| SUPERBLOCK_COUNT | BIGINT | Displays the number of superblocks. |
| FILL_RATIO | DOUBLE | Displays the fill ratio. |

## Additional Information

This view shows information about the number and distribution of superblocks inside data volumes:

- SUPERBLOCK_COUNT is the total number of superblocks.
- USED_SUPERBLOCK_COUNT is the number of superblocks currently occupied by at least one used or shadow page.
- FILL_RATIO specifies the ratio of the number of used superblocks versus the total number of superblocks. The fill ratio of the superblocks themselves is not part of this formula.

## Related Information

M_DATA_VOLUME_PAGE_STATISTICS System View [→](M_DATA_VOLUME_PAGE_STATISTICS-System-View.md) M_DATA_STATISTICS System View [→](M_DATA_STATISTICS-System-View.md) M_DATA_VOLUMES System View [→](M_DATA_VOLUMES-System-View.md) M_DATA_VOLUME_PARTITION_STATISTICS System View [→](M_DATA_VOLUME_PARTITION_STATISTICS-System-View.md)
