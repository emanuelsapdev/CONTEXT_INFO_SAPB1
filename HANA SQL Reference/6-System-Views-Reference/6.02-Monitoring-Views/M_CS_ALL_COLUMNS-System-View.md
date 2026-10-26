# 6.2.55 M_CS_ALL_COLUMNS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1707–1712

Provides runtime information for all columns in column tables, including internal column tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| PART_ID | INTEGER | Returns the table partition ID:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• For replicated tables, the part ID is 1 for the original table, and subsequent part IDs are assigned to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• The part ID -1 indicates that the table schema is being modified. |
| MEMORY_SIZE_IN_TOTAL | BIGINT | Displays the sum of the MEMORY_SIZE_IN_MAIN and MEMORY_SIZE_IN_DELTA columns in bytes. |
| MEMORY_SIZE_IN_MAIN | BIGINT | Displays the current memory consumption in main in bytes. Returns 0 if the memory is not loaded in main. |
| MEMORY_SIZE_IN_DELTA | BIGINT | Displays the current memory consumption in delta in bytes. Returns 0 if the memory is not loaded in delta. |
| MEMORY_SIZE_IN_PAGE_LOADABLE_MAIN | BIGINT | Displays the total paged memory size of the column in bytes. |
| PERSISTENT_MEMORY_SIZE_IN_TOTAL | BIGINT | For columns stored in persistent memory, displays the total memory size in bytes. |
| UNCOMPRESSED_SIZE | BIGINT | Displays the estimated, uncompressed column size in bytes. |
| COMPRESSION_RATIO_IN_PERCENTAGE | DOUBLE | Displays the compression ratio percent age. This value is determined by dividing the MEMORY_SIZE_IN_TOTAL by the UNCOMPRESSED_SIZE and multiplying the result by 100. |
| COUNT | BIGINT | Displays the record count. Returns 0 if the count is not loaded. |
| DISTINCT_COUNT | BIGINT | Displays the distinct count of values. Returns 0 if the count is not loaded. |
| COMPRESSION_TYPE | VARCHAR(16) | Displays the type of column compression. This value can be: SPARSE, PRE FIXED, CLUSTERED, INDIRECT, RLE, or DEFAULT (if the column is only dictionary coded). The columns in the M_CS_COLUMNS system view show the runtime value, which can be changed during the runtime. |
| INDEX_TYPE | VARCHAR(16) | Displays the type of inverted index:<br>**FULL**<br>Displays that a FULL inverted index is defined on the column. A FULL index is a data structure that as signs a position to each value in the column. FULL indexes are the conventional form of index. **BLOCK**<br>Displays that a block index is defined on the column.<br>A BLOCK index is a data structure where each value in the column is assigned to one of a list of fixed size blocks for the column. BLOCK indexes are typically much smaller than FULL indexes. Reverse look-ups on BLOCK indexes are effec tively a combination of reading the index (fast) and scanning the read blocks (possibly slow, depending on the compression of the column). BLOCK indexes can be used with compressed columns. **MINMAX**<br>Displays that a min-max index is defined for the column. **NONE**<br>Displays that no index is defined for the column. |
| INDEX_LOADED | VARCHAR(16) | Displays the load status of the inverted index: NOT APPLICABLE, UNLOADED, or LOADED. |
| IMPLEMENTATION_FLAGS | BIGINT | Displays the column internal implementation specification summary. |
| LAST_ACCESS_TIME | TIMESTAMP | Displays the last time that the column was read or there was an INSERT to, UPDATE of, or DELETE from the column. This value is undefined for un loaded columns. |
| LOADED | VARCHAR(5) | Displays whether the flag to indicate that the column is loaded into memory (including DRAM or persistent memory): TRUE/FALSE. |
| LOADED_FROM_PERSISTENT_MEMORY | VARCHAR(5) | Displays whether the column was loaded from persistent memory: TRUE/ FALSE. |
| STORED_IN_PERSISTENT_MEMORY | VARCHAR(5) | Displays whether there is an associated persistent memory block: TRUE/ FALSE. |
| LOAD_UNIT | VARCHAR(7) | Displays the load unit for the columns: PAGE, COLUMN, and UNKNOWN. |
| TABLE_OID | BIGINT | Displays the object ID of the table. |
| MAIN_MEMORY_SIZE_IN_DATA | BIGINT | Displays the current memory consumption in the data in bytes. |
| MAIN_MEMORY_SIZE_IN_DICT | BIGINT | Displays the current memory consumption in the dictionary in bytes. |
| MAIN_MEMORY_SIZE_IN_INDEX | BIGINT | Displays the current memory consumption in the index in bytes. |
| MAIN_MEMORY_SIZE_IN_MISC | BIGINT | Displays the miscellaneous current memory consumption in bytes. |
| DELTA_MEMORY_SIZE_IN_DATA | BIGINT | Displays the current memory consumption in the data in bytes. |
| DELTA_MEMORY_SIZE_IN_DICT | BIGINT | Displays the current memory consumption in the dictionary in bytes. |
| DELTA_MEMORY_SIZE_IN_INDEX | BIGINT | Displays the current memory consumption in the index in bytes. |
| DELTA_MEMORY_SIZE_IN_MISC | BIGINT | Displays the miscellaneous current memory consumption in bytes. |
| MAIN_PAGE_LOADABLE_MEMORY_SIZE_IN_DATA | BIGINT | Displays the total paged memory size of the column index vector in bytes. |
| MAIN_PAGE_LOADABLE_MEMORY_SIZE_IN_DICT | BIGINT | Displays the total paged memory of the column dictionary in bytes. |
| MAIN_PAGE_LOADABLE_MEMORY_SIZE_IN_INDEX | BIGINT | Displays the total paged memory of the column's inverted index in bytes. |
| MAIN_PAGE_LOADABLE_MEMORY_SIZE_IN_MISC | BIGINT | Displays the total paged memory size of other column structures in bytes. |
| MAIN_PERSISTENT_MEMORY_SIZE_IN_DATA | BIGINT | For columns stored in persistent memory, displays the current memory consumption in the data in bytes. |
| MAIN_PERSISTENT_MEMORY_SIZE_IN_DICT | BIGINT | For columns stored in persistent memory, displays the current memory consumption in the dictionary in bytes. |
| MAIN_PERSISTENT_MEMORY_SIZE_IN_INDEX | BIGINT | For columns stored in persistent memory, displays the current memory consumption in the index in bytes. |
| MAIN_PERSISTENT_MEMORY_SIZE_IN_MISC | BIGINT | For columns stored in persistent memory, displays the current memory consumption not already accounted for in the other memory size columns in bytes. |
| MAIN_PERSISTENT_MEMORY_SIZE_UNUSED | BIGINT | Displays the amount of persistent memory, in bytes, that is not directly mapped to a corresponding data structure during load, but was only read to construct the data structure in DRAM. This column also includes persistent memory block overhead if the requested persistent memory allocation is not a multiple of a block size. |
| INDEX_CREATE_DURATION | BIGINT | Displays the time needed to create an inverted index. |
| DELTA_IMPLEMENTATION_FLAGS | BIGINT | Displays the internal column implementation specification summary. |
| INTERNAL_ATTRIBUTE_TYPE | VARCHAR(32) | Displays the attribute type for internal columns. Returns NULL for non-internal columns. |
| LAST_LOAD_TIME | TIMESTAMP | Displays the last time that the column was loaded. This value is undefined for unloaded columns. |
| PERSISTENT_MEMORY | VARCHAR(5) | Displays the persistent memory preference inferred from the userspecified preferences. |
| NUMA_NODE_INDEX | SMALLINT | Displays the NUMA node index where allocations are performed and columns are loaded. |
| PERSISTENT_MEMORY_FILE_NAME | VARCHAR(256) | Displays the name of the persistent memory file associated with the column. If there is no associated persistent memory file, then NULL is re turned. |

## Additional Information

The information returned in the view is valid only for loaded columns (LOADED = TRUE).

## Related Information

M_CS_ALL_COLUMN_STATISTICS System View [→](M_CS_ALL_COLUMN_STATISTICS-System-View.md) CS_ALL_COLUMNS System View [→](../6.01-System-Views/CS_ALL_COLUMNS-System-View.md) CS_CONCAT_COLUMNS System View [→](../6.01-System-Views/CS_CONCAT_COLUMNS-System-View.md) CS_VIEW_COLUMNS System View [→](../6.01-System-Views/CS_VIEW_COLUMNS-System-View.md) RENAME COLUMN Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RENAME-COLUMN-Statement-Data-Definition.md)
