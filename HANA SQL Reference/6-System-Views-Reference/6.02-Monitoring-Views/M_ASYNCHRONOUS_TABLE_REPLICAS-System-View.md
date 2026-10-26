# 6.2.12 M_ASYNCHRONOUS_TABLE_REPLICAS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1651–1652

Provides detailed information about asynchronous table replicas. Deprecated.

This view has a resettable counterpart. This means you can also see the values since the last reset in the dependent view M_ASYNCHRONOUS_TABLE_REPLICAS_RESET. To reset the values, use the SQL command: ALTER SYSTEM RESET MONITORING VIEW SYS.M_ASYNCHRONOUS_TABLE_REPLICAS_RESET

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Host name |
| PORT | INTEGER | Internal port |
| VOLUME_ID | INTEGER | Persistence Volume ID |
| SCHEMA_NAME | NVARCHAR(256) | Schema name of replica (replication target) |
| TABLE_NAME | NVARCHAR(256) | Table name of replica (replication tar get) |
| TABLE_TYPE | VARCHAR(6) | Replica table type: ROW, COLUMN |
| SOURCE_SCHEMA_NAME | NVARCHAR(256) | Schema name of replication source |
| SOURCE_TABLE_NAME | NVARCHAR(256) | Table name of replication source |
| SOURCE_TABLE_TYPE | VARCHAR(6) | Source Table type: ROW, COLUMN |
| SOURCE_TABLE_VOLUME_ID | INTEGER | Volume ID of its source table |
| PART_ID | INTEGER | Partition ID. 0 for non-partitioned tables, 1 through number of partitions for partitioned tables |
| REPLICATION_STATUS | VARCHAR(8) | Current asynchronous replication status: ENABLED, ENABLING, DISABLED |
| LAST_ENABLE_TIME | TIMESTAMP | Time of last replication enable |
| LAST_DISABLE_TIME | TIMESTAMP | Time of last replication disable |
| LAST_ERROR_CODE | INTEGER | Last error code |
| LAST_ERROR_MESSAGE | NVARCHAR(5000) | Last error message |
| LAST_ERROR_TIME | TIMESTAMP | Time of the last error |
| INSERT_RECORD_COUNT | BIGINT | Inserted record count |
| UPDATE_RECORD_COUNT | BIGINT | Updated record count |
| DELETE_RECORD_COUNT | BIGINT | Deleted record count |
| INSERT_RETRY_COUNT | BIGINT | Insert statement retry count |
| UPDATE_RETRY_COUNT | BIGINT | Update statement retry count |
| DELETE_RETRY_COUNT | BIGINT | Delete statement retry count |
