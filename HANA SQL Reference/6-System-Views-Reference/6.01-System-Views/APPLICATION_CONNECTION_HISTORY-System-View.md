# 6.1.19 APPLICATION_CONNECTION_HISTORY System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1420–1421

Provides stored application connection history information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| APPLICATION_NAME | NVARCHAR(256) | Displays the application name. |
| CLIENT_IP | VARCHAR(45) | Displays the IP address of the client. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| CONNECT_DATE | DATE | Displays the established date of the connection. |
| CONNECT_COUNT | INTEGER | Displays the count of connections established in a day. |

## Related Information

APPLICATION_ENCRYPTION_KEYS System View [→](APPLICATION_ENCRYPTION_KEYS-System-View.md) CONNECT Statement (Session Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CONNECT-Statement-Session-Management.md) M_CONNECTIONS System View [→](../6.02-Monitoring-Views/M_CONNECTIONS-System-View.md)
