# 6.2.261 M_SERVICE_THREADS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1999–2002

Displays detailed information about threads created by services.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SERVICE_NAME | VARCHAR(32) | Displays the service name. See M_SERVICE_TYPES for all known service names. |
| HIERARCHY | VARCHAR(128) | Displays the thread grouping information. This column contains the connection ID, the update transaction ID, and the transaction ID. The column is empty if the threads are inactive. |
| CONNECTION_ID | INTEGER | Displays the connection ID. |
| THREAD_ID | BIGINT | Displays the thread ID. |
| THREAD_TYPE | VARCHAR(128) | Displays the thread type. |
| THREAD_METHOD | VARCHAR(256) | Displays the thread method. |
| THREAD_DETAIL | NCLOB | Displays the thread detail. |
| THREAD_STATE | VARCHAR(32) | Displays the thread state. |
| IS_ACTIVE | VARCHAR(5) | Displays whether the thread is active. |
| DURATION | BIGINT | Displays the thread duration in milliseconds. |
| CALLER | VARCHAR(256) | Displays the service that called the thread. |
| CALLING | VARCHAR(256) | Displays the service called by the thread. |
| STATEMENT_ID | VARCHAR(20) | Displays the ID of the statement being executed. |
| STATEMENT_HASH | VARCHAR(32) | Displays the MD5 hash value for STATEMENT_STRING. |
| ROOT_STATEMENT_ID | VARCHAR(20) | Displays the ID of the root statement being executed. |
| ROOT_STATEMENT_HASH | VARCHAR(32) | Displays the MD5 hash value for the root statement string. |
| USER_NAME | NVARCHAR(256) | Displays the SQL user name. |
| APPLICATION_NAME | NVARCHAR(256) | Displays the name of the application. |
| APPLICATION_USER_NAME | NVARCHAR(256) | Displays the application user name. |
| APPLICATION_SOURCE | NVARCHAR(256) | Displays that the application can define which source file SAP HANA is called from. This value is also displayed in the M_PREPARED_STATEMENTS.APPLICATION_SOURCE system view. |
| CPU_TIME_SELF | BIGINT | Displays the active CPU time of the thread in microseconds. |
| CPU_TIME_CUMULATIVE | BIGINT | Displays the active CPU time of the thread and its associated children in microseconds. |
| CLIENT_IP | VARCHAR(45) | Displays the IP of the client machine. |
| CLIENT_PID | BIGINT | Displays the client process ID. |
| STATEMENT_EXECUTION_ID | BIGINT | Displays the statement execution ID. |
| TRANSACTION_ID | INTEGER | Displays the transaction ID. |
| UPDATE_TRANSACTION_ID | BIGINT | Displays the update transaction ID. |
| LOCK_WAIT_COMPONENT | VARCHAR(32) | Displays the component assigned to the lock. |
| LOCK_WAIT_NAME | VARCHAR(128) | Displays the internal name of the lock (can be joined with the STATISTICS_NAME column from, for example, M_MUTEXES). |
| LOCK_OWNER_THREAD_ID | BIGINT | Displays the ID of the thread that is holding the lock. |
| LOCKS_OWNED | VARCHAR(256) | Displays the locks currently owned by the thread, including the lock type (shared/exclusive). This column does not show all locks that are monitored. |
| PRIORITY | INTEGER | Displays the statement priority. |
| STATEMENT_THREAD_LIMIT | INTEGER | Displays the statement thread limit. |
| STATEMENT_MEMORY_LIMIT | INTEGER | Displays the statement memory limit. |
| PASSPORT_ROOTCONTEXT_ID | VARBINARY(16) | Displays the passport root context ID. |
| PASSPORT_TRANSACTION_ID | NVARCHAR(32) | Displays the passport transaction ID. |
| PASSPORT_CONNECTION_ID | VARBINARY(16) | Displays the passport connection ID. |
| PASSPORT_CONNECTION_COUNTER | BIGINT | Displays the passport connection counter. |
| PASSPORT_COMPONENT_NAME | NVARCHAR(32) | Displays the passport component name. |
| PASSPORT_ACTION | NVARCHAR(40) | Displays the passport action. |
| NUMA_NODE_INDEX | SMALLINT | Displays the last known NUMA node that the thread was executed on. |

## Additional Information

While this view is publicly visible, its contents can only be seen by users with the DATABASE ADMIN privilege.

## Related Information

M_SERVICE_THREAD_CALLSTACKS System View [→](M_SERVICE_THREAD_CALLSTACKS-System-View.md) M_SERVICE_THREAD_SAMPLES System View [→](M_SERVICE_THREAD_SAMPLES-System-View.md)
