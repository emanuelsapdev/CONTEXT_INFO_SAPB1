# 6.1.126 REMOTE_SOURCE_OBJECT_COLUMN_CONSTRAINTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1545–1546

Provides remote source object column constraint information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the user name. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| OBJECT_NAME | NVARCHAR(5000) | Displays the unique name to identify the remote source object. |
| COLUMN_NAME | NVARCHAR(256) | Displays the name of the column. |
| POSITION | INTEGER | Displays the position of the column. |
| CONSTRAINT_NAME | NVARCHAR(256) | Displays the constraint name. |
| IS_PRIMARY_KEY | VARCHAR(5) | Displays whether or not the specified key is the primary key: TRUE/FALSE. |
| IS_UNIQUE_KEY | VARCHAR(5) | Displays whether or not the specified key is unique: TRUE/FALSE. |

## Related Information

REMOTE_SOURCES System View [→](REMOTE_SOURCES-System-View.md) REMOTE_SOURCE_OBJECTS System View [→](REMOTE_SOURCE_OBJECTS-System-View.md) REMOTE_SOURCE_OBJECT_COLUMNS System View [→](REMOTE_SOURCE_OBJECT_COLUMNS-System-View.md) REMOTE_SOURCE_OBJECT_COLUMN_DESCRIPTIONS System View [→](REMOTE_SOURCE_OBJECT_COLUMN_DESCRIPTIONS-System-View.md) REMOTE_SOURCE_OBJECT_DESCRIPTIONS System View [→](REMOTE_SOURCE_OBJECT_DESCRIPTIONS-System-View.md) REMOTE_SUBSCRIPTIONS System View [→](REMOTE_SUBSCRIPTIONS-System-View.md) CREATE REMOTE SOURCE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-REMOTE-SOURCE-Statement-Access-Control.md) ALTER REMOTE SOURCE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-REMOTE-SOURCE-Statement-Access-Control.md) DROP REMOTE SOURCE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-REMOTE-SOURCE-Statement-Access-Control.md) CONSTRAINTS System View [→](CONSTRAINTS-System-View.md)
