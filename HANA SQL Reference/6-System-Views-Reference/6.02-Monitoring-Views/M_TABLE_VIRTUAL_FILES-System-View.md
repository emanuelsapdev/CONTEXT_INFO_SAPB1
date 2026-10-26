# 6.2.321 M_TABLE_VIRTUAL_FILES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2095–2096

Provides information about all virtual files that belong to a table.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| PART_ID | INTEGER | Displays the table partition ID:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that the table schema is currently in being modified. |
| IS_HISTORY | VARCHAR(5) | Displays whether history is part of a table: TRUE/FALSE. |
| CONTAINER_ID | BIGINT | Displays the container ID. |
| NAMESPACE | VARCHAR(512) | Displays the namespace address in the database storage system. |
| NAME | VARCHAR(512) | Displays the name in the database storage system. |
| PHYSICAL_SIZE | BIGINT | Displays the storage size used for the file in bytes. |
| PAGE_COUNT | BIGINT | Displays the number of storage pages used for the file. |

## Related Information

M_TABLES System View [→](M_TABLES-System-View.md) M_TABLE_LOB_FILES System View [→](M_TABLE_LOB_FILES-System-View.md)
