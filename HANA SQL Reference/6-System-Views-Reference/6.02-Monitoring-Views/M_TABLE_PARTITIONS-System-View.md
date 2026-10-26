# 6.2.308 M_TABLE_PARTITIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2078–2081

Provides information regarding partitionspecific memory and disk usage for partitioned tables.

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| NODE_ID | INTEGER | Displays the ID of the partition node. |
| PARENT_NODE_ID | INTEGER | Displays the ID of the parent node. |
| PART_ID | INTEGER | Displays the table partition ID:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• For replicated tables, the part ID is 1 for the original table and subsequent part IDs are assigned to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is currently in progress. |
| LOAD_UNIT | VARCHAR(7) | Displays the effective load unit. Valid values are PAGE (when the partition uses page loadable storage) and COL UMN (when the partition uses column loadable storage). |
| STORAGE_TYPE | VARCHAR(8) | Displays DEFAULT when a column storage type is used. Displays EXTENDED when an extended storage type is used. |
| MEMORY_SIZE_IN_TOTAL | BIGINT | Displays the total memory size in bytes, which is the sum of the memory in the main, delta, and history parts. |
| MEMORY_SIZE_IN_MAIN | BIGINT | Displays the current memory consumption in main in bytes. This value varies depending on the number of loaded attributes and includes data for open transactions. |
| MEMORY_SIZE_IN_PAGE_LOADABLE | BIGINT | Displays the total resident paged memory size, in bytes, of the partition. |
| MEMORY_SIZE_IN_DELTA | BIGINT | Displays the current memory consumption in delta in bytes. |
| DISK_SIZE | BIGINT | Displays the total size of a table partition on a disk in bytes. Column storage displays the size on the disk per partition. Extended storage displays the size on the disk for all extended storage partitions. |
| DISK_SIZE_IN_PAGE_LOADABLE | BIGINT | Displays the total disk size, in bytes, of page-loadable storage for this partition. |
| ESTIMATED_MAX_MEMORY_SIZE_IN_TOTAL | BIGINT | Displays the total estimated maximum memory consumption in bytes for fully loaded partitions. This value does not include data for open transactions. |
| LAST_ESTIMATED_MEMORY_SIZE | BIGINT | Displays the last estimated memory consumption in bytes of a fully loaded partition. |
| LAST_ESTIMATED_MEMORY_SIZE_TIME | TIMESTAMP |   |
| RECORD_COUNT | BIGINT | Displays the record count. |
| RAW_RECORD_COUNT_IN_MAIN | BIGINT | Displays the current number of entries in the main part. This value differs from the number of visible main rows be cause there are entries for modified rows that are marked as invalidated.Displays the last time that the last-estimated memory consumption was calculated. |
| RAW_RECORD_COUNT_IN_DELTA | BIGINT | Displays the current number of entries in the delta part. This value differs from the number of visible delta rows be cause there are additional entries, such as deleted rows or updated rows. This value can contain deleted records. |
| LOADED | VARCHAR(10) | Displays the last time that the last-estimated memory consumptionDisplays how many columns in the table are loaded in memory. Valuse are: NO, PAR TIALLY, or FULL. For a description of each column, see M_CS_COLUMNS. |
| IS_REPLICA | VARCHAR(5) | Displays whether the part is a replica (TRUE/FALSE). |
| GROUP_TYPE | NVARCHAR(256) | Displays the effective group type. |
| SUBTYPE | NVARCHAR(256) | Displays the effective group subtype. |
| GROUP_NAME | NVARCHAR(256) | Displays the effective group name. |

## Related Information

TABLE_PARTITIONS System View [→](../6.01-System-Views/TABLE_PARTITIONS-System-View.md) M_TABLE_PARTITION_STATISTICS System View [→](M_TABLE_PARTITION_STATISTICS-System-View.md) M_CS_COLUMNS System View [→](M_CS_COLUMNS-System-View.md) CREATE TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.68-CREATE-TABLE/README.md)
