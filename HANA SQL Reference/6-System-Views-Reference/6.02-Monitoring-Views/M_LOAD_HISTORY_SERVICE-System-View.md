# 6.2.162 M_LOAD_HISTORY_SERVICE System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1874–1878

Lists servicespecific load history KPIs.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| TIME | TIMESTAMP | Displays the KPI collection timestamp. |
| CPU | BIGINT | Displays the percent of CPU used by the service. |
| SYSTEM_CPU | BIGINT | Displays the percent of OS Kernel/ System CPU used by the service. |
| MEMORY_USED | BIGINT | Displays the memory used by the service in bytes. |
| MEMORY_ALLOCATION_LIMIT | BIGINT | Displays the memory allocation limit for the service in bytes. |
| HANDLE_COUNT | BIGINT | Displays the number of open handles. |
| PING_TIME | BIGINT | Displays the duration, in microseconds, of the service ping request (THREAD_METHOD=__nsWatchdog). This request includes the time it takes to measure the values shown in this view. |
| SWAP_IN | BIGINT | Displays the bytes read from the swap by the service (column 12(majflt) in / proc/`<pid>`/stat \* sysconf(_SC_PAGESIZE)). |
| CONNECTION_COUNT | BIGINT | Displays the number of open SQL connections. |
| INTERNAL_CONNECTION_COUNT | BIGINT | Displays the number of open SQL internal connections. |
| EXTERNAL_CONNECTION_COUNT | BIGINT | Displays the number of open SQL external connections. |
| IDLE_CONNECTION_COUNT | BIGINT | Displays the number of open SQL idle connections. |
| TRANSACTION_COUNT | BIGINT | Displays the number of open SQL transactions. |
| INTERNAL_TRANSACTION_COUNT | BIGINT | Displays the number of internal trans actions. |
| EXTERNAL_TRANSACTION_COUNT | BIGINT | Displays the number of external trans actions. |
| USER_TRANSACTION_COUNT | BIGINT | Displays the number of user transactions. |
| BLOCKED_TRANSACTION_COUNT | BIGINT | Displays the number of blocked SQL transactions. |
| STATEMENT_COUNT | BIGINT | Displays the number of finished SQL statements. |
| COMMIT_ID_RANGE | BIGINT | Displays the range between the newest and oldest active commit IDs. |
| MVCC_VERSION_COUNT | BIGINT | Displays the number of active MVCC versions. |
| PENDING_SESSION_COUNT | BIGINT | Displays the number of pending requests. |
| RECORD_LOCK_COUNT | BIGINT | Displays the number of acquired record locks. |
| CS_READ_COUNT | BIGINT | Displays the number of read requests (SELECT). |
| CS_WRITE_COUNT | BIGINT | Displays the number of write requests (INSERT, UPDATE, DELETE). |
| CS_MERGE_COUNT | BIGINT | Displays the number of merge requests. |
| CS_UNLOAD_COUNT | BIGINT | Displays the number of column un loads. |
| ACTIVE_THREAD_COUNT | BIGINT | Displays the number of active threads. |
| WAITING_THREAD_COUNT | BIGINT | Displays the number of waiting threads. |
| TOTAL_THREAD_COUNT | BIGINT | Displays the total number of threads. |
| ACTIVE_SQL_EXECUTOR_COUNT | BIGINT | Displays the number of active SQLExe cutors. |
| WAITING_SQL_EXECUTOR_COUNT | BIGINT | Displays the number of waiting SQLEx ecutors. |
| TOTAL_SQL_EXECUTOR_COUNT | BIGINT | Displays the total number of SQLExecu tors. |
| DATA_WRITE_SIZE | BIGINT | Displays the bytes written to the data area. |
| DATA_WRITE_TIME | BIGINT | Displays the time used for writing to the data area in microseconds. |
| LOG_WRITE_SIZE | BIGINT | Displays the bytes written to the log area. |
| LOG_WRITE_TIME | BIGINT | Displays the time used for writing to the log area in microseconds. |
| DATA_READ_SIZE | BIGINT | Displays the bytes read from the data area. |
| DATA_READ_TIME | BIGINT | Displays the time used for reading from the data area in microseconds. |
| LOG_READ_SIZE | BIGINT | Displays the bytes read from the log area. |
| LOG_READ_TIME | BIGINT | Displays the time used for reading from the log area in microseconds. |
| DATA_BACKUP_WRITE_SIZE | BIGINT | Displays the bytes written to the data backup. |
| DATA_BACKUP_WRITE_TIME | BIGINT | Displays the time used for writing to the data backup in microseconds. |
| LOG_BACKUP_WRITE_SIZE | BIGINT | Displays the bytes written to the log backup. |
| LOG_BACKUP_WRITE_TIME | BIGINT | The time used for writing to the log backup. |
| MUTEX_COLLISION_COUNT | BIGINT | Displays the number of collisions on mutexes. |
| READ_WRITE_LOCK_COLLISION_COUNT | BIGINT | Displays the number of collisions on read/write locks. |
| ADMISSION_CONTROL_ADMIT_COUNT | BIGINT | Displays the number of admission requests admitted by admission control. |
| ADMISSION_CONTROL_REJECT_COUNT | BIGINT | Displays the number of session requests rejected by admission control. |
| ADMISSION_CONTROL_QUEUE_SIZE | BIGINT | Displays the number of session requests waiting in the admission control queue. |
| ADMISSION_CONTROL_WAIT_TIME | BIGINT | Displays the total wait time of the session requests queued in the admission control queue in microseconds. |

## Related Information

[M_LOAD_HISTORY_HOST System View](M_LOAD_HISTORY_HOST-System-View.md)

M_LOAD_HISTORY_INFO System View [→](M_LOAD_HISTORY_INFO-System-View.md) LOAD Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/LOAD-Statement-Data-Manipulation.md) PERSISTENCE_HISTORY System View [→](../6.01-System-Views/PERSISTENCE_HISTORY-System-View.md)
