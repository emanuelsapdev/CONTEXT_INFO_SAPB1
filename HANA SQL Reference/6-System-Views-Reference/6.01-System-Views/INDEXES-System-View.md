# 6.1.88 INDEXES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1506–1508

Provides information about indexes on tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the name of the table that the index is on. |
| TABLE_OID | BIGINT | Displays the object ID of the table that the index is on. |
| INDEX_NAME | NVARCHAR(256) | Displays the name of the index. |
| INDEX_OID | BIGINT | Displays the object ID for the index. |
| INDEX_TYPE | VARCHAR(32) | Displays the index type.<br>Row store index types: BTREE, BTREE_UNIQUE, CPBTREE, or CPBTREE_UNIQUE.<br>Column store index types: INVERTED VALUE, INVERTED VALUE UNIQUE, IN VERTED HASH, INVERTED INDIVID UAL, FULLTEXT TEXT ANALYSIS, or GEOCODE. |
| CONSTRAINT | VARCHAR(32) | Displays the constraint on the index: UNIQUE, NOT_NULL_UNIQUE, or PRIMARY_KEY. |
| KEY_LENGTH | SMALLINT | Displays the length of the key. |
| BTREE_FILL_FACTOR | SMALLINT | Displays the B-tree fill factor from 50-100. |
| BTREE_SPLIT_TYPE | TINYINT | Displays the B-tree split type: SPLIT_PERCENT/SPLIT_INVOKER. |
| BTREE_SPLIT_POSITION | TINYINT | Displays the B-tree split position from 0-100. |
| CREATE_TIME | TIMESTAMP | Displays the time that the index was created. |
| STORAGE_TYPE | VARCHAR(8) | Displays the partial index storage type. NULL is returned if it is not a partial index. For multistore partial index, the value can be a string of DEFAULT\|EX TENDED. |
| LOAD_UNIT | VARCHAR(7) | Displays the load unit for the index. Valid values are: COLUMN, PAGE, DE FAULT, or NULL. |

## Related Information

INDEX_COLUMNS System View [→](INDEX_COLUMNS-System-View.md) M_INDEXING_QUEUES System View [→](../6.02-Monitoring-Views/M_INDEXING_QUEUES-System-View.md) CREATE INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-INDEX-Statement-Data-Definition.md)

ALTER INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-INDEX-Statement-Data-Definition.md) RENAME INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RENAME-INDEX-Statement-Data-Definition.md) DROP INDEX Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-INDEX-Statement-Data-Definition.md)
