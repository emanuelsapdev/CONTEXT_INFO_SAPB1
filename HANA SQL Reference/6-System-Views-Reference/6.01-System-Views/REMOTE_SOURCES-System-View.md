# 6.1.123 REMOTE_SOURCES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1542–1543

Provides information about remote sources.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SUBSCRIPTION_OID | BIGINT | Displays the remote subscription OID. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| ADAPTER_NAME | NVARCHAR(256) | Displays the adapter name. |
| CONNECTION_INFO | NVARCHAR(256) | Displays the connection information. |
| LOCATION | VARCHAR(11) | Displays the adapter location |
| AGENT_NAME | NVARCHAR(256) | Displays the agent name. |
| IS_CDC_SUPPORTED | VARCHAR(5) | Displays whether or not the CDC is supported: TRUE/FALSE. |
| IS_REFRESH_OBJECTS_SUPPORTED | VARCHAR(5) | Displays whether or not refresh objects is supported: TRUE/FALSE. |
| AGENT_GROUP_NAME | NVARCHAR(256) | Displays the agent group name. |
| IS_TREE | VARCHAR(5) | Displays whether or not the browsing hierarchy is deeply nested: TRUE/ FALSE. |
| IS_LINKED_DATABASE_SUPPORTED | VARCHAR(5) | Displays whether or not the linked data base is supported for this remote source: TRUE/FALSE. |

## Related Information

REMOTE_SOURCE_OBJECTS System View [→](REMOTE_SOURCE_OBJECTS-System-View.md) REMOTE_SOURCE_OBJECT_COLUMNS System View [→](REMOTE_SOURCE_OBJECT_COLUMNS-System-View.md) REMOTE_SOURCE_OBJECT_COLUMN_CONSTRAINTS System View [→](REMOTE_SOURCE_OBJECT_COLUMN_CONSTRAINTS-System-View.md) REMOTE_SOURCE_OBJECT_COLUMN_DESCRIPTIONS System View [→](REMOTE_SOURCE_OBJECT_COLUMN_DESCRIPTIONS-System-View.md)

REMOTE_SOURCE_OBJECT_DESCRIPTIONS System View [→](REMOTE_SOURCE_OBJECT_DESCRIPTIONS-System-View.md) CREATE REMOTE SOURCE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-REMOTE-SOURCE-Statement-Access-Control.md) ALTER REMOTE SOURCE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-REMOTE-SOURCE-Statement-Access-Control.md) DROP REMOTE SOURCE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-REMOTE-SOURCE-Statement-Access-Control.md)
