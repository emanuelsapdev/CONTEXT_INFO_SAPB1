# 6.1.3 ADAPTERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1403–1404

Displays adapters available in the SAP HANA system.

## Structure

| **Column** | **Data type** | **Description** |
| --- | --- | --- |
| ADAPTER_NAME | NVARCHAR(64) | Displays the adapter name. |
| PROPERTIES | NVARCHAR(1000) | Displays the optional properties of the adapter such as dis play_name and description. |
| CONFIGURATION | NCLOB | Displays the UI properties that must be displayed when con figuring remote data source. |
| IS_SYSTEM_ADAPTER | VARCHAR(5) | Displays whether the adapter is a system adapter: TRUE/ FALSE. |
| IS_ESS_DEFINITION_SUPPORTED | VARCHAR(5) | Displays whether the procedure GET_REMOTE_SOURCE_TABLE_ESS_DEFINITIONS is enabled for remote sources created using this adapter: TRUE/FALSE. |

## Related Information

ADAPTER_CAPABILITIES System View [→](ADAPTER_CAPABILITIES-System-View.md) ADAPTER_LOCATIONS System View [→](ADAPTER_LOCATIONS-System-View.md)
