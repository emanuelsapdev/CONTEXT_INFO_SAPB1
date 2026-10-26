# 6.2.75 M_DATABASE_REPLICA_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1740–1742

Provides statistics on databases involved in replication.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SOURCE_DATABASE_NAME | NVARCHAR(256) | Displays the name of the source data base. |
| SOURCE_HOST | VARCHAR(64) | Displays the source host name. |
| SOURCE_PORT | INTEGER | Displays the source internal port. |
| SOURCE_VOLUME_ID | INTEGER | Displays the source volume ID. |
| TARGET_DATABASE_NAME | NVARCHAR(256) | Displays the name of the target data base. |
| TARGET_HOST | VARCHAR(64) | Displays the target host name. |
| TARGET_PORT | INTEGER | Displays the target port. |
| TARGET_ACTIVE_STATUS | VARCHAR(16) | Displays the target active status. |
| TARGET_CONNECT_TIME | TIMESTAMP | Displays the time that the connection was established from the target. |
| TARGET_RECONNECT_TIME | INTEGER | Displays the target reconnect count. |
| TARGET_FAILOVER_COUNT | INTEGER | Displays the target failover count. |
| TARGET_FULLY_RECOVERABLE | VARCHAR(5) | Indicates if the target is fully recoverable. |
| REPLICATION_MODE | VARCHAR(16) | Displays the replication mode. |
| REPLICATION_STATUS | VARCHAR(16) | Displays the replication status. |
| REPLICATION_STATUS_DETAILS | VARCHAR(1024) | Displays the replication status details. |
| LAST_LOG_POSITION | BIGINT | Displays the current log position. |
| LAST_LOG_POSITION_TIME | TIMESTAMP | Displays the current log position time stamp. |
| SHIPPED_LOG_POSITION | BIGINT | Displays the shipped log position. |
| SHIPPED_LOG_POSITION_TIME | TIMESTAMP | Displays the shipped log position time stamp. |
| SHIPPED_LOG_BUFFERS_COUNT | BIGINT | Displays the shipped log buffers count. |
| SHIPPED_LOG_BUFFERS_SIZE | BIGINT | Displays the shipped log buffers size in bytes. |
| SHIPPED_LOG_BUFFERS_DURATION | BIGINT | Displays the shipped log buffer duration in microseconds. |
| ASYNC_BUFFER_FULL_COUNT | BIGINT | Displays the number of times the asynchronous replication buffer got full. |
| BACKLOG_SIZE | BIGINT | Displays the current replication backlog in bytes. |
| MAX_BACKLOG_SIZE | BIGINT | Displays the max replication backlog in bytes. |
| BACKLOG_TIME | BIGINT | Displays the current replication backlog in microseconds. |
| MAX_BACKLOG_TIME | BIGINT | Displays the max replication backlog in microseconds. |

## Related Information

M_DATABASE_REPLICAS System View [→](M_DATABASE_REPLICAS-System-View.md) M_DATABASE System View [→](M_DATABASE-System-View.md) M_DATABASES System View [→](M_DATABASES-System-View.md) M_DATABASE_HISTORY System View [→](M_DATABASE_HISTORY-System-View.md) CREATE DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-DATABASE-Statement-Tenant-Database-Management.md) ALTER DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ALTER-DATABASE-Statement-Tenant-Database-Management.md) RENAME DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/RENAME-DATABASE-Statement-Tenant-Database-Management.md) DROP DATABASE Statement (Tenant Database Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-DATABASE-Statement-Tenant-Database-Management.md)
