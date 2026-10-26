# 6.1.190 VIRTUAL_TABLES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1625–1626

Provides information about virtual tables.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| REMOTE_DB_NAME | NVARCHAR(256) | Displays the remote database name. |
| REMOTE_OWNER_NAME | NVARCHAR(256) | Displays the remote owner name. |
| REMOTE_OBJECT_NAME | NVARCHAR(256) | Displays the remote object name. |
| IS_INSERTABLE | VARCHAR(5) | Displays whether or not INSERT is supported: TRUE/FALSE. |
| IS_UPDATABLE | VARCHAR(5) | Displays whether or not UPDATE is supported: TRUE/FALSE. |
| IS_DELETABLE | VARCHAR(5) | Displays whether or not DELETE is supported: TRUE/FALSE. |
| IS_UPSERTABLE | VARCHAR(5) | Displays whether or not UPSERT is supported: TRUE/FALSE. |
| IS_SELECTABLE | VARCHAR(5) | Displays whether or not SELECT is supported: TRUE/FALSE. |
| IS_REMOTE_SUBSCRIPTION_SUPPORTED | VARCHAR(5) | Displays whether or not REMOTE SUB SCRIPTION is supported: TRUE/FALSE. |
| IS_REMOTE_SUBSCRIPTION_TRANSACTIONAL | VARCHAR(5) | Displays whether or not transactional REMOTE SUBSCRIPTION is supported: TRUE/FALSE. |

## Related Information

CREATE VIRTUAL TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-VIRTUAL-TABLE-Statement-Data-Definition.md) ALTER VIRTUAL TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-VIRTUAL-TABLE-Statement-Data-Definition.md)

VIRTUAL_TABLE_PARAMETERS System View [→](VIRTUAL_TABLE_PARAMETERS-System-View.md) VIRTUAL_TABLE_PROPERTIES System View [→](VIRTUAL_TABLE_PROPERTIES-System-View.md)
