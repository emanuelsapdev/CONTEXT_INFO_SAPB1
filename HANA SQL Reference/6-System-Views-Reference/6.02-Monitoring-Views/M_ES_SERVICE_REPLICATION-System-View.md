# 6.2.105 M_ES_SERVICE_REPLICATION System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1782–1784

Provides extended storage service replication information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| STORE_NAME | VARCHAR(256) | Displays the name of the store. |
| SECONDARY_CONNECT_TIME | TIMESTAMP | Displays the time that the connection was established on the secondary. |
| SECONDARY_RECONNECT_COUNT | INTEGER | Displays the secondary reconnect count. |
| SECONDARY_FAILOVER_COUNT | INTEGER | Displays the secondary failover count. |
| SECONDARY_FULLY_RECOVERABLE | VARCHAR(5) | Indicates whether or not the secondary if fully recoverable. |
| REPLICATION_MODE | VARCHAR(16) | Displays the replication mode. |
| REPLICATION_STATUS | VARCHAR(16) | Displays the replication status. |
| REPLICATION_STATUS_DETAILS | VARCHAR(1024) | Displays the replication status details. |
| FULL_SYNC | VARCHAR(16) | Displays the Replication Full sync status. |
| LAST_LOG_POSITION | BIGINT | Displays the last log position. |
| LAST_LOG_POSITION_TIME | TIMESTAMP | Displays the last log position time stamp. |
| SHIPPED_LOG_POSITION | BIGINT | Displays the shipped log position. |
| SHIPPED_LOG_POSITION_TIME | TIMESTAMP | Displays the shipped log position time stamp. |
| SHIPPED_LOG_BUFFERS_COUNT | BIGINT | Displays the shipped log buffers count. |
| SHIPPED_LOG_BUFFERS_SIZE | BIGINT | Displays the shipped log buffers size in bytes. |
| SHIPPED_LOG_BUFFERS_DURATION | BIGINT | Displays the shipped log buffer duration in microseconds. |
| REPLAYED_LOG_POSITION | BIGINT | Displays the log end position of the last known replayed log buffer on the secondary site. |
| REPLAYED_LOG_POSITION_TIME | TIMESTAMP | Displays the timestamp of the last known replayed log buffer on the secondary site. |
| SHIPPED_FULL_REPLICA_COUNT | BIGINT | Displays the full shipped replica count. |
| SHIPPED_FULL_REPLICA_SIZE | BIGINT | Displays the full shipped replica size in bytes. |
| SHIPPED_FULL_REPLICA_DURATION | BIGINT | Displays the full shipped replica duration in microseconds. |
| SHIPPED_LAST_FULL_REPLICA_SIZE | BIGINT | Displays the last full shipped replica size in bytes. |
| SHIPPED_LAST_FULL_REPLICA_START_TIME | TIMESTAMP | Displays the last full shipped replica start time. |
| SHIPPED_LAST_FULL_REPLICA_END_TIME | TIMESTAMP | Displays the last full shipped replica end time. |
| ASYNC_BUFFER_FULL_COUNT | BIGINT | Displays the number of times that the asynchronous replication buffer was full. |
| BACKLOG_SIZE | BIGINT | Displays the replication backlog in bytes. |
| BACKLOG_TIME | BIGINT | Displays the replication backlog in microseconds. |
| MAX_BACKLOG_SIZE | BIGINT | Displays the max replication backlog in bytes. |
| MAX_BACKLOG_TIME | BIGINT | Displays the max replication backlog in microseconds. |

## Related Information

[M_SERVICE_REPLICATION System View](M_SERVICE_REPLICATION-System-View.md)
