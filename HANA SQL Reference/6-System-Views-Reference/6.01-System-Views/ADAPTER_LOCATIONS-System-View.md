# 6.1.5 ADAPTER_LOCATIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1405

Displays the location of adapters.

## Structure

| **Column** | **Data type** | **Description** |
| --- | --- | --- |
| ADAPTER_NAME | NVARCHAR(64) | Displays the adapter name. |
| LOCATION | VARCHAR(11) | Displays the location of the adapter: 'indexserver', 'dpserver', 'agent'. |
| AGENT_NAME | NVARCHAR(256) | Displays the agent name. |
| CONFIGURATION | NCLOB | Displays the configuration of the adapter. |
| PROPERTIES | NCLOB | Displays the properties of the adapter. |

## Related Information

ADAPTERS System View [→](ADAPTERS-System-View.md) ADAPTER_CAPABILITIES System View [→](ADAPTER_CAPABILITIES-System-View.md)
