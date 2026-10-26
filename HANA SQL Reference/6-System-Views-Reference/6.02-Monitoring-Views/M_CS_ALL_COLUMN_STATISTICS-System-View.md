# 6.2.56 M_CS_ALL_COLUMN_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1712–1713

Provides information on how many scans and index searches were performed on any specified columns.

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| PART_ID | INTEGER | Returns the table partition ID:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• For replicated tables, the part ID is 1 for the original table and subsequent part IDs are assigned to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is currently in progress. |
| SCANNED_RECORD_COUNT | BIGINT | Displays the number of scanned rows on the main part of a specified column. The value is reset when the column is unloaded or merged. |
| INDEX_LOOKUP_COUNT | BIGINT | Displays the number of index lookups performed on the main part of a speci fied column. The value is reset when the column is unloaded or merged. |

## Related Information

M_CS_ALL_COLUMNS System View [→](M_CS_ALL_COLUMNS-System-View.md) CS_ALL_COLUMNS System View [→](../6.01-System-Views/CS_ALL_COLUMNS-System-View.md) CS_CONCAT_COLUMNS System View [→](../6.01-System-Views/CS_CONCAT_COLUMNS-System-View.md) CS_VIEW_COLUMNS System View [→](../6.01-System-Views/CS_VIEW_COLUMNS-System-View.md) RENAME COLUMN Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RENAME-COLUMN-Statement-Data-Definition.md)
