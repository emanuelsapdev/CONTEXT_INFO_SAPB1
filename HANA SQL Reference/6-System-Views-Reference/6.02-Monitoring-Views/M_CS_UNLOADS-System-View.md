# 6.2.69 M_CS_UNLOADS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1734–1736

Provides a history of column unloads.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| UNLOAD_TIME | TIMESTAMP | Displays the timestamp of unload event. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. Empty if the whole table is unloaded. |
| PART_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| TABLE_OID | BIGINT | Displays the object ID of the table. |
| IS_HISTORY | VARCHAR(5) | Indicates whether the history part is un loaded (only relevant for history tables). Empty if the whole table is unloaded. |
| REASON | NVARCHAR(16) | Displays the possible reasons for the unload. Values are LOW MEMORY, SHRINK, EXPLICIT, MERGE, or UN USED RESOURCE. Unloads caused by a manual shrink are reported as SHRINK, whereas unloads caused by memory management's automatic shrink on out of memory (OOM) are reported as LOW MEMORY. |
| PERSISTENT_MEMORY | VARCHAR(6) | Displays whether persistent memory is removed as part of the unload. Values are RETAIN or DELETE. Empty if the user did not specify a value for the un load. |

## Related Information

[UNLOAD Statement (Data Manipulation)](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/UNLOAD-Statement-Data-Manipulation.md)
