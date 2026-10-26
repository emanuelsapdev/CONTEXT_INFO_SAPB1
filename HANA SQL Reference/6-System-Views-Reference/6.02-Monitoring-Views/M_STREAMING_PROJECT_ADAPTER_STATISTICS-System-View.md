# 6.2.287 M_STREAMING_PROJECT_ADAPTER_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2047–2048

Provides streaming project adapter statistics monitoring information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema in which the application is deployed. |
| PROJECT_NAME | NVARCHAR(256) | Displays the name given to the project. |
| PROJECT_INSTANCE | INTEGER | Displays the instance number of the project. |
| ADAPTER_NAME | NVARCHAR(256) | Displays the name of the adapter. |
| STATISTICS_NAME | VARCHAR(128) | Displays the name of the adapter statistic. |
| STATISTICS_VALUE | NVARCHAR(256) | Displays the value for the statistic. This value is converted to a string. |
| LAST_UPDATE_TIME | TIMESTAMP | Displays the last time the statistic was updated for the adapter. |

## Related Information

M_STREAMING_PROJECT_ADAPTERS System View [→](M_STREAMING_PROJECT_ADAPTERS-System-View.md) M_STREAMING_PROJECT_GD_SUBSCRIPTIONS System View [→](M_STREAMING_PROJECT_GD_SUBSCRIPTIONS-System-View.md) M_STREAMING_PROJECT_PUBLISHERS System View [→](M_STREAMING_PROJECT_PUBLISHERS-System-View.md) M_STREAMING_PROJECT_STREAMS System View [→](M_STREAMING_PROJECT_STREAMS-System-View.md) M_STREAMING_PROJECT_SUBSCRIBERS System View [→](M_STREAMING_PROJECT_SUBSCRIBERS-System-View.md)
