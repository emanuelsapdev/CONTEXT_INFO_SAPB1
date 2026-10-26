# 6.2.40 M_COLLECTION_TABLE_VIRTUAL_FILES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1679–1680

Provides information about the virtual files for JSON collections.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| TABLE_OID | BIGINT | Displays the object ID of the table. |
| COLLECTION_ID | BIGINT | Displays the ID of the collection. |
| VOLUME_ID | INTEGER | Displays the volume ID. |
| FILE_TYPE | VARCHAR | Displays the type of file. |
| INTERNAL_OBJECT_ID | BIGINT | Displays the internal identifier for the table. |
| FILE | VARCHAR(256) | Displays the file. |
| CONTAINER_ID | BIGINT | Displays the container ID. |
| PHYSICAL_SIZE | BIGINT | Displays the storage size used for the file in bytes. |
| PAGE_COUNT | BIGINT | Displays the number of storage pages used for the file. |

## Related Information

M_COLLECTION_TABLES System View [→](M_COLLECTION_TABLES-System-View.md) DROP COLLECTION Statement (JSON Document Store) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-COLLECTION-Statement-JSON-Document-Store.md)
