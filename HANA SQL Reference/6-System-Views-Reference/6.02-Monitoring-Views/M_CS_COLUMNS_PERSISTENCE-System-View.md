# 6.2.58 M_CS_COLUMNS_PERSISTENCE System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1717–1718

Provides column persistence information for column tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| PART_ID | INTEGER | Returns the table partition ID:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• For replicated tables, the part ID is 1 for the original table and subsequent part IDs are assigned to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is currently in progress. |
| COLUMN_ID | INTEGER | Displays the numeric column ID. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| PERSISTENCE_TYPE | VARCHAR(16) | Displays the type of column persistence: SINGLE, PAGED, VIRTUAL_FILE, or VIRTUAL_PAGED. |
| MAIN_PHYSICAL_SIZE | BIGINT | Displays the storage size, in bytes, used by the column. |
| MAIN_PHYSICAL_SIZE_IN_PAGE_LOADABLE | BIGINT | Displays the total on-disk size stored in a page-loadable format for the table in bytes. |

## Related Information

M_CS_COLUMNS System View [→](M_CS_COLUMNS-System-View.md) M_CS_ALL_COLUMNS System View [→](M_CS_ALL_COLUMNS-System-View.md) M_CS_ALL_COLUMN_STATISTICS System View [→](M_CS_ALL_COLUMN_STATISTICS-System-View.md)
