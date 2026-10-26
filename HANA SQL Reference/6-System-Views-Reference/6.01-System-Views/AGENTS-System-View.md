# 6.1.12 AGENTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1411–1412

Lists active data provisioning agents in the system.

## Structure

| **Column** | **Data type** | **Description** |
| --- | --- | --- |
| AGENT_NAME | NVARCHAR(256) | Displays the agent name. |
| PROTOCOL | VARCHAR(4) | Displays the protocol for communication with SAP HANA database: TCP/HTTP. |
| AGENT_HOST | NVARCHAR(64) | Displays the agent host specified when using TCP. |
| AGENT_PORT | INTEGER | Displays the agent port number specified when using TCP. |
| IS_SSL_ENABLED | VARCHAR(5) | Displays whether the agent listening on the TCP port uses SSL: TRUE/FALSE. |
| AGENT_GROUP_NAME | NVARCHAR(256) | Displays the agent clustering group to which the agent belongs. |

## Related Information

AGENT_CONFIGURATION System View [→](AGENT_CONFIGURATION-System-View.md) AGENT_GROUPS System View [→](AGENT_GROUPS-System-View.md) M_AGENTS System View [→](../6.02-Monitoring-Views/M_AGENTS-System-View.md)
