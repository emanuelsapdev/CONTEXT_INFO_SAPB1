# 6.2.290 M_STREAMING_PROJECT_STREAMS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2052–2054

Provides streaming project stream monitoring information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema in which the application is deployed. |
| PROJECT_NAME | NVARCHAR(256) | Displays the name given to the project. |
| PROJECT_INSTANCE | INTEGER | Displays the instance number of the project. |
| STREAM_NAME | NVARCHAR(256) | Displays the name of the stream. |
| STREAM_TYPE | NVARCHAR(32) | Displays the type of stream: STREAM, DELTASTREAM, WINDOW, or META DATA. |
| VISIBILITY | NVARCHAR(32) | Displays the visibility of the stream: IN PUT, OUTPUT, LOCAL, or INTERMEDI ATE. |
| TARGET_NAME | NVARCHAR(256) | Denotes that this stream is an intermediate stream used to populate this target. |
| GD_SUPPORT_LEVEL | NVARCHAR(32) | Indicates whether GD (guaranteed delivery) is enabled for the stream or window: NOT_SUPPORTED, SUPPORTED, or SUPPORTED_WITH_CHECKPOINT. |
| TRANSACTION_THROUGHPUT | REAL | Displays the stream's performance, in transactions per second, since the last update. |
| ROW_THROUGHPUT | REAL | Displays the stream's performance, in rows per second, since the last update. |
| INCREMENTAL_TRANSACTION_COUNT | BIGINT | Displays the number of transactions processed by the server since the last update. |
| INCREMENTAL_ROW_COUNT | BIGINT | Displays the number of rows processed by the server since the last update. |
| QUEUE_SIZE | INTEGER | Displays the stream's input queue size in bytes. |
| STORE_ROW_COUNT | BIGINT | Displays the Number of rows in the store. This is only applicable for Windows. |
| SEQUENCE_NUMBER | BIGINT | Displays a sequentially increasing number that represents how many times the statistics have been updated. |
| CPU_CORE_UTILIZATION | REAL | Displays the total CPU usage for the stream thread, as a percentage of a single CPU core. |
| CPU_UTILIZATION | REAL | Displays the total CPU usage for the stream, as a percentage of all CPU cores on the machine. |
| CPU_SYSTEM_UTILIZATION | REAL | Displays the system CPU usage for the stream, as a percentage of all CPU cores on the machine. |
| CPU_USER_UTILIZATION | REAL | Displays the user CPU usage for the stream, as a percentage of all CPU cores on the machine. |
| TOTAL_CPU_TIME | BIGINT | Displays the total CPU time since the creation of the stream, in microseconds. |
| TOTAL_CPU_SYSTEM_TIME | BIGINT | Displays the total system CPU time, in microseconds, since the creation of the client thread. |
| TOTAL_CPU_USER_TIME | BIGINT | Displays the total user CPU time, in microseconds, since the creation of the client thread. |
| LAST_UPDATE_TIME | TIMESTAMP | Displays the last time the statistics were updated for the stream. |

## Related Information

M_STREAMING_PROJECT_ADAPTERS System View [→](M_STREAMING_PROJECT_ADAPTERS-System-View.md) M_STREAMING_PROJECT_SUBSCRIBERS System View [→](M_STREAMING_PROJECT_SUBSCRIBERS-System-View.md) M_STREAMING_PROJECT_GD_SUBSCRIPTIONS System View [→](M_STREAMING_PROJECT_GD_SUBSCRIPTIONS-System-View.md) M_STREAMING_PROJECT_PUBLISHERS System View [→](M_STREAMING_PROJECT_PUBLISHERS-System-View.md)
