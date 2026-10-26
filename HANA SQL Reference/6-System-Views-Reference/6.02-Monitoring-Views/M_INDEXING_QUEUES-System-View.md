# 6.2.132 M_INDEXING_QUEUES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1825–1827

Provides the status of indexing queues.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| QUEUE_TYPE | VARCHAR(16) | Displays the type of the queue: TEXT/ GEOCODE. |
| INDEX_OID | BIGINT | Displays the OID of the corresponding index. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema of the data table. |
| TABLE_NAME | NVARCHAR(256) | Displays the name of the data table. |
| PART_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| COLUMN_NAME | NVARCHAR(256) | Displays the name of the document column. |
| STATUS | NVARCHAR(16) | Displays the queue status: ACTIVE/ SUSPENDED. |
| TOTAL_DOCUMENT_COUNT | BIGINT | Displays the total number of documents in the original table. |
| INDEXED_DOCUMENT_COUNT | BIGINT | Displays the number of successfully indexed documents. |
| QUEUE_DOCUMENT_COUNT | BIGINT | Displays the number of documents in the queue. |
| ERROR_DOCUMENT_COUNT | BIGINT | Displays the number of failed documents. |

## Related Information

INDEXING_STATUS Function (Fulltext) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/INDEXING_STATUS-Function-Fulltext.md) INDEXES System View [→](../6.01-System-Views/INDEXES-System-View.md) ALTER INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-INDEX-Statement-Data-Definition.md) CREATE INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-INDEX-Statement-Data-Definition.md) RENAME INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RENAME-INDEX-Statement-Data-Definition.md)

[DROP INDEX Statement (Data Definition)](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-INDEX-Statement-Data-Definition.md)
