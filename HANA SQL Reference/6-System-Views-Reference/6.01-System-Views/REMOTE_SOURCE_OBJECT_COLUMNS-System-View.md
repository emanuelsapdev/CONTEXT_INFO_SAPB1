# 6.1.125 REMOTE_SOURCE_OBJECT_COLUMNS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1544–1545

Provides remote source object column information.

## Structure

| **Column Name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the user name. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| OBJECT_NAME | NVARCHAR(5000) | Displays the unique name to identify the remote source object. |
| COLUMN_NAME | NVARCHAR(256) | Displays the name of the column. |
| DATA_TYPE_NAME | VARCHAR(16) | Displays the SAP HANA data type. |
| REMOTE_DATA_TYPE_NAME | NVARCHAR(256) | Displays the remote data type. |
| REMOTE_CONTENT_TYPE | NVARCHAR(256) | Displays the remote content type. |
| LENGTH | INTEGER | Displays the length of the column. If there is a decimal then this value is the precision. |
| SCALE | INTEGER | Displays the scale. |
| IS_NULLABLE | VARCHAR(5) | Displays whether or not this column is allowed to be NULL: TRUE/FALSE. |
| IS_AUTOINCREMENT | VARCHAR(5) | Displays whether or not this column is automatically incremented: TRUE/ FALSE. |

## Related Information

REMOTE_SOURCES System View [→](REMOTE_SOURCES-System-View.md) REMOTE_SOURCE_OBJECTS System View [→](REMOTE_SOURCE_OBJECTS-System-View.md) REMOTE_SOURCE_OBJECT_COLUMN_CONSTRAINTS System View [→](REMOTE_SOURCE_OBJECT_COLUMN_CONSTRAINTS-System-View.md) REMOTE_SOURCE_OBJECT_COLUMN_DESCRIPTIONS System View [→](REMOTE_SOURCE_OBJECT_COLUMN_DESCRIPTIONS-System-View.md) REMOTE_SOURCE_OBJECT_DESCRIPTIONS System View [→](REMOTE_SOURCE_OBJECT_DESCRIPTIONS-System-View.md) REMOTE_SUBSCRIPTIONS System View [→](REMOTE_SUBSCRIPTIONS-System-View.md) REMOTE_SUBSCRIPTION_DATA_CONTAINERS System View [→](REMOTE_SUBSCRIPTION_DATA_CONTAINERS-System-View.md) CREATE REMOTE SOURCE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-REMOTE-SOURCE-Statement-Access-Control.md) ALTER REMOTE SOURCE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-REMOTE-SOURCE-Statement-Access-Control.md) DROP REMOTE SOURCE Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-REMOTE-SOURCE-Statement-Access-Control.md)
