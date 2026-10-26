# 6.2.106 M_ES_TABLES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1784–1786

Provides extended storage table information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name for the table. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| PART_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| IS_DELTA_ENABLED | VARCHAR(5) | Indicates whether the table is an RLV table or not: TRUE/FALSE. |
| TABLE_SIZE | BIGINT | Displays the size of the compressed data in bytes. |
| RECORD_COUNT | BIGINT | Displays the record count in the extended table. |
| LAST_MODIFIED_TIME | TIMESTAMP | Displays the timestamp when the table was last modified. |

## Related Information

CREATE TABLE Statement (Extended Store Table) [Dynamic Tiering] [→](../../5-Additional-SAP-HANA-Contexts/5.02-Dynamic-Tiering/CREATE-TABLE-Statement-Extended-Store-Table-Dynamic-Tiering.md) ALTER TABLE Statement (Extended Store Table) [Dynamic Tiering] [→](../../5-Additional-SAP-HANA-Contexts/5.02-Dynamic-Tiering/ALTER-TABLE-Statement-Extended-Store-Table-Dynamic-Tiering.md)
