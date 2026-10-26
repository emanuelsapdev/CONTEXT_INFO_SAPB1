# 6.2.183 M_MULTIDIMENSIONAL_STATEMENT_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1906–1908

Displays all multidimensional statement statistics gathered since the server started. This information does not persist when you restart the server.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| STATEMENT_STRING | NCLOB | Displays the statement string. |
| STATEMENT_HASH | VARCHAR(32) | Displays the statement hash. |
| USER_NAME | NVARCHAR(256) | Displays the name of the user. |
| APPLICATION_USER_NAME | NVARCHAR(256) | Displays the name of the application user. |
| APPLICATION_NAME | NVARCHAR(256) | Displays the name of the application. |
| STATEMENT_TYPE | VARCHAR(3) | Displays the statement type as either INA or MDX. |
| LAST_CONNECTION_ID | INTEGER | Displays the last connection ID that executed the statement. |
| LAST_EXECUTION_TIMESTAMP | TIMESTAMP | Displays the time of the last execution. |
| LAST_METADATA_READ_DURATION | BIGINT | Displays the last metadata read duration. |
| LAST_QUERY_PREPARATION_DURATION | BIGINT | Displays the last query preparation duration. |
| LAST_PLAN_EXECUTION_DURATION | BIGINT | Displays the last plan execution duration. |
| LAST_POST_PROCESSING_DURATION | BIGINT | Displays the last post processing duration. |
| LAST_CUBE_PROCESSING_DURATION | BIGINT | Displays the last cube processing duration. |
| LAST_PLAN_EXECUTION_RESULTSET_SIZE | BIGINT | Displays the last size of the intermediate result returned by the plan execution, in bytes. |
| LAST_RESULTSET_SIZE | BIGINT | Displays the size of the last result set, in bytes. |
| LAST_RESULTSET_CELL_COUNT | BIGINT | Displays the number of cells in the last result set. |
| LAST_HIERARCHY_COUNT | INTEGER | Displays the latest number of hierar chies. |
| LAST_CACHED_HIERARCHY_COUNT | INTEGER | Displays the last number of hierarchy cache hits. |
| LAST_CALCULATION_ENTITY_COUNT | INTEGER | Displays the last number of calculation entities. |
| LAST_CALCULATION_ENTITY_GROUP_COUNT | INTEGER | Displays the last number of calculation entity groups. |
| LAST_DRILL_DIMENSION_COUNT | INTEGER | Displays the last number of dimensions in the drill. |
| LAST_AGGREGATION_DIMENSION_COUNT | INTEGER | Displays the last number of aggregation dimensions. |
| LAST_SERIALIZED_CUBE_SIZE | BIGINT | Displays the last size of the serialized cube, in bytes. |
| LAST_REQUEST_QUEUE_COUNT | BIGINT | Displays the number of jobs waiting in the request queue. |
| LAST_EXECUTION_STATUS | VARCHAR(16) | Displays the last execution status of the statement. |
| LAST_PERFORMANCE_DATA | NCLOB | Displays the last performance data. |
| EXECUTION_COUNT | INTEGER | Displays the execution count. |
| TOTAL_METADATA_CACHE_HIT_COUNT | INTEGER | Displays the number of data cache hits. |
| TOTAL_DATA_CACHE_HIT_COUNT | INTEGER | Displays the number of data cached hits. |
| TOTAL_EXECUTION_TIME | BIGINT | Displays the total time of the execution. |
| AVG_EXECUTION_TIME | BIGINT | Displays the average time of the execution. |
| MIN_EXECUTION_TIME | BIGINT | Displays the minimum time of the execution. |
| MAX_EXECUTION_TIME | BIGINT | Displays the maximum time of the execution. |
| MAX_CALLED_THREAD_COUNT | INTEGER | Displays the maximum thread count. |
| MAX_EXECUTION_MEMORY_SIZE | BIGINT | Displays the maximum memory size in bytes. |
