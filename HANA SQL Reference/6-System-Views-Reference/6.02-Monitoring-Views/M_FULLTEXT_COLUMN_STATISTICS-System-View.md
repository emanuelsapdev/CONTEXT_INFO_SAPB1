# 6.2.116 M_FULLTEXT_COLUMN_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1802–1803

Tracks the usage of fulltext indexes.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name to which the table belongs. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| COLUMN_NAME | NVARCHAR(256) | Displays the internal name of the text column. |
| LOOKUP_COUNT | BIGINT | Displays the total number of text look ups executed on this column. |
| LAST_LOOKUP_TIME | TIMESTAMP | Displays the timestamp when the last lookup was executed. |

## Related Information

M_FULLTEXT_QUEUES System View [→](M_FULLTEXT_QUEUES-System-View.md) CREATE FULLTEXT INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-FULLTEXT-INDEX-Statement-Data-Definition.md) ALTER FULLTEXT INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-FULLTEXT-INDEX-Statement-Data-Definition.md) DROP FULLTEXT INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-FULLTEXT-INDEX-Statement-Data-Definition.md)
