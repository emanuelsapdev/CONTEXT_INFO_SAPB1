# 6.2.118 M_FUZZY_SEARCH_INDEXES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1804–1806

Provides runtime information of fuzzy search indexes of column tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| PART_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| FUZZY_SEARCH_MODE | NVARCHAR(256) | Displays the fuzzy index search mode. |
| MEMORY_SIZE_IN_TOTAL | BIGINT | Displays the sum of MEMORY_SIZE_IN_MAIN and MEMORY_SIZE_IN_DELTA in bytes. |
| MEMORY_SIZE_IN_MAIN | BIGINT | Displays the current size of the fuzzy search indexes in main in bytes. This value is 0 if not loaded. |
| MEMORY_SIZE_IN_DELTA | BIGINT | Displays the current size of the fuzzy search indexes in delta, in bytes. This value is 0 if not loaded. |
| LOADED | VARCHAR(5) | Displays a flag to indicate that tge column is loaded into memory: TRUE/ FALSE. |

## Additional Information

This view shows the memory usage of all fuzzy search indexes. A fuzzy search index has no name and is identified by its schema name, table name, and column name.

## Related Information

CREATE FULLTEXT INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-FULLTEXT-INDEX-Statement-Data-Definition.md) ALTER FULLTEXT INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-FULLTEXT-INDEX-Statement-Data-Definition.md) INDEXES System View [→](../6.01-System-Views/INDEXES-System-View.md)
