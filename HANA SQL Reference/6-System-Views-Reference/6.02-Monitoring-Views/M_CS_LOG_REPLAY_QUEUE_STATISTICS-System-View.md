# 6.2.62 M_CS_LOG_REPLAY_QUEUE_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1722–1724

Provides information about column store log replay queue statistics.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the name of the host. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| LOG_REPLAY_QUEUE_ID | INTEGER | Displays the ID of the recovery queue. |
| TOTAL_CS_LOG_RECORD_COUNT | BIGINT | Displays the total number of redo records that were processed in this queue. |
| TOTAL_DML_LOG_RECORD_COUNT | BIGINT | Displays the total number of column store DML redo records that were processed in this queue. |
| TOTAL_DDL_LOG_RECORD_COUNT | BIGINT | Displays the total number of column store DDL redo records that were processed in this queue. |
| LAST_CS_LOG_RECORD_TYPE | VARCHAR(40) | Displays the last column store log record type in this queue. |
| LAST_LOG_REPLAY_POSITION | BIGINT | Displays the last log replay position that was processed in this queue. |
| LAST_SAVEPOINT_POSITION | BIGINT | Displays the last savepoint position that was passed in this queue. |
| TOTAL_SAVEPOINT_COUNT | BIGINT | Displays the total number of savepoints that were passsed in this queue. |
| ACTIVE_TABLE_COUNT | BIGINT | Displays the number of tables that are currently handled in this queue. |
| ACTIVE_DELTA_MERGE_COUNT | BIGINT | Displays the number of delta merges that are currently ongoing for tables that are handled in this queue. |
| TOTAL_DELTA_MERGE_COUNT | BIGINT | Displays the total number of delta merges that were started on this queue. |
| TOTAL_SUCCESSFUL_DELTA_MERGE_COUNT | BIGINT | Displays the total number of successful merges. |
| TOTAL_DELTA_FUSION_COUNT | BIGINT | Displays the total number of delta fusions that were made in this queue. |
| ACTIVE_OPTIMIZE_COMPRESSION_COUNT | BIGINT | Displays the number of optimize compressions that are currently ongoing for tables that are handled in this queue. |
| TOTAL_OPTIMIZE_COMPRESSION_COUNT | BIGINT | Displays the total number of successful optimize compressions. |
| TOTAL_SUCCESSFUL_OPTIMIZE_COMPRESSION_COUNT | BIGINT | Displays the total number of successful optimize compressions. |
| TOTAL_DML_CONTEXT_CREATE_COUNT | BIGINT | Displays the number of expensive creations of DML contexts. |

## Related Information

[M_CS_LOG_REPLAY_QUEUE_STATISTICS_RESET System View](M_CS_LOG_REPLAY_QUEUE_STATISTICS_RESET-System-View.md)
