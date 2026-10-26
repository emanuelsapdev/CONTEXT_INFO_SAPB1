# 6.1.90 INVALID_CONNECT_ATTEMPTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1509–1510

Provides the number of invalid connection attempts for a user between two successful connections.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| USER_NAME | NVARCHAR(256) | Displays the name of the user. |
| SUCCESSFUL_CONNECT_TIME | TIMESTAMP | Displays the time the valid connection was attempted. |
| INVALID_CONNECT_ATTEMPTS | BIGINT | Displays the number of invalid connection attempts for this user since the last successful connection. |

## Related Information

CONNECT Statement (Session Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CONNECT-Statement-Session-Management.md) M_CONNECTIONS System View [→](../6.02-Monitoring-Views/M_CONNECTIONS-System-View.md)
