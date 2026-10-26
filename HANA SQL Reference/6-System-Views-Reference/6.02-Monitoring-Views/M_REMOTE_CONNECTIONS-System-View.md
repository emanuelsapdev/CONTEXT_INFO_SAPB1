# 6.2.218 M_REMOTE_CONNECTIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1947–1948

Provides detailed information on remote connections between databases and remote sources. The information includes connection status, adapter name, and adapter properties.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| CONNECTION_ID | INTEGER | Displays the connection ID. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name. |
| ADAPTER_NAME | NVARCHAR(256) | Displays the adapter name. |
| REMOTE_SOURCE_USER_NAME | NVARCHAR(256) | Displays the remote source user name. |
| START_TIME | TIMESTAMP | Displays the connected time. |
| CONNECTION_STATUS | VARCHAR(16) | Displays the connection status: CON NECTED/DISCONNECTED. |
| DETAILS | VARCHAR(512) | Displays the adapter properties. |
| STATEMENT_COUNT | BIGINT | Displays the number of executed statements. |

## Related Information

M_CONNECTIONS System View [→](M_CONNECTIONS-System-View.md) CONNECT Statement (Session Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CONNECT-Statement-Session-Management.md)
