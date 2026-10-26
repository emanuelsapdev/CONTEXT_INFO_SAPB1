# 6.2.83 M_DEBUG_CONNECTIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1753–1754

Provides an overview of connections used per debug session.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| DEBUG_SESSION_ID | VARCHAR(32) | Displays the landscape-wide unique identifier for debug session. |
| CONNECTION_ID | INTEGER | Displays the connection that is used for communication. |
| CONNECTION_USAGE | VARCHAR(16) | Indicates whether this connection is used for debugger communication or debugging. |
| OPERATION | NVARCHAR(512) | Displays the operation that is currently running within this connection. |

## Related Information

M_DEBUG_SESSIONS System View [→](M_DEBUG_SESSIONS-System-View.md) M_CE_DEBUG_INFOS System View [→](M_CE_DEBUG_INFOS-System-View.md) M_CE_DEBUG_JSONS System View [→](M_CE_DEBUG_JSONS-System-View.md)
