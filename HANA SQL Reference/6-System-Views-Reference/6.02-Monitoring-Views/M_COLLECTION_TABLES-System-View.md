# 6.2.39 M_COLLECTION_TABLES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1678–1679

Provides information about JSON collections.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| TABLE_OID | BIGINT | Displays the object ID of the table. |
| COLLECTION_ID | BIGINT | Displays the ID of the collection. |
| CREATE_TIME | TIMESTAMP | Displays the creation time of the table collection. |
| ESTIMATED_DOCUMENT_COUNT | BIGINT | Displays the estimated document count. |
| ALLOCATED_SIZE | BIGINT | Displays the allocated size of the collection in bytes. |
| USED_SIZE | BIGINT | Displays the used size of the collection in bytes. |
| LOAD_STATUS | VARCHAR | Displays whether the table collection is LOADED or UNLOADED. |

## Related Information

M_COLLECTION_TABLE_VIRTUAL_FILES System View [→](M_COLLECTION_TABLE_VIRTUAL_FILES-System-View.md) DROP COLLECTION Statement (JSON Document Store) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-COLLECTION-Statement-JSON-Document-Store.md)
