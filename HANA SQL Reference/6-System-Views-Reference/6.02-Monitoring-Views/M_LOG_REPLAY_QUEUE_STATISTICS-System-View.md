# 6.2.168 M_LOG_REPLAY_QUEUE_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1886

Provides information about log replay queue statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the name of the host. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| LOG_REPLAY_QUEUE_ID | INTEGER | Displays the ID of the log replay queue. |
| LOG_RECORD_TYPE | VARCHAR(40) | Displays the type of redo log record. |
| TOTAL_LOG_RECORD_COUNT | BIGINT | Displays the total number of replayed log entries. |
| TOTAL_EXECUTION_TIME | BIGINT | Displays the accumulated execute time to replay log entries in microseconds. |
| TOTAL_WAIT_TIME | BIGINT | Displays the accumulated local wait time during replay of log entries in microseconds. |
| TOTAL_LOG_RECORD_SIZE | BIGINT | Displays the accumulated log size of replayed log entries. |

## Related Information

[M_LOG_REPLAY_QUEUE_STATISTICS_RESET System View](M_LOG_REPLAY_QUEUE_STATISTICS_RESET-System-View.md)
