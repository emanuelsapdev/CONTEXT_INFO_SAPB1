# 6.2.281 M_SQL_PLAN_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2034–2041

Provides statistics of a live or evicted individual execution plan.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| VOLUME_ID | INTEGER | Displays the persistence volume ID. |
| STATEMENT_STRING | NCLOB | Displays the statement string. |
| STATEMENT_HASH | VARCHAR(32) | Displays the MD5 hash value for STATEMENT_STRING. |
| USER_NAME | NVARCHAR(256) | Displays the user name who prepared the plan. |
| SESSION_USER_NAME | NVARCHAR(256) | Displays the SESSION_USER name who prepared the plan. The same value as M_CONNECTIONS.USER_NAME. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name that the SQL plan belongs to. |
| SESSION_PROPERTIES | NVARCHAR(500) | Displays the composed variables that can be changed by session context. |
| IS_VALID | VARCHAR(5) | Displays whether the plan is currently valid: TRUE/ FALSE. |
| IS_EVICTED | VARCHAR(5) | Displays whether the plan has already been evicted: TRUE/FALSE. |
| LAST_INVALIDATION_REASON | VARCHAR(64) | Displays the last plan invalidation reason. |
| IS_INTERNAL | VARCHAR(5) | Displays whether the plan is executed from a data base internal connection (TRUE) or from a remote connection (FALSE). |
| IS_DISTRIBUTED_EXECUTION | VARCHAR(5) | Displays whether the tables are located in multiple nodes: TRUE/FALSE. |
| COMPILATION_OPTIONS | VARCHAR(128) | Displays the compilation options that are used by the SQL Query Optimizer when it generates cached execution plans:<br>• Returns an empty string if the SQL Query Optimizer compiled without any special settings<br>• Returns a STATEMENT HINT option when the SQL Query Optimizer compiles and optimizes with a statement hint<br>• Returns an ABSTRACT SQL PLAN option when the SQL Query Optimizer compiles with an abstract sql plan<br>Multiple options can be used together to create a list of options, for example: STATEMENT HINT, AB STRACT SQL PLAN. |
| IS_PINNED_PLAN | VARCHAR(5) | Displays whether the plan is explicitly stored by Plan Viz utility: TRUE/FALSE. |
| PINNED_PLAN_ID | BIGINT | If this plan is pinned, dispalys the same value as PINNED_SQL_PLANS.ID. |
| ABAP_VARCHAR_MODE | VARCHAR(5) | Displays whether ABAP VARCHAR mode is enabled: TRUE/FALSE. |
| APPLICATION_NAME | NVARCHAR(256) | Displays the application name information. |
| APPLICATION_SOURCE | NVARCHAR(256) | Displays the application source information. |
| ACCESSED_TABLES | VARCHAR(5000) | Displays the relevant base table ID list accessed in the plan. |
| ACCESSED_TABLE_NAMES | NCLOB | Displays the relevant base table name list accessed in the plan. |
| ACCESSED_OBJECTS | VARCHAR(5000) | Displays the relevant table object ID list accessed in the plan. |
| ACCESSED_OBJECT_NAMES | NCLOB | Displays the relevant schema object name list accessed in the plan. |
| TABLE_LOCATIONS | VARCHAR(2000) | Displays the relevant table locations for the plan. |
| TABLE_TYPES | VARCHAR(128) | Displays whether the plan refers Column store only, Row store only or mixed. |
| PLAN_SHARING_TYPE | VARCHAR(128) | Displays the plan sharing type. |
| OWNER_CONNECTION_ID | BIGINT | Displays the connection owning the plan. The possible values are:<br>• GLOBAL: -1 (always)<br>• SESSION EXCLUSIVE GLOBAL: -1, owner connection ID, which is a positive value<br>• SESSION LOCAL: owner connection ID, which is a positive value (never changed) |
| PLAN_ID | BIGINT | Displays the logical plan ID, which is a non-negative value. If the plan is evicted, -1 is shown. |
| PLAN_MEMORY_SIZE | BIGINT | Displays the memory size used by the plan in bytes. |
| EVICTION_COUNT | BIGINT | Displays the number of evictions that have occurred for the plan. |
| LAST_EVICTION_TIMESTAMP | TIMESTAMP | Displays the timestamp when the plan was evicted for the last time. Returns zero if the plan has never been evicted. |
| REFERENCE_COUNT | BIGINT | Displays the number of statements using the plan. |
| PARAMETER_COUNT | BIGINT | Displays the number of parameters to be assigned for the execution. |
| UPDATED_TABLE_OID | BIGINT | Displays the object ID of the table changed by the plan. |
| LOGICAL_CONNECTION_VOLUME_ID | BIGINT | Displays the volume ID of the logical connection. This value is 0 if there is no session context. |
| EXECUTION_COUNT | BIGINT | Displays the accumulated count of plan execution for valid and evicted plans. |
| EXECUTION_COUNT_BY_ROUTING | BIGINT | Displays the accumulated count of plan execution by client-routed connection in statement routing for valid and evicted plans. |
| TOTAL_CURSOR_DURATION | BIGINT | Displays the sum of time, in microseconds, that cursors were opened. This includes plan execution and communication time with clients for valid and evicted plans. |
| AVG_CURSOR_DURATION | BIGINT | Displays the average time, in microseconds, of the plan execution, including communication time with clients for valid and evicted plans. |
| MIN_CURSOR_DURATION | BIGINT | Displays the minimum time, in microseconds, of the plan execution, including communication time with clients for valid and evicted plans. |
| MAX_CURSOR_DURATION | BIGINT | Displays the maximum time, in microseconds, of the plan execution, including communication time with clients for valid and evicted plans. |
| TOTAL_EXECUTION_TIME | BIGINT | Displays the sum of time, in microseconds, of the plan execution for valid and evicted plans. |
| AVG_EXECUTION_TIME | BIGINT | Displays the average time of the plan execution. |
| MIN_EXECUTION_TIME | BIGINT | Displays the minimum time of the plan execution. |
| MAX_EXECUTION_TIME | BIGINT | Displays the maximum time of the plan execution. |
| TOTAL_EXECUTION_OPEN_TIME | BIGINT | Displays the sum of time in microseconds for cursor open for valid and evicted plans. |
| AVG_EXECUTION_OPEN_TIME | BIGINT | Displays the average time in microseconds for cursor open for valid and evicted plans. |
| MIN_EXECUTION_OPEN_TIME | BIGINT | Displays the minimum time in microseconds for cursor open for valid and evicted plans. |
| MAX_EXECUTION_OPEN_TIME | BIGINT | Displays the maximum time in microseconds for cursor open for valid and evicted plans. |

| TOTAL_EXECUTION_FETCH_TIME | BIGINT |
| --- | --- |

Displays the sum of time in microseconds for cursor fetch for valid and evicted plans.

| AVG_EXECUTION_FETCH_TIME | BIGINT | Displays the average time in microseconds for cursor fetch for valid and evicted plans. |
| --- | --- | --- |
| MIN_EXECUTION_FETCH_TIME | BIGINT | Displays the minimum time in microseconds for cursor fetch for valid and evicted plans |
| MAX_EXECUTION_FETCH_TIME | BIGINT | Displays the maximum time in microseconds for cursor fetch for valid and evicted plans. |
| TOTAL_EXECUTION_CLOSE_TIME | BIGINT | Displays the sum of time in microseconds for cursor close for valid and evicted plans. |

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| AVG_EXECUTION_CLOSE_TIME | BIGINT | Displays the average time in microseconds for cursor close for valid and evicted plans. |
| MIN_EXECUTION_CLOSE_TIME | BIGINT | Displays the minimum time in microseconds for cursor close for valid and evicted plans. |
| MAX_EXECUTION_CLOSE_TIME | BIGINT | Displays the maximum time in microseconds for cursor close for valid and evicted plans. |
| TOTAL_METADATA_CACHE_MISS_COUNT | BIGINT | Deprecated. |
| TOTAL_TABLE_LOAD_TIME_DURING_PREPARATION | BIGINT | Displays the sum of table loading time during plan preparation for valid and evicted plans. |
| AVG_TABLE_LOAD_TIME_DURING_PREPARATION | BIGINT | Displays the average table loading time in microseconds during plan preparation for valid and evicted plans. |
| MIN_TABLE_LOAD_TIME_DURING_PREPARATION | BIGINT | Displays the minimum table loading time during plan preparation for valid and evicted plans. |
| MAX_TABLE_LOAD_TIME_DURING_PREPARATION | BIGINT | Displays the maximum table loading time in microseconds during plan preparation for valid and evicted plans. |
| PREPARATION_COUNT | BIGINT | Displays the count of plan preparations for valid and evicted plans. |
| TOTAL_PREPARATION_TIME | BIGINT | Displays the sum of time in microseconds of plan preparation for valid and evicted plans. |
| AVG_PREPARATION_TIME | BIGINT | Displays the average time in microseconds of plan preparation for valid and evicted plans. |
| MIN_PREPARATION_TIME | BIGINT | Displays the minimum time in microseconds of plan preparation for valid and evicted plans. |
| MAX_PREPARATION_TIME | BIGINT | Displays the maximum time in microseconds of plan preparation for valid and evicted plans. |
| TOTAL_RESULT_RECORD_COUNT | BIGINT | Displays the accumulated number of records during plan execution for valid and evicted plans. |
| TOTAL_LOCK_WAIT_COUNT | BIGINT | Displays the accumulated lock wait count for the plan for valid and evicted plans. |
| TOTAL_LOCK_WAIT_DURATION | BIGINT | Displays the accumulated lock wait duration in microseconds for the plan for valid and evicted plans. |
| LAST_CONNECTION_ID | BIGINT | Displays the last connection ID that executed the plan. |
| LAST_EXECUTION_TIMESTAMP | TIMESTAMP | Displays the timestamp when the plan was executed for the last time. |
| LAST_PREPARATION_TIMESTAMP | TIMESTAMP | Displays the timestamp when the plan was compiled for the last time. |
| TOTAL_EXECUTION_MEMORY_SIZE | BIGINT | With memory tracking, displays the average size in bytes of tracked actual memory consumption for valid and evicted plans. |
| AVG_EXECUTION_MEMORY_SIZE | BIGINT | With memory tracking, displays the maximum size in bytes of tracked actual memory consumption for valid and evicted plans. |
| MIN_EXECUTION_MEMORY_SIZE | BIGINT | With memory tracking, displays the minimum size in bytes of tracked actual memory consumption for valid and evicted plans. |
| MAX_EXECUTION_MEMORY_SIZE | BIGINT | With memory tracking, displays the total size in bytes of tracked actual memory consumption for valid and evicted plans. |
| AVG_SERVICE_NETWORK_REQUEST_COUNT | BIGINT | Displays the average count of service network requests during plan execution for valid and evicted plans. |
| MAX_SERVICE_NETWORK_REQUEST_COUNT | BIGINT | Displays the maximum count of service network requests during plan execution for valid and evicted plans. |
| TOTAL_SERVICE_NETWORK_REQUEST_COUNT | BIGINT | Displays the total count of service network requests during plan execution for valid and evicted plans. |
| AVG_CALLED_THREAD_COUNT | BIGINT | Displays the average count of called threads used during plan execution for valid and evicted plans. |
| MAX_CALLED_THREAD_COUNT | BIGINT | Displays the average count of called threads used during plan execution for valid and evicted plans. |
| TOTAL_CALLED_THREAD_COUNT | BIGINT | Displays the total count of called threads used during plan execution for valid and evicted plans. |
| TOTAL_BATCH_EXECUTION_COUNT | BIGINT | Displays a total batch count per one execution for cached DML plans for valid and evicted plans. |
| AVG_BATCH_EXECUTION_COUNT | BIGINT | Displays an average batch count per one execution for cached DML plans for valid and evicted plans. |
| MIN_BATCH_EXECUTION_COUNT | BIGINT | Displays a minimum batch count per one execution for cached DML plans for valid and evicted plans. |
| MAX_BATCH_EXECUTION_COUNT | BIGINT | Displays a maximum batch count per one execution for cached DML plans for valid and evicted plans. |
| AVG_SERVICE_NETWORK_REQUEST_DURATION | REAL | Displays the average time of the service network requests during plan execution. |
| MAX_SERVICE_NETWORK_REQUEST_DURATION | BIGINT | Displays the maximum time of the service network requests during plan execution. |
| TOTAL_SERVICE_NETWORK_REQUEST_DURATION | BIGINT | Displays the total time of the service network requests during plan execution. |
| AVG_SERVICE_NETWORK_REQUEST_SIZE | REAL | Displays the average data amount of service network requests during plan execution in bytes. |
| MAX_SERVICE_NETWORK_REQUEST_SIZE | BIGINT | Displays the maximum amount of service network requests during plan execution in bytes. |
| TOTAL_SERVICE_NETWORK_REQUEST_SIZE | BIGINT | Displays the total amount of service network requests during plan execution in bytes. |

## Additional Information

The M_SQL_PLAN_STATISTICS view shows statistics for an individual plan, whether it is live or evicted. A plan is evicted from the plan cache, and is not stored in the M_SQL_PLAN_CACHE System View, if it is the least recently used cache entry. It shows whether a specified plan runs longer than expected or which part of execution is dominant. For each cached plan, this view delivers statistics from execution on distributed configuration, as well as technical details such as related object IDs, updated objects, and so on.

Information about live and evicted plans is useful in the following scenarios:

- If a previously evicted plan entry is recreated in the plan cache with a high execution statistics number, then you might assume that the plan should not have been evicted and should increase your plan cache size.
- If you want to have an overview of plan statistics, even though some plans have already been evicted.
- If you want to determine which kinds of queries are repeatedly evicted.
- If you want to determine the cause of performance regression, then you can check the statistics of evicted plans for information on how frequently the plan was executed, for how long, and so on.

## Related Information

M_SQL_PLAN_CACHE System View [→](M_SQL_PLAN_CACHE-System-View.md) M_CONNECTIONS System View [→](M_CONNECTIONS-System-View.md) M_SQL_PLAN_STATISTICS_RESET System View [→](M_SQL_PLAN_STATISTICS_RESET-System-View.md)
