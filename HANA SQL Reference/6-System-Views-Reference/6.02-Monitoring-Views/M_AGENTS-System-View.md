# 6.2.10 M_AGENTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1649–1650

Provides agent host information.

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| AGENT_NAME | NVARCHAR(256) | Displays the agent name. |
| FREE_PHYSICAL_MEMORY | BIGINT | Displays the free physical memory on the agent host in bytes. |
| FREE_SWAP_SPACE | BIGINT | Displays the free swap memory on the agent host in bytes. |
| LAST_CONNECT_TIME | TIMESTAMP | Displays the last successful connection time. |
| SYS_TIMESTAMP | TIMESTAMP | Displays the agent host timestamp in the agent host's local timezone. |
| USED_PHYSICAL_MEMORY | BIGINT | Displays the used physical memory on the agent host in bytes. |
| USED_SWAP_SPACE | BIGINT | Displays the used swap memory on the agent host in bytes. |
| UTC_TIMESTAMP | TIMESTAMP | Displays the agent host timestamp in UTC. |
| AGENT_VERSION | VARCHAR(32) | Displays the agent version. |
| AGENT_STATUS | VARCHAR(16) | Displays the agent status. |

## Related Information

AGENTS System View [→](../6.01-System-Views/AGENTS-System-View.md) AGENT_CONFIGURATION System View [→](../6.01-System-Views/AGENT_CONFIGURATION-System-View.md) AGENT_GROUPS System View [→](../6.01-System-Views/AGENT_GROUPS-System-View.md)
