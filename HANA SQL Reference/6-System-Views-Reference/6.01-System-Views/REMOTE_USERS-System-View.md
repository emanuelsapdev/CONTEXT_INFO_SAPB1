# 6.1.132 REMOTE_USERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1552

Provides information about user mappings for cross-database access.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR (256) | Displays the name of the user in the local database. |
| REMOTE_USER_NAME | NVARCHAR (256) | Displays the name of the user in the remote database. |
| REMOTE_DATABASE_NAME | NVARCHAR (256) | Displays the name of the remote data base. |

## Related Information

REMOTE_SOURCES System View [→](REMOTE_SOURCES-System-View.md) REMOTE_SUBSCRIPTIONS System View [→](REMOTE_SUBSCRIPTIONS-System-View.md) CREATE USER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-USER-Statement-Access-Control.md) ALTER USER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-USER-Statement-Access-Control.md) DROP USER Statement (Access Control) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-USER-Statement-Access-Control.md)
