# 6.2.57 M_CS_COLUMNS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1713–1717

Provides runtime information about columns in column tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| PART_ID | INTEGER | Returns the table partition ID:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• For replicated tables, the part ID is 1 for the original table and subsequent part IDs are assigned to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• The part ID -1 indicates that the table schema is being modified. |
| MEMORY_SIZE_IN_TOTAL | BIGINT | Displays the sum, in bytes, of the memory used. |
| MEMORY_SIZE_IN_MAIN | BIGINT | Displays the current memory consumption, in bytes, in main. Returns 0 if the memory is not loaded in main. |
| MEMORY_SIZE_IN_DELTA | BIGINT | Displays the current memory consumption, in bytes, in delta. Returns 0 if the memory is not loaded in delta. |
| MEMORY_SIZE_IN_PAGE_LOADABLE_MAIN | BIGINT | Displays the total paged memory size of the column in bytes. |
| PERSISTENT_MEMORY_SIZE_IN_TOTAL | BIGINT | For columns stored in persistent memory, displays the total memory size in bytes. |
| UNCOMPRESSED_SIZE | BIGINT | Displays the estimated column size, in bytes, if the column is not compressed. |
| COMPRESSION_RATIO_IN_PERCENTAGE | DOUBLE | Displays the compression ratio percent age. This value is determined by dividing the MEMORY_SIZE_IN_TOTAL by the UNCOMPRESSED_SIZE and multiplying the result by 100. |
| COUNT | BIGINT | Displays the record count. This value is -1 if the count is not loaded. |
| DISTINCT_COUNT | BIGINT | Displays a distinct count of values, generally. This value is 0 if the count is not loaded.<br>The values in this column are not equal to actual values that might be returned by a SELECT DISTINCT query. Do not use these values in a production system if precision is required. |
| COMPRESSION_TYPE | VARCHAR(16) | Displays the type of column compression:<br>• SPARSE<br>• PREFIXED<br>• CLUSTERED<br>• INDIRECT<br>• RLE<br>• DEFAULT (if the column is only dictionary coded) |
| INDEX_TYPE | VARCHAR(16) | Displays the type of inverted index:<br>**FULL**<br>Displays that a conventional index is defined on the column. **BLOCK**<br>Displays that a block index is defined on the column. **MINMAX**<br>Displays that a min-max index is defined on the column. **NONE**<br>Displays that no index is defined on the column. |
| INDEX_LOADED | VARCHAR(16) | Displays the load status of the inverted index: NOT APPLICABLE, UNLOADED, or LOADED. |
| IMPLEMENTATION_FLAGS | BIGINT | Displays the internal implementation specification summary of the column. |
| LAST_ACCESS_TIME | TIMESTAMP | Displays the last time that the column was read or there was an INSERT to, UPDATE of, or DELETE from the column. This value is undefined for un loaded columns. |
| LOADED | VARCHAR(5) | Indicates whether the column is loaded into the memory: TRUE/FALSE. |
| LOADED_FROM_PERSISTENT_MEMORY | VARCHAR(5) | Displays whether the column was loaded from persistent memory: TRUE/ FALSE. |
| STORED_IN_PERSISTENT_MEMORY | VARCHAR(5) | Displays whether there is an associated persistent memory block: TRUE/ FALSE. |
| LOAD_UNIT | VARCHAR(7) | Displays the load unit for the column: PAGE, COLUMN, and UNKNOWN. |
| LAST_LOAD_TIME | TIMESTAMP | Displays the last time that the column was loaded. This is undefined for un loaded columns. |
| PERSISTENT_MEMORY | VARCHAR(5) | Displays the persistent memory preference inferred from the userspecified preferences in a bottom-up manner starting from this object: TRUE/FALSE. |
| NUMA_NODE_INDEX | SMALLINT | Displays the NUMA node index where allocations are performed and columns are loaded. |
| PERSISTENT_MEMORY_FILE_NAME | VARCHAR(256) | Displays the name of the persistent memory file associated with the column. If there is no associated persistent memory file, then NULL is re turned. |

## Additional Information

The information returned in the view is valid only for loaded columns (LOADED = TRUE).

## Related Information

M_CS_ALL_COLUMNS System View [→](M_CS_ALL_COLUMNS-System-View.md) CS_ALL_COLUMNS System View [→](../6.01-System-Views/CS_ALL_COLUMNS-System-View.md) CS_CONCAT_COLUMNS System View [→](../6.01-System-Views/CS_CONCAT_COLUMNS-System-View.md) CS_VIEW_COLUMNS System View [→](../6.01-System-Views/CS_VIEW_COLUMNS-System-View.md) RENAME COLUMN Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RENAME-COLUMN-Statement-Data-Definition.md)
