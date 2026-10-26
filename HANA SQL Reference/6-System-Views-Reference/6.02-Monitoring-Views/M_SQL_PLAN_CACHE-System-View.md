# 6.2.275 M_SQL_PLAN_CACHE System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2019–2028

Provides statistics for an individual execution plan.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| STATEMENT_STRING | NCLOB | Displays the statement string. |
| STATEMENT_HASH | VARCHAR(32) | Displays the MD5 hash value for the STATEMENT_STRING column. |
| USER_NAME | NVARCHAR(256) | Displays the user name who prepared the plan. |
| SESSION_USER_NAME | NVARCHAR(256) | Displays the session user name who prepared the plan. This is the same value appears for USER_NAME in the M_CONNECTIONS.USER monitoring view. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name that the SQL plan belongs to. SQL plans are generated in each schema even though the statement string is the same, since the query optimizer statistics might be different. |
| SESSION_PROPERTIES | NVARCHAR(500) | Displays the composed variables from the session context. |
| IS_VALID | VARCHAR(5) | Displays whether a plan is currently validated (TRUE/FALSE). A plan is invalidated when its corresponding schema objects, such as table and view, are changed. Invalidated plans are recompiled if the same statement is executed; otherwise, they are evicted by another plan when newly compiled. |
| LAST_INVALIDATION_REASON | VARCHAR(64) | Displays the reason for the last invalidation. |
| IS_INTERNAL | VARCHAR(5) | Displays TRUE if the query plan was initiated from a database internal connection, not from the user nor other servers. For example, when an internal SAP HANA component executes a SQL statement related to the Statistics Service (_SYS_STATISTICS), or runs SQL statements in a background thread that exploit SQL Plan Cache, and so on.<br>Displays FALSE if the query plan was initiated by a client application. |
| IS_DISTRIBUTED_EXECUTION | VARCHAR(5) | Displays whether tables are located in multiple nodes or multiple services are involved in plan execution (TRUE/ FALSE). |
| COMPILATION_OPTIONS | VARCHAR(128) | Displays the compilation options that are used by the SQL Query Optimizer when it generates cached execution plans:<br>• Returns an empty string if the SQL Query Optimizer compiled without any special settings<br>• Returns a STATEMENT HINT option when the SQL Query Optimizer compiles and optimizes with a statement hint<br>• Returns an ABSTRACT SQL PLAN option when the SQL Query Optimizer compiles with an abstract sql plan<br>Multiple options can used together to create a list of options, for example: STATEMENT HINT, ABSTRACT SQL PLAN. |
| IS_PINNED_PLAN | VARCHAR(5) | Displays whether the plan is explicitly stored by the PlanViz utility (TRUE/ FALSE). |
| PINNED_PLAN_ID | VARCHAR(5) | This is deprecated. |
| ABAP_VARCHAR_MODE | VARCHAR(5) | Displays whether the ABAP VARCHAR mode is enabled (TRUE/FALSE). Only ABAP application developers are concerned with this mode, which indicates if it is a NULL terminated string or not. |
| APPLICATION_NAME | NVARCHAR(256) | Displays the application name information. |
| APPLICATION_SOURCE | NVARCHAR(256) | Displays the application source information. |
| ACCESSED_TABLES | VARCHAR(5000) | Displays the relevant base table ID list accessed in the plan. The format is ( ) for a list entry, with entries separated by commas. |
| ACCESSED_TABLE_NAMES | NCLOB | Displays the relevant base table name list accessed in the plan. The format is ( ) for a list entry, with entries separated by commas. |
| ACCESSED_OBJECTS | VARCHAR(5000) | Displays the relevant schema object ID list accessed in the plan. The format is ( ) for a list entry, with entries separated by commas. |
| ACCESSED_OBJECT_NAMES | NCLOB | Displays the relevant schema object name list accessed in the plan. The format is ( ) for a list entry, with entries separated by commas. |
| TABLE_LOCATIONS | VARCHAR(2000) | Displays all relevant table locations for both original and replicated tables.<br>The table location contains the host, port, database ID, and volume ID, for example `lddbqm0:30240, 0, 3`. |
| TABLE_TYPES | VARCHAR(128) | Displays whether the plan refers to the column store only, row store only, or mixed. Possible values are: ROW, COL UMN, or ROW, COLUMN. |
| PLAN_SHARING_TYPE | VARCHAR(128) | Displays the plan sharing type: GLOBAL, SESSION EXCLUSIVE GLOBAL, SESSION LOCAL, or LOGICAL SESSION GLOBAL.<br>See below for definitions. |
| OWNER_CONNECTION_ID | INTEGER | Displays the connection owning the plan. |
| PLAN_ID | BIGINT | Displays the logical plan ID, which is anon-negative value. |
| PLAN_MEMORY_SIZE | BIGINT | Displays the memory size used by the plan in bytes. |
| REFERENCE_COUNT | BIGINT | Displays the number of statements using the plan. When the number reaches zero, it can be evicted by the victim selection policy of the plan cache. |
| PARAMETER_COUNT | BIGINT | Displays the number of parameters as signed to the execution. |
| UPDATED_TABLE_OID | BIGINT | Displays the object ID of the updated table for the plan. |
| LOGICAL_CONNECTION_VOLUME_ID | BIGINT | Displays the volume ID of the logical connection. This value is 0 if there is no session context defining it as a global plan. |
| EXECUTION_COUNT | BIGINT | Displays the accumulated count of the plan execution. |
| EXECUTION_COUNT_BY_ROUTING | BIGINT | Displays the accumulated count of the plan execution by a client-routed connection in the statement routing. This column shows how many times the statement is executed in the routed connection. The routed connection is a physical connection in a part of the logical session. |
| TOTAL_CURSOR_DURATION | BIGINT | Displays the sum of time of the plan execution in microseconds, including the communication time with clients. |
| AVG_CURSOR_DURATION | BIGINT | Displays the average time of the plan execution in microseconds, including the communication time with clients. |
| MIN_CURSOR_DURATION | BIGINT | Displays the minimum time of the plan execution in microseconds, including the communication time with clients. |
| MAX_CURSOR_DURATION | BIGINT | Displays the maximum time of the plan execution in microseconds, including the communication time with clients. |
| TOTAL_EXECUTION_TIME | BIGINT | Displays the sum of time of the plan executions in microseconds. |
| AVG_EXECUTION_TIME | BIGINT | Displays the average time of the plan execution in microseconds. |
| MIN_EXECUTION_TIME | BIGINT | Displays the minimum time of the plan execution in microseconds. |
| MAX_EXECUTION_TIME | BIGINT | Displays the maximum time of the plan execution in microseconds. |
| TOTAL_EXECUTION_OPEN_TIME | BIGINT | Displays the sum of time in microseconds establishing result sets. |
| AVG_EXECUTION_OPEN_TIME | BIGINT | Displays the average time that the cursor is open in microseconds. |
| MIN_EXECUTION_OPEN_TIME | BIGINT | Displays the minimum time for cursor open in microseconds. |
| MAX_EXECUTION_OPEN_TIME | BIGINT | Displays the maximum time for cursor open in microseconds. |
| TOTAL_EXECUTION_FETCH_TIME | BIGINT | Displays the sum of time for transfer ring rows in microseconds. |
| AVG_EXECUTION_FETCH_TIME | BIGINT | Displays the average time for cursor fetch in microseconds. |
| MIN_EXECUTION_FETCH_TIME | BIGINT | Displays the minimum time for cursor fetch in microseconds. |
| MAX_EXECUTION_FETCH_TIME | BIGINT | Displays the maximum time for cursor fetch in microseconds. |
| TOTAL_EXECUTION_CLOSE_TIME | BIGINT | Displays the sum of time for result set cleanup in microseconds. |
| AVG_EXECUTION_CLOSE_TIME | BIGINT | Displays the average time for cursor close in microseconds. |
| MIN_EXECUTION_CLOSE_TIME | BIGINT | Displays the minimum time for cursor close in microseconds. |
| MAX_EXECUTION_CLOSE_TIME | BIGINT | Displays the maximum time for cursor close in microseconds. |
| TOTAL_METADATA_CACHE_MISS_COUNT | BIGINT | Deprecated. |
| TOTAL_TABLE_LOAD_TIME_DURING_PREPARATION | BIGINT | Displays the sum of the table loading time during plan preparation in microseconds. |
| AVG_TABLE_LOAD_TIME_DURING_PREPARATION | BIGINT | Displays the average table loading time during plan preparation in microseconds. |
| MIN_TABLE_LOAD_TIME_DURING_PREPARATION | BIGINT | Displays the minimum table loading time during plan preparation in microseconds. |
| MAX_TABLE_LOAD_TIME_DURING_PREPARATION | BIGINT | Displays the maximum table loading time during plan preparation in microseconds. |
| PREPARATION_COUNT | BIGINT | Displays the number of plan preparations. |
| TOTAL_PREPARATION_TIME | BIGINT | Displays the sum of time of the plan preparation in microseconds. |
| AVG_PREPARATION_TIME | BIGINT | Displays the average time of the plan preparation in microseconds. |
| MIN_PREPARATION_TIME | BIGINT | Displays the minimum time of the plan preparation in microseconds. |
| MAX_PREPARATION_TIME | BIGINT | Displays the maximum time of the plan preparation in microseconds. |
| TOTAL_RESULT_RECORD_COUNT | BIGINT | Displays the accumulated number of records during plan execution. |
| TOTAL_LOCK_WAIT_COUNT | BIGINT | Displays the accumulated lock wait count for the plan. |
| TOTAL_LOCK_WAIT_DURATION | BIGINT | Displays the accumulated lock wait duration for the plan in microseconds. |
| LAST_CONNECTION_ID | INTEGER | Displays the last connection ID that executed the plan. |
| LAST_EXECUTION_TIMESTAMP | TIMESTAMP | Displays the last execution timestamp. |
| LAST_PREPARATION_TIMESTAMP | TIMESTAMP | Displays the last preparation time stamp. |
| TOTAL_EXECUTION_MEMORY_SIZE | BIGINT | Displays the sum of memory peaks of all plan executions, in bytes.<br>In cases where a query was executed in a scale-out system (that is, the query was running distributed across multiple hosts), then TOTAL_EXECUTION_MEMORY_SIZE is the highest peak memory usage across all involved hosts). So, if host A had a peak usage of 2 GB and host B has a peak usage of 3 GB, then MEMORY_SIZE displays 3 GB. |
| AVG_EXECUTION_MEMORY_SIZE | BIGINT | Displays the average memory peak of all plan executions, in bytes. |
| MIN_EXECUTION_MEMORY_SIZE | BIGINT | Displays the minimum memory peak of all plan executions, in bytes. |
| MAX_EXECUTION_MEMORY_SIZE | BIGINT | Displays the maximum memory peak of all plan executions, in bytes. |
| AVG_SERVICE_NETWORK_REQUEST_COUNT | REAL | Displays the average count of service network requests during plan execution. |
| MAX_SERVICE_NETWORK_REQUEST_COUNT | BIGINT | Displays the maximum count of service network requests during plan execution. |
| TOTAL_SERVICE_NETWORK_REQUEST_COUNT | BIGINT | Displays the total count of service net work requests during plan execution. |
| AVG_CALLED_THREAD_COUNT | REAL | Displays the average count of called threads used during plan execution. |
| MAX_CALLED_THREAD_COUNT | BIGINT | Displays the maximum count of called threads used during plan execution. |
| TOTAL_CALLED_THREAD_COUNT | BIGINT | Displays the total count of called threads used during plan execution. |
| TOTAL_BATCH_EXECUTION_COUNT | BIGINT | Displays a total batch count per one execution for cached DML plans. |
| AVG_BATCH_EXECUTION_COUNT | BIGINT | Displays an average batch count per one execution for cached DML plans. |
| MIN_BATCH_EXECUTION_COUNT | BIGINT | Displays a minimum batch count per one execution for cached DML plans. |
| MAX_BATCH_EXECUTION_COUNT | BIGINT | Displays a maximum batch count per one execution for cached DML plans. |
| AVG_SERVICE_NETWORK_REQUEST_DURATION | REAL | Displays the average time in microseconds of service network requests during plan execution. |
| MAX_SERVICE_NETWORK_REQUEST_DURATION | BIGINT | Displays the maximum time in microseconds of service network requests during plan execution. |
| TOTAL_SERVICE_NETWORK_REQUEST_DURATION | BIGINT | Displays the total time in microseconds of service network requests during plan execution. |
| AVG_SERVICE_NETWORK_REQUEST_SIZE | REAL | Displays the average data amount in bytes of service network requests during plan execution. |
| MAX_SERVICE_NETWORK_REQUEST_SIZE | BIGINT | Displays the maximum amount in bytes of service network requests during plan execution. |
| TOTAL_SERVICE_NETWORK_REQUEST_SIZE | BIGINT | Displays the total amount in bytes of service network requests during plan execution. |
| EXECUTION_ENGINE | VARCHAR(32) | Displays the list of all involved execution frameworks. |
| TOTAL_EXECUTION_CPU_TIME | BIGINT | Displays the total amount of tracked CPU time. |
| AVG_EXECUTION_CPU_TIME | BIGINT | Displays the average amount of tracked CPU time. |
| MIN_EXECUTION_CPU_TIME | BIGINT | Displays the minimum amount of tracked CPU time. |
| MAX_EXECUTION_CPU_TIME | BIGINT | Displays the maximum amount of tracked CPU time. |

## Additional Information

- GLOBAL: A plan always can be shared with any other connections concurrently. There are no restrictions for this plan sharing type.
- SESSION EXCLUSIVE GLOBAL: If a connection uses a plan, the plan cannot be shared with any other connections concurrently, but after the connection releases the plan, it can be acquired by another connection.
- SESSION LOCAL: A plan is never shared. This sharing type is more restricted than SESSION EXCLUSIVE GLOBAL. If a connection generates a plan, the plan belongs to the connection. This plan cannot be shared with any other connection and it cannot be also shared with any other cursor even if in the same connection.
- GLOBAL: -1 (always).
- SESSION EXCLUSIVE GLOBAL: -1 or owner connection ID with positive value (can be changed).
- SESSION LOCAL: owner connection ID with positive value (never changed).

The M_SQL_PLAN_CACHE view shows statistics for an individual plan but not all plans. It shows whether a specified plan runs longer than expected or which part of execution is dominant. For each cached plan, this view delivers statistics from execution on distributed configuration as well as technical details such as related object IDs, updated objects and so on.

This view has a resettable counterpart; you can see the values since the last reset in the M_SQL_PLAN_CACHE_RESET system view. To reset the view, execute the following statement: `ALTER SYSTEM RESET MONITORING VIEW SYS.M_SQL_PLAN_CACHE_RESET;`.

## Related Information

ALTER SYSTEM RESET MONITORING VIEW Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RESET-MONITORING-VIEW-Statement-System.md) M_SQL_PLAN_CACHE_RESET System View [→](M_SQL_PLAN_CACHE_RESET-System-View.md) M_CONNECTIONS System View [→](M_CONNECTIONS-System-View.md)
