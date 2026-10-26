# 6.2.259 M_SERVICE_REPLICATION System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1993–1997

Provides information about replicated services.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER(10) | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the volume ID. |
| SITE_ID | INTEGER | Displays the generated site ID. |
| SITE_NAME | VARCHAR(256) | Displays the logical site name. |
| SECONDARY_HOST | VARCHAR(64) | Displays the secondary host name. |
| SECONDARY_PORT | INTEGER | Displays the secondary port. |
| SECONDARY_SITE_ID | INTEGER | Displays the generated ID of the secondary site. |
| SECONDARY_SITE_NAME | VARCHAR(256) | Displays the secondary logical site name. |
| SECONDARY_ACTIVE_STATUS | VARCHAR(16) | Displays the secondary active status. |
| SECONDARY_CONNECT_TIME | TIMESTAMP | Displays the time the connection was established from the secondary site. |
| SECONDARY_RECONNECT_COUNT | INTEGER | Displays the secondary reconnect count. |
| SECONDARY_FAILOVER_COUNT | INTEGER | Displays the secondary failover count. |
| SECONDARY_FULLY_RECOVERABLE | VARCHAR(5) | Displays that the secondary system can be fully recovered with a backup from the primary system.<br>If this value is FALSE, then the backup history is broken. If there is a takeover at that time, then start a new data backup once the takeover is finished. |
| REPLICATION_MODE | VARCHAR(16) | Displays the replication mode. |
| REPLICATION_STATUS | VARCHAR(16) | Displays the replication status. |
| REPLICATION_STATUS_DETAILS | VARCHAR(1.024) | Displays the replication status details. |
| FULL_SYNC | VARCHAR(16) | Displays the full sync status:<br>• DISABLED: the full sync is not configured<br>• ENABLED: the full sync is configured, but it is not yet active (trans actions do not block in this state)<br>• ACTIVE: the full sync mode is configured and active |
| LAST_LOG_POSITION | BIGINT | Displays the current log position. |
| LAST_LOG_POSITION_TIME | TIMESTAMP | Displays the current log position time stamp. |
| LAST_SAVEPOINT_VERSION | INTEGER | Displays the current savepoint version. |
| LAST_SAVEPOINT_LOG_POSITION | BIGINT(19) | Displays the current savepoint log position. |
| LAST_SAVEPOINT_START_TIME | TIMESTAMP | Displays the current savepoint time stamp. |
| SHIPPED_LOG_POSITION | BIGINT | Displays the shipped log positon. |
| SHIPPED_LOG_POSITION_TIME | TIMESTAMP | Displays the shipped log position time stamp. |
| SHIPPED_LOG_BUFFERS_COUNT | BIGINT | Displays the shipped log buffers count. |
| SHIPPED_LOG_BUFFERS_SIZE | BIGINT | Displays the shipped log buffers size in bytes. |
| SHIPPED_LOG_BUFFERS_DURATION | BIGINT | Displays the shipped log buffer duration in microseconds. |
| REPLAYED_LOG_POSITION | BIGINT | Displays the log end position of the last known replayed log buffer on the secondary site. |
| REPLAYED_LOG_POSITION_TIME | TIMESTAMP | Displays the timestamp of the last known replayed log buffer on the secondary site. |
| SHIPPED_SAVEPOINT_VERSION | INTEGER | Displays the shipped savepoint version. |
| SHIPPED_SAVEPOINT_LOG_POSITION | BIGINT | Displays the shipped savepoint log position. |
| SHIPPED_SAVEPOINT_START_TIME | TIMESTAMP | Displays the shipped savepoint start time. |
| SHIPPED_FULL_REPLICA_COUNT | BIGINT | Displays the shipped full replica count. |
| SHIPPED_FULL_REPLICA_SIZE | BIGINT | Displays the shipped full replica size in bytes. |
| SHIPPED_FULL_REPLICA_DURATION | BIGINT | Displays the shipped full replica duration in microseconds. |
| SHIPPED_LAST_FULL_REPLICA_SIZE | BIGINT | Displays the shipped last full replica size in bytes. |
| SHIPPED_LAST_FULL_REPLICA_START_TIME | TIMESTAMP | Displays the shipped last full replica start time. |
| SHIPPED_LAST_FULL_REPLICA_END_TIME | TIMESTAMP | Displays the shipped last full replica end time. |
| SHIPPED_DELTA_REPLICA_COUNT | BIGINT | Displays the shipped delta replica count. |
| SHIPPED_DELTA_REPLICA_SIZE | BIGINT | Displays the shipped delta replica size in bytes. |
| SHIPPED_DELTA_REPLICA_DURATION | BIGINT | Displays the shipped delta replica duration in microseconds. |
| SHIPPED_LAST_DELTA_REPLICA_SIZE | BIGINT | Displays the shipped last delta replica size in bytes. |
| SHIPPED_LAST_DELTA_REPLICA_START_TIME | TIMESTAMP | Displays the shipped last delta replica start time. |
| SHIPPED_LAST_DELTA_REPLICA_END_TIME | TIMESTAMP | Displays the shipped last delta replica end time. |
| ASYNC_BUFFER_FULL_COUNT | BIGINT | Displays the number of times the asynchronous replication buffer was full. |
| BACKLOG_SIZE | BIGINT | Displays the current replication backlog in bytes. |
| MAX_BACKLOG_SIZE | BIGINT | Displays the maximum replication backlog in bytes. |
| BACKLOG_TIME | BIGINT | Displays the current replication backlog in microseconds. |
| MAX_BACKLOG_TIME | BIGINT | Displays the maximum replication backlog in microseconds. |
| REPLAY_BACKLOG_SIZE | BIGINT | Displays the size, in bytes, of all log buffers that have been shipped to the secondary site but have not yet been replayed on the scondary site. |
| MAX_REPLAY_BACKLOG_SIZE | BIGINT | Displays the maximumsize, in bytes, of the REPLAY_BACKLOG_SIZE since the system startup. |
| REPLAY_BACKLOG_TIME | BIGINT | Displays the time difference, in microseconds, between the time of the last shipped log buffer and the last replayed log buffer on the secondary site. |
| MAX_REPLAY_BACKLOG_TIME | BIGINT | Displays the maximum time, in microseconds, of the REPLAY_BACKLOG_TIME since the system startup. |
