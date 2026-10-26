# 6.2.126 M_HOST_AGENT_INFORMATION System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1813–1814

Displays computer system information retrieved from the SAP Host Agent.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| CLASS_NAME | NVARCHAR(64) | Displays the name of the class. |
| INSTANCE_NUMBER | INTEGER | Displays the number of instances per class, for example, if the host has multi ple CPUs, then all the properties of one CPU have the same instance number. |
| PROPERTY_NAME | NVARCHAR(64) | Displays the name of the property. |
| PROPERTY_VALUE | NVARCHAR(512) | Displays the value of the property. |

## Related Information

M_HOST_AGENT_METRICS System View [→](M_HOST_AGENT_METRICS-System-View.md) AGENTS System View [→](../6.01-System-Views/AGENTS-System-View.md) AGENT_CONFIGURATION System View [→](../6.01-System-Views/AGENT_CONFIGURATION-System-View.md) M_AGENTS System View [→](M_AGENTS-System-View.md)
