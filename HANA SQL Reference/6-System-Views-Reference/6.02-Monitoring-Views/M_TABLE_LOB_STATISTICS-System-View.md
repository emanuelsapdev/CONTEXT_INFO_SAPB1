# 6.2.305 M_TABLE_LOB_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2074–2076

Provides information about the aggregated file and packed LOB statistics per host, port, table, partition, and column.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the name of the host. |
| PORT | INTEGER | Displays the internal port number. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name associated with the LOBs. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name associated with the LOBs. |
| PART_ID | INTEGER | Returns the table partition ID:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• For replicated tables, the part ID is 1 for the original table and subsequent part IDs are assigned to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is currently in progress. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name associated with the LOBs. |
| LOB_STORAGE_TYPE | VARCHAR(7) | Displays that the LOB storage type is one of the following:<br>**INPLACE**<br>Small LOBs (completely loaded into the main memory). **PACKED**<br>Medium-sized LOBs where the size is between two thresholds (only loaded into the main memory when required). **FILE**<br>Large LOBs (individually loaded into the main memory on demand). |
| CONTAINER_ID | BIGINT | Displays the container ID of the packed LOB container; NULL for file LOBs. |
| DISK_SIZE | BIGINT | Displays the number of bytes used for the LOBs on a disk. |
| BINARY_SIZE | BIGINT | Displays the binary size in bytes of the LOBs. This value may be less than the DISK_SIZE due to management information and paging. |
| CHARACTER_SIZE | BIGINT | Displays the number of characters in the NCLOBs (only) column. For packed LOBs, this corresponds to the total number of characters of all of the LOBs in the container. |
| LOB_COUNT | BIGINT | Displays the total number of associated LOBs. |
| READ_COUNT | BIGINT | Displays the counter for read operations on the LOBs. |
| MEMORY_SIZE | BIGINT | Displays the size in bytes of the LOB pages that are loaded in the memory. |
| MEMORY_PAGE_COUNT | BIGINT | Displays the number of LOB pages loaded in the memory. |

## Related Information

M_TABLE_LOB_FILES System View [→](M_TABLE_LOB_FILES-System-View.md) Large Object (LOB) Data Types [→](../../4-SQL-Reference/4.03-Data-Types/4.03.06-Large-Object-LOB-Data-Types.md)
