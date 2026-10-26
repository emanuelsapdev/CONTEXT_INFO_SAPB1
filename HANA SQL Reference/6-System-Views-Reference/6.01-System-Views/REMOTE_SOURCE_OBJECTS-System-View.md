# 6.1.124 REMOTE_SOURCE_OBJECTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1543–1544

Provides remote source object information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the user name. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| OBJECT_NAME | NVARCHAR(5000) | Displays the unique name to identify the remote source object. |
| DISPLAY_NAME | NVARCHAR(256) | Displays the name for the object. |
| IS_IMPORTABLE | VARCHAR(5) | Displays whether or not the object is importable as a virtual table: TRUE/ FALSE. |
| IS_EXPANDABLE | VARCHAR(5) | Displays whether or not the object can be expanded or browsed to get inner objects: TRUE/FALSE. |
| PARENT_OBJECT_NAME | NVARCHAR(5000) | Displays the parent object name for the specified object. |
| DEFINITION_TYPE | VARCHAR(32) | Displays the object definition type. |
| DEFINITION | NCLOB | Displays the object definition. |

## Related Information

REMOTE_SOURCES System View [→](REMOTE_SOURCES-System-View.md) REMOTE_SOURCE_OBJECT_COLUMNS System View [→](REMOTE_SOURCE_OBJECT_COLUMNS-System-View.md) REMOTE_SOURCE_OBJECT_COLUMN_CONSTRAINTS System View [→](REMOTE_SOURCE_OBJECT_COLUMN_CONSTRAINTS-System-View.md) REMOTE_SOURCE_OBJECT_COLUMN_DESCRIPTIONS System View [→](REMOTE_SOURCE_OBJECT_COLUMN_DESCRIPTIONS-System-View.md)

REMOTE_SOURCE_OBJECT_DESCRIPTIONS System View [→](REMOTE_SOURCE_OBJECT_DESCRIPTIONS-System-View.md) REMOTE_SUBSCRIPTIONS System View [→](REMOTE_SUBSCRIPTIONS-System-View.md) REMOTE_SUBSCRIPTION_DATA_CONTAINERS System View [→](REMOTE_SUBSCRIPTION_DATA_CONTAINERS-System-View.md) CREATE REMOTE SOURCE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-REMOTE-SOURCE-Statement-Access-Control.md) ALTER REMOTE SOURCE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-REMOTE-SOURCE-Statement-Access-Control.md) DROP REMOTE SOURCE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-REMOTE-SOURCE-Statement-Access-Control.md)
