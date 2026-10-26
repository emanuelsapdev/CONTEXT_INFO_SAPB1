# 6.2.316 M_TABLE_REPLICAS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2090–2092

Provides detailed information on asynchronous/synchronous table replicas.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the replica (replication target). |
| TABLE_NAME | NVARCHAR(256) | Displays the table name of the replica (replication target). |
| TABLE_TYPE | VARCHAR(6) | Displays the replica table type: ROW/ COLUMN. |
| REPLICA_TYPE | VARCHAR(12) | Displays the replication type: ASYN CHRONOUS/SYNCHRONOUS. |
| SOURCE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the replication source. |
| SOURCE_TABLE_NAME | NVARCHAR(256) | Displays the table name of the replication source. |
| SOURCE_TABLE_TYPE | VARCHAR(6) | Displays the source table type: ROW/ COLUMN. |
| SOURCE_TABLE_VOLUME_ID | INTEGER | Displays the volume ID of the source table. |
| PART_ID | INTEGER | Displays the table partition ID:<br>• For partitioned tables, the part ID is equal to the sequential number of the partition, starting at 1.<br>• In the case of replicated tables, the part ID is 1 for the original table and subsequent part IDs are as signed to replica tables.<br>• The part ID is 0 for tables that are not partitioned.<br>• A part ID value of -1 indicates that the table schema is currently in being modified. |
| REPLICATION_STATUS | VARCHAR(8) | Displays the async replication status: ENABLED, ENABLING, or DISABLED. |
| LAST_ENABLE_TIME | TIMESTAMP | Displays the time of the last replication enablement. |
| LAST_DISABLE_TIME | TIMESTAMP | Displays the time of the last replication disablement. |
| LAST_ERROR_CODE | INTEGER | Displays the last error code. |
| LAST_ERROR_MESSAGE | NVARCHAR(5000) | Displays the last error message. |
| LAST_ERROR_TIME | TIMESTAMP | Displays the time of the last error. |
| INSERT_RECORD_COUNT | BIGINT | Displays the inserted record count. |
| UPDATE_RECORD_COUNT | BIGINT | Displays the updated record count. |
| DELETE_RECORD_COUNT | BIGINT | Displays the deleted record count. |
| INSERT_RETRY_COUNT | BIGINT | Displays the insert statement retry count. |
| UPDATE_RETRY_COUNT | BIGINT | Displays the update statement retry count. |
| DELETE_RETRY_COUNT | BIGINT | Displays the delete statement retry count. |

## Related Information

M_TABLE_REPLICAS_RESET System View [→](M_TABLE_REPLICAS_RESET-System-View.md) TABLE_REPLICAS System View [→](../6.01-System-Views/TABLE_REPLICAS-System-View.md)

ALTER SYSTEM {ENABLE | DISABLE} ALL [ASYNCHRONOUS | SYNCHRONOUS] TABLE REPLICAS Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-ENABLE-DISABLE-ALL-ASYNCHRONOUS-SYNCHRONOUS.md) ALTER TABLE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.20-ALTER-TABLE/README.md)
