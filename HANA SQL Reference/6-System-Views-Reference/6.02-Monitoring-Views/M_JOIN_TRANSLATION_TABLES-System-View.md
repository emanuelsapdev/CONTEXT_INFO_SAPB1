# 6.2.142 M_JOIN_TRANSLATION_TABLES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1839–1841

Provides column store join engine translation tables statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME1 | NVARCHAR(256) | Displays the first schema name. |
| TABLE_NAME1 | NVARCHAR(256) | Displays the first table name. |
| COLUMN_NAME1 | NVARCHAR(256) | Displays the first table's column name. |
| PART_ID1 | INTEGER | Displays the first table partition ID. Re turns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| VERSION1 | BIGINT | Displays the version information of the first table. |
| SCHEMA_NAME2 | NVARCHAR(256) | Displays the second schema name. |
| TABLE_NAME2 | NVARCHAR(256) | Displays the second table name. |
| COLUMN_NAME2 | NVARCHAR(256) | Displays the second table's column name. |
| PART_ID2 | INTEGER | Displays the second table partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| VERSION2 | BIGINT | Displays the version information of the second table. |
| IMPLEMENTATION_TYPE | NVARCHAR(8) | Displays the implementation type. |
| IMPLEMENTATION_TYPE_CHANGE_TIME | TIMESTAMP | Displays the last time that the implementation type was changed. |
| IMPLEMENTATION_TYPE_CHANGE_COUNT | INTEGER | Displays the number of implementation type changes. |
| VALUE_ID_COUNT1 | BIGINT | Displays the number of translated value IDs of the first table. |
| VALUE_ID_COUNT2 | BIGINT | Displays the number of translated value IDs of the second table. |
| TRANSLATION_TABLE_MEMORY_SIZE | BIGINT | Displays the memory used by the translation table in bytes. |
| ESTIMATED_HASHMAP_MEMORY_SIZE | BIGINT | Displays the estimated memory used by the HASHMAP implementation in bytes. |
| ESTIMATED_VECTOR_MEMORY_SIZE | BIGINT | Displays the estimated memory used by the vector implementation in bytes. |
| LAST_USED_COUNT | BIGINT | Displays the counter to support LRU cache replacement algorithm. |

## Related Information

[M_JOINENGINE_STATISTICS System View](M_JOINENGINE_STATISTICS-System-View.md)

[M_JOIN_DATA_STATISTICS System View](M_JOIN_DATA_STATISTICS-System-View.md)
