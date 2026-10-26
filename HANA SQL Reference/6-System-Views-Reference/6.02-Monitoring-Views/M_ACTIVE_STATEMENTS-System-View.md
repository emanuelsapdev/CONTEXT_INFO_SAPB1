# 6.2.4 M_ACTIVE_STATEMENTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1641–1644

Provides a prepared statements list.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| CONNECTION_ID | INTEGER | Displays the connection ID. |
| STATEMENT_ID | VARCHAR(20) | Displays the prepared statement ID. |
| STATEMENT_HASH | VARCHAR(32) | Displays the MD5 hash value for the statement string. |
| START_MVCC_TIMESTAMP | BIGINT | Displays the internal MVCC timestamp of the transaction start time. |
| COMPILED_TIME | TIMESTAMP | Displays the compilation timestamp of the statement. |
| STATEMENT_STATUS | VARCHAR(128) | Displays the status of the SQL statement. |
| STATEMENT_STRING | NCLOB | Displays the SQL statement. |
| ALLOCATED_MEMORY_SIZE | BIGINT | Displays the memory peak used for executing this statement. In case of distributed execution it is a sum of the local peak memories of multiple servers. |
| USED_MEMORY_SIZE | BIGINT | Deprecated. This value is the same as ALLOCATED_MEMORY_SIZE. |
| PLAN_ID | BIGINT | Displays the logical plan ID. |
| LAST_EXECUTED_TIME | TIMESTAMP | Displays the recently executed time of the statement. This timestamp is updated when opening cursors and executing DML/DDL, but not when fetching cursor results or closing cursors. |
| LAST_ACTION_TIME | TIMESTAMP | Displays the recently performed time of action against the statement. This time stamp is updated when opening cursors, executing DML/DDL, fetching results, and closing cursors. |
| RECOMPILE_COUNT | BIGINT | Displays the recompile count. |
| EXECUTION_COUNT | BIGINT | Displays the number of executions. |
| AVG_EXECUTION_TIME | BIGINT | Displays the average statement execution time. |
| MAX_EXECUTION_TIME | BIGINT | Displays the maximum statement execution time. |
| MIN_EXECUTION_TIME | BIGINT | Displays the minimum statement execution time. |
| TOTAL_EXECUTION_TIME | BIGINT | Displays the sum of the statement execution time. |
| AVG_CURSOR_DURATION | BIGINT | Displays the average time of the statement execution including communication time with the clients. |
| MAX_CURSOR_DURATION | BIGINT | Displays the maximum time of the statement execution, including communication time with the clients. |
| MIN_CURSOR_DURATION | BIGINT | Displays the minimum time of the statement execution, including communication time with the clients. |
| TOTAL_CURSOR_DURATION | BIGINT | Displays the sum of the statement execution time, including communication time with clients. |
| AVG_EXECUTION_MEMORY_SIZE | BIGINT | Displays the average memory size, in bytes, used during each execution. |
| MAX_EXECUTION_MEMORY_SIZE | BIGINT | Displays the maximum memory size, in bytes, used during each execution. |
| MIN_EXECUTION_MEMORY_SIZE | BIGINT | Displays the minimum memory size, in bytes, used during each execution. |
| TOTAL_EXECUTION_MEMORY_SIZE | BIGINT | Displays the sum of the memory size, in bytes, used during each execution. |
| AVG_LOCKWAIT_TIME | BIGINT | Displays the average lock wait time for the statement. |
| MAX_LOCKWAIT_TIME | BIGINT | Displays the maximum lock wait time for the statement. |
| MIN_LOCKWAIT_TIME | BIGINT | Displays the minimum lock wait time for the statement. |
| TOTAL_LOCKWAIT_COUNT | BIGINT | Displays the total lock wait count for the statement. |
| TOTAL_LOCKWAIT_TIME | BIGINT | Displays the accumulated lock wait time for the statement. |
| AVG_PREPARATION_TIME | BIGINT | Displays the average time of statement preparation. |
| MAX_PREPARATION_TIME | BIGINT | Displays the maximum time of statement preparation. |
| MIN_PREPARATION_TIME | BIGINT | Displays the minimum time of statement preparation. |
| TOTAL_PREPARATION_TIME | BIGINT | Displays the total time of statement preparation. |
| TOTAL_PREPARATION_COUNT | BIGINT | Displays the total count of statement preparation. |
| HAS_HOLDABLE_CURSOR | VARCHAR(5) | Displays the holdable cursor existence. |
| CURSOR_TYPE | VARCHAR(18) | Displays the type of cursor. |

| PARENT_STATEMENT_ID | VARCHAR(256) |
| --- | --- |

Displays the parent prepared statement ID.

| APPLICATION_SOURCE | NVARCHAR(256) | Displays the application source information. |
| --- | --- | --- |
| WORKLOAD_CLASS_NAME | NVARCHAR(256) | Displays the name of the effective work load class used for the execution. |

## Additional Information

Setting the value of the APPLICATION_SOURCE is only available via internal APIs of the SAP HANA database client interfaces (for more information see SAP Note 2873396).

## Related Information

SAP Note 2873396 M_ACTIVE_PROCEDURES System View [→](M_ACTIVE_PROCEDURES-System-View.md) WORKLOAD_CLASSES System View [→](../6.01-System-Views/WORKLOAD_CLASSES-System-View.md)
