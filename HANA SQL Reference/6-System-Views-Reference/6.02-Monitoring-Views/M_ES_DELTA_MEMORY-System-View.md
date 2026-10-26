# 6.2.99 M_ES_DELTA_MEMORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1775–1776

Provides extended storage DELTA memory information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| FRAGMENT_COUNT | INTEGER | Displays the number of store fragments for the table. |
| TOTAL_SIZE | INTEGER | Displays the total DELTA memory used, in megabytes, by this table. |
| DATA_SIZE | INTEGER | Displays the total DELTA memory used, in megabytes, to store the table data. |
| DICTIONARY_SIZE | INTEGER | Displays the total DELTA memory used, in megabytes, to store the dictionaries for this table. |
| BITMAP_SIZE | INTEGER | Displays the DELTA memory used, in megabytes, to store the table-level bit maps. |
| RIDSPACE_INDEX | BIGINT | Displays the size of the RID space index in megabytes. |
| TRANSACTION_ID | BIGINT | Displays the associated transaction ID. |

## Related Information

M_ES_DELTA_MERGE_STATISTICS System View [→](M_ES_DELTA_MERGE_STATISTICS-System-View.md) M_ES_DELTA_MEMORY System View [Dynamic Tiering] [→](../../7-System-Views-Additional-Contexts/7.01-Dynamic-Tiering/7.01.04-M_ES_DELTA_MEMORY-System-View-Dynamic-Tiering.md)
