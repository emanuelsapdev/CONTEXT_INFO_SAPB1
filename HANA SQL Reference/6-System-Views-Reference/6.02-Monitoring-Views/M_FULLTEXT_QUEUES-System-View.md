# 6.2.117 M_FULLTEXT_QUEUES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1803–1804

Provides fulltext index queue status.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| INDEX_OID | BIGINT | Displays the OID of the corresponding fulltext index. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema of the data table. |
| TABLE_NAME | NVARCHAR(256) | Displays the name of the data table. |
| PART_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| COLUMN_NAME | NVARCHAR(256) | Displays the name of the document column. |
| STATUS | NVARCHAR(16) | Displays the queue status: ACTIVE/ SUSPENDED. |
| TOTAL_DOCUMENT_COUNT | BIGINT | Displays the total number of documents in the original table. |
| INDEXED_DOCUMENT_COUNT | BIGINT | Displays the number of successfully indexed documents. |
| QUEUE_DOCUMENT_COUNT | BIGINT | Displays the number of documents currently in the queue. |
| ERROR_DOCUMENT_COUNT | BIGINT | Displays the number of failed documents. |

## Related Information

M_FULLTEXT_COLUMN_STATISTICS System View [→](M_FULLTEXT_COLUMN_STATISTICS-System-View.md) ALTER FULLTEXT INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-FULLTEXT-INDEX-Statement-Data-Definition.md)
