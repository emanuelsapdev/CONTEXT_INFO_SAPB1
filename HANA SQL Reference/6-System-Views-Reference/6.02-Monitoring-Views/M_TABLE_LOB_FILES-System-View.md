# 6.2.304 M_TABLE_LOB_FILES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2073–2074

Provides information about all LOB files that belong to a table.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| PART_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| TABLE_OID | BIGINT | Displays the table OID, same as owner_oid if the table is found; 0 other wise. |
| CONTAINER_ID | BIGINT | Displays the container ID. |
| PHYSICAL_SIZE | BIGINT | Displays the file size in bytes. |
| BINARY_SIZE | BIGINT | Displays the LOB size in bytes. |
| CHARACTER_SIZE | INTEGER | Displays the number of characters in NCLOB. |
| PAGE_COUNT | BIGINT | Displays the number of pages used for a LOB file. |
| LOB_TYPE | VARCHAR(5) | Displays the type of LOB. |

## Related Information

M_TABLE_LOB_STATISTICS System View [→](M_TABLE_LOB_STATISTICS-System-View.md) Large Object (LOB) Data Types [→](../../4-SQL-Reference/4.03-Data-Types/4.03.06-Large-Object-LOB-Data-Types.md) ALTER TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.20-ALTER-TABLE/README.md)
