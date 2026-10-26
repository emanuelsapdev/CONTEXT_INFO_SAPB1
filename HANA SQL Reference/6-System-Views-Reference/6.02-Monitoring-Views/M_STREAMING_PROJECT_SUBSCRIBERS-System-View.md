# 6.2.291 M_STREAMING_PROJECT_SUBSCRIBERS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2054–2057

Provides monitoring information regarding streaming project subscribers.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema in which the application is deployed. |
| PROJECT_NAME | NVARCHAR(256) | Displays the name given to the project. |
| PROJECT_INSTANCE | INTEGER | Displays the instance number of the project. |
| STREAMING_CONNECTION_ID | INTEGER | Displays the unique handle identifying the connection. |
| STREAM_NAME | NVARCHAR(256) | Displays the name of the stream. |
| USER_NAME | NVARCHAR(256) | Displays the user name provided by the client during the connection establishment. This value is shown once the user is authenticated. |
| CLIENT_HOST | NVARCHAR(256) | Displays the symbolic host name of the client machine, if available. If not available, the host is the IP address of the client machine. |
| CLIENT_IP | VARCHAR(45) | Displays the IP address of the client machine as a string. |
| CLIENT_PORT | INTEGER | Displays the TCP port number from which the connection originates. |
| CONNECTION_TAG | NVARCHAR(256) | Displays the user-provided symbolic connection tag name. If this is not set by the user, then the connection tag is NULL. |
| IS_SUBSCRIBED | NVARCHAR(5) | Displays the whether or not the user is subscribed to a stream: TRUE/FALSE. |
| TRANSACTION_THROUGHPUT | REAL | Displays the client's performance, in transactions per second, sent by the client since the last update. Envelopes and any service messages count as transactions. |
| ROW_THROUGHPUT | REAL | Displays the client's performance, in data rows per second, sent by the client since the last update. |
| INCREMENTAL_TRANSACTION_COUNT | BIGINT | Displays the number of transactions, envelopes, or messages sent by the client since the last update. |
| INCREMENTAL_ROW_COUNT | BIGINT | Displays the number of data rows sent by the client since the last update. |
| TOTAL_TRANSACTION_COUNT | BIGINT | Displays the total number of transactions, envelopes, or messages sent by the client. |
| TOTAL_ROW_COUNT | BIGINT | Displays the total number of data rows received by the client. |
| TOTAL_ROWS_DROPPED_COUNT | BIGINT | Displays the total number of data rows dropped in the gateway because they were not read quickly enough by the client. |
| ACCUMULATOR_SIZE | INTEGER | Displays the number of rows collected in the accumulator to be sent in the next pulse. This value is for pulsed subscriptions only. |
| QUEUE_SIZE | INTEGER | Displays the number of rows queued for transmission to the client. |
| QUEUE_UTILIZATION | REAL | Displays the percentage usage of the queue for transmitting rows to the client. |
| WORK_QUEUE_SIZE | INTEGER | Displays the number of rows queued for transmission to the client. These rows have been transferred from the internal queue to the socket buffer and can be regrouped by envelopes. |
| CPU_CORE_UTILIZATION | REAL | Displays the total CPU usage for the client thread, as a percentage of a single CPU core. |
| CPU_UTILIZATION | REAL | Displays the total CPU usage for the client, as a percentage of all CPU cores on the machine. |
| CPU_SYSTEM_UTILIZATION | REAL | Displays the total systemn CPU time, in microseconds, since the creation of the client thread. |
| CPU_USER_UTILIZATION | REAL | Displays the total user CPU time, in microseconds, since the creation of the client thread. |
| TOTAL_CPU_TIME | BIGINT | Displays the total CPU time since the creation of the client, in microseconds. |
| TOTAL_CPU_SYSTEM_TIME | BIGINT | Displays the total system CPU time, in microseconds, since the creation of the client thread. |
| TOTAL_CPU_USER_TIME | BIGINT | Displays the total user CPU time, in microseconds, since the creation of the client thread. |
| CONNECT_TIME | TIMESTAMP | Displays the time the server accepts (but does not authenticate) the connection. |
| SUBSCRIBER_DURATION | BIGINT | Displays the duration of lapsed real time, in microseconds, since the creation of the client thread. |
| LAST_UPDATE_TIME | TIMESTAMP | Displays the last time statistics were updated for the subscriber. |

## Related Information

M_STREAMING_PROJECT_GD_SUBSCRIPTIONS System View [→](M_STREAMING_PROJECT_GD_SUBSCRIPTIONS-System-View.md) M_STREAMING_PROJECTS System View [→](M_STREAMING_PROJECTS-System-View.md)
