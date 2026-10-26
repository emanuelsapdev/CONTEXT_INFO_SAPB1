# 6.2.59 M_CS_INDEXES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1718–1719

Provides information for column store indexes.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| INDEX_NAME | NVARCHAR(256) | Displays the index name. |
| PART_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| HASH_COLLISION_COUNT | BIGINT | Displays the count of hash collisions aggregated over all values. |
| CONCAT_COLUMN_NAME | NVARCHAR(256) | Displays the name of the concat column in the case of multi-column indexes. This is empty in the case of a single-column index. |

## Related Information

INDEXES System View [→](../6.01-System-Views/INDEXES-System-View.md) CREATE INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-INDEX-Statement-Data-Definition.md) ALTER INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-INDEX-Statement-Data-Definition.md) DROP INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-INDEX-Statement-Data-Definition.md)
