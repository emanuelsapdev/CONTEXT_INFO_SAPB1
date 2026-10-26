# 6.2.288 M_STREAMING_PROJECT_GD_SUBSCRIPTIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2048–2050

Provides streaming project Guaranteed Delivery (GD) subscription monitoring information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema in which the application is deployed. |
| PROJECT_NAME | NVARCHAR(256) | Displays the name given to the project. |
| PROJECT_INSTANCE | INTEGER | Displays the instance number of the project. |
| GD_KEY | NVARCHAR(1024) | Displays the automatically generated key for the GD session. |
| STREAM_NAME | NVARCHAR(256) | Displays the name of the stream being subscribed to. |
| USER_NAME | NVARCHAR(256) | Displays the name of the subscribing user. |
| GD_NAME | NVARCHAR(256) | Displays the name of the guaranteed delivery session. |
| GD_SEQUENCE_NUMBER | BIGINT | Displays the sequence number of the last event committed from stream_name in this guaranteed delivery session. A value of 0 indicates that no commits have been issued. |
| STREAMING_CONNECTION_ID | INTEGER | Displays the unique handle for active external subscribers. For active internal adapters it is always 0. Inactive subscribers have a value of -1. |
| LAST_UPDATE_TIME | TIMESTAMP | Displays the last time the statistic was updated for the GD subscription. |

## Related Information

M_STREAMING_PROJECT_ADAPTERS System View [→](M_STREAMING_PROJECT_ADAPTERS-System-View.md) M_STREAMING_PROJECT_PUBLISHERS System View [→](M_STREAMING_PROJECT_PUBLISHERS-System-View.md) M_STREAMING_PROJECT_STREAMS System View [→](M_STREAMING_PROJECT_STREAMS-System-View.md) M_STREAMING_PROJECT_SUBSCRIBERS System View [→](M_STREAMING_PROJECT_SUBSCRIBERS-System-View.md)
