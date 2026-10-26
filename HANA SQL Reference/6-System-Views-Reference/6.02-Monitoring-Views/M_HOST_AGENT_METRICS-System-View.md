# 6.2.127 M_HOST_AGENT_METRICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1814–1815

Displays performance metrics retrieved from the SAP Host Agent.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| CLASS_NAME | NVARCHAR(64) | Displays the name of the class, which identifies the property as a CIM metric or a SAPOSCOL metric. |
| INSTANCE_ID | NVARCHAR(256) | Identifies the metric of a specific measured element. |
| DEFINITION_ID | NVARCHAR(64) | Displays the ID of the metric. |
| TIMESTAMP | TIMESTAMP | Displays the timestamp from the host agent when the metric instance was created. |
| CAPTION | NVARCHAR(64) | Displays the name of the metric. |
| VALUE | NVARCHAR(128) | Displays the value of the metric. |
| UNIT | NVARCHAR(32) | Displays the unit of the metric (bytes, percent, and so on). |
| CIM_DATA_TYPE | SMALLINT | Displays a numerical value that identi fies the data type of the metric as defined by the CIM standard. |
| DESCRIPTION | NVARCHAR(512) | Displays a detailed description of the metric. |
| MEASURED_ELEMENT_NAME | NVARCHAR(256) | Displays the name of the measured element: CPU ID, file system name, net work port name, or disk name. |
| MEASURED_ELEMENT_TYPE | NVARCHAR(64) | Displays the type of measured element (file system, operating system, and so on). |

## Related Information

M_HOST_AGENT_INFORMATION System View [→](M_HOST_AGENT_INFORMATION-System-View.md) AGENTS System View [→](../6.01-System-Views/AGENTS-System-View.md) AGENT_CONFIGURATION System View [→](../6.01-System-Views/AGENT_CONFIGURATION-System-View.md) M_AGENTS System View [→](M_AGENTS-System-View.md)
