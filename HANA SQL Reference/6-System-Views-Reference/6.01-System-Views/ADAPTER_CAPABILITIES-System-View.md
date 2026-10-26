# 6.1.4 ADAPTER_CAPABILITIES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1404–1405

Displays supported capabilities for each adapter.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| ADAPTER_NAME | NVARCHAR(64) | Displays the adapter name. |
| SOURCE_VERSION | NVARCHAR(64) | Displays the source versions that are supported by the adapter. |
| CAPABILITY_NAME | VARCHAR(128) | Displays the capability name. |
| DESCRIPTION | NVARCHAR(512) | Displays the description of the capability. |
| SCOPE | VARCHAR(10) | Displays the capability scope. |
| IS_SDA_SUPPORTED | VARCHAR(5) | Displays whether the SDA capability is supported: TRUE/FALSE. |
| IS_CDC_SUPPORTED | VARCHAR(5) | Displays whether the CDC capability is supported: TRUE/FALSE. |

## Related Information

[ADAPTERS System View](ADAPTERS-System-View.md)

[ADAPTER_LOCATIONS System View](ADAPTER_LOCATIONS-System-View.md)
