# 6.2.64 M_CS_MVCC System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1724–1727

Provides column store MVCC information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the port number. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| PART_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| IS_HISTORY | VARCHAR(5) | Indicates if the partition is a history partition: TRUE/FALSE. |
| LOADED | VARCHAR(5) | Indicates if the MVCC data is loaded into the memory. |
| FRAGMENT_TYPE | VARCHAR(7) | Displays the fragment type: DELTA1, DELTA2, or MAIN. |
| RECORD_COUNT | BIGINT | Displays the number of visible records in the table. |
| RAW_RECORD_COUNT | BIGINT | Displays the number of physical records in the table. |
| ROWSTATE_BLOCK_COUNT | BIGINT | Displays the number of active rowstate blocks. |
| CTS_BLOCK_COUNT | BIGINT | Displays the number of blocks used to store creation timestamps (CTS). |
| DTS_BLOCK_COUNT | BIGINT | Displays the number of blocks used to store deletion timestamps (DTS). |
| ROWSTATE_STUB_BLOCK_COUNT | BIGINT | Displays the total number of stub blocks, both visible and invisible, present in the MVCC layer associated with the fragment. |
| VISIBLE_ROWSTATE_STUB_BLOCK_COUNT | BIGINT | Displays the number of visible stub blocks present in the MVCC layer associated with the fragment. |
| CTS_STUB_BLOCK_COUNT | BIGINT | Displays the number of active CTS stub blocks. |
| DTS_STUB_BLOCK_COUNT | BIGINT | Displays the number of active DTS stub blocks. |
| FREE_ROWSTATE_BLOCK_COUNT | BIGINT | Displays the number of free row-state blocks available for successive operations. |
| FREE_TS_BLOCK_COUNT | BIGINT | Displays the number of free CTS/DTS blocks. |
| FREE_TS_STUB_BLOCK_COUNT | BIGINT | Displays the number of free CTS/DTS stub blocks. |
| PAGE_COUNT | BIGINT | Displays the number of pages in the MVCC page chain. |
| MEMORY_SIZE_IN_TOTAL | BIGINT | If MVCC data is loaded, then it displays the total memory size of MVCC structures in bytes. |
| PAGE_CHAIN_MEMORY_SIZE | BIGINT | If MVCC data is loaded, then it displays the memory size of the pinned MVCC page chain in bytes. |
| PAGE_CHAIN_ACTIVE_MEMORY_SIZE | BIGINT | Displays the memory size of the active part of the MVCC page chain in bytes. |
| ROWSTATE_MEMORY_SIZE | BIGINT | If MVCC data is loaded, then it displays the memory size of transient rowstate structures in bytes. |
| CTS_MEMORY_SIZE | BIGINT | Displays the amount of memory used to store CTS blocks in bytes. |
| DTS_MEMORY_SIZE | BIGINT | Displays the amount of memory used to store DTS blocks in bytes. |
| MISC_MEMORY_SIZE | BIGINT | If MVCC data is loaded, then it displays the memory size of miscellaneous MVCC related structures in bytes. |
| SPARSE_DTS_BLOCK_COUNT | INTEGER | Displays the number of DTS blocks that are sparse timestamp blocks. |
| SPARSE_DTS_MEMORY_SIZE | INTEGER | Displays the memory size of the sparse block in bytes. |
| FREE_SPARSE_TS_BLOCK_COUNT | INTEGER | Displays the number of available sparse timestamp blocks for successive operations. |

## Related Information

CURRENT_MVCC_SNAPSHOT_TIMESTAMP Function (Datetime) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CURRENT_MVCC_SNAPSHOT_TIMESTAMP-Function-Datetime.md) M_MVCC_SNAPSHOTS System View [→](M_MVCC_SNAPSHOTS-System-View.md) M_MVCC_OVERVIEW System View [→](M_MVCC_OVERVIEW-System-View.md) M_MVCC_TABLES System View [→](M_MVCC_TABLES-System-View.md)
