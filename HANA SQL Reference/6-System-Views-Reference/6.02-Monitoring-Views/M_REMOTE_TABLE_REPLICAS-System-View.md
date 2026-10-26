# 6.2.233 M_REMOTE_TABLE_REPLICAS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1962–1964

Provides remote table replication information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistent volume ID of the server. |
| IS_SOURCE_SYSTEM | VARCHAR(5) | Indicates whether or not the system has a source table: TRUE/FALSE. |
| REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name on the replication system. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the replication table. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name of the replication table. |
| TABLE_OID | BIGINT | Displays the Table OID of the replication table. |
| TABLE_TYPE | VARCHAR(16) | Displays the type of replication table: ROW/COLUMN. |
| REPLICA_TYPE | VARCHAR(12) | Displays the replication type: SYN CHRONOUS/ASYNCHRONOUS. |
| SOURCE_REMOTE_SOURCE_NAME | NVARCHAR(256) | Displays the remote source name on the source system. |
| SOURCE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the source table. |
| SOURCE_TABLE_NAME | NVARCHAR(256) | Displays the table name of the source table. |
| SOURCE_TABLE_OID | BIGINT | Displays the table OID of a source table. |
| SOURCE_TABLE_TYPE | VARCHAR(6) | Displays the source table type: ROW/ COLUMN. |
| PART_ID | INTEGER | Displays the partition ID. Returns the following:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that a modification of the table schema is in progress. |
| REPLICATION_STATUS | VARCHAR(16) | Displays the replication status: ENA BLING, ENABLED, or DISABLED. |
| LAST_ENABLE_TIME | TIMESTAMP | Displays the timestamp when the table was last enabled. |
| LAST_DISABLE_TIME | TIMESTAMP | Displays the timestamp when the table was last disabled. |
| LAST_ERROR_CODE | INTEGER | Displays the last error code number. |
| LAST_ERROR_MESSAGE | NVARCHAR(5000) | Displays the last error message. |
| LAST_ERROR_TIME | TIMESTAMP | Displays the timestamp when the last error occurred. |
| INSERT_RECORD_COUNT | BIGINT | Displays the number of inserted records. |
| UPDATE_RECORD_COUNT | BIGINT | Displays the number of updated records. |
| DELETE_RECORD_COUNT | BIGINT | Displays the number of deleted records. |
| INSERT_RETRY_COUNT | BIGINT | Displays the number of retries to insert. |
| UPDATE_RETRY_COUNT | BIGINT | Displays the number of retries to up date. |
| DELETE_RETRY_COUNT | BIGINT | Displays the number of retries to delete. |
