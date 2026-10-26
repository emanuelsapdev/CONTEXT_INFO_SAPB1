# 6.2.286 M_STREAMING_PROJECT_ADAPTERS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2046–2047

Provides streaming project adapter monitoring information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema in which the application is deployed. |
| PROJECT_NAME | NVARCHAR(256) | Displays the name given to the project. |
| PROJECT_INSTANCE | INTEGER | Displays the instance number of the project. |
| ADAPTER_NAME | NVARCHAR(256) | Displays the name of the adapter. |
| ADAPTER_TYPE | VARCHAR(32) | Displays the adapter type defined in the ATTACH ADAPTER statement. |
| STREAM_NAME | NVARCHAR(256) | Displays the name of the stream on which the adapter is defined. |
| IS_INPUT | VARCHAR(5) | Indicates whether or not the connection is an input or an output. This value is TRUE for an input connection and FALSE for an output connection. |
| STARTUP_GROUP_NAME | NVARCHAR(256) | Displays the start up group to which the connector belongs. |
| ADAPTER_STATE | VARCHAR(32) | Displays the state of the adapter: READY, INITIAL, CONTINOUS, IDLE, DONE, or DEAD. |
| TOTAL_ROW_COUNT | BIGINT | Displays the total number of data records recognized in the input data. |
| SUCCESSFUL_ROW_COUNT | BIGINT | Displays the number of data records successfully processed. |
| UNSUCCESSFUL_ROW_COUNT | BIGINT | Displays the number of data records that experienced errors. |
| MEMORY_USAGE | BIGINT | Displays the total memory used by the adapter, in bytes. |
| LAST_ERROR_TIME | TIMESTAMP | Displays the tast time that an error occurred. |
| LAST_ERROR_MESSAGE | NVARCHAR(256) | Displays the complete text of the error message as written to the log. |
| LATENCY | BIGINT | Displays the latency introduced by the adapter. |

## Related Information

M_STREAMING_PROJECT_STREAMS System View [Streaming Analytics] [→](../../7-System-Views-Additional-Contexts/7.02-Streaming-Analytics/7.02.08-M_STREAMING_PROJECT_STREAMS-System-View-Streaming-Analytics.md) M_STREAMING_PROJECT_ADAPTER_STATISTICS System View [→](M_STREAMING_PROJECT_ADAPTER_STATISTICS-System-View.md) M_STREAMING_PROJECT_GD_SUBSCRIPTIONS System View [→](M_STREAMING_PROJECT_GD_SUBSCRIPTIONS-System-View.md) M_STREAMING_PROJECT_PUBLISHERS System View [→](M_STREAMING_PROJECT_PUBLISHERS-System-View.md) M_STREAMING_PROJECT_STREAMS System View [→](M_STREAMING_PROJECT_STREAMS-System-View.md) M_STREAMING_PROJECT_SUBSCRIBERS System View [→](M_STREAMING_PROJECT_SUBSCRIBERS-System-View.md)
