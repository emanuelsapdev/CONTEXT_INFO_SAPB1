# 6.2.110 M_EXPENSIVE_STATEMENTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1792–1796

Provides all statements with a duration longer than a specified threshold.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| CONNECTION_ID | INTEGER | Displays the connection ID. |
| TRANSACTION_ID | INTEGER | Displays the transaction object ID. |
| UPDATE_TRANSACTION_ID | BIGINT | Displays the write transaction ID. |
| STATEMENT_ID | NVARCHAR(256) | Displays the statement ID. |
| PARENT_STATEMENT_ID | VARCHAR(20) | Displays the parent statement ID. |
| STATEMENT_HASH | VARCHAR(32) | Displays the unique identifier for an SQL string. |
| DB_USER | NVARCHAR(256) | Displays the user name. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema in whose context the statement is executed. |
| APP_USER | NVARCHAR(256) | Displays the application user name. |
| START_TIME | TIMESTAMP | Displays the statement start time. |
| DURATION_MICROSEC | BIGINT | Displays the statement duration in microseconds. |
| OBJECT_NAME | NVARCHAR(5000) | Displays the related objects. |
| OPERATION | NVARCHAR(5000) | Displays the type of operation (prepare, execute, fetch, or close). |
| RECORDS | BIGINT | Displays the number of records. |
| STATEMENT_STRING | NCLOB | Displays the statement string. |
| PARAMETERS | NVARCHAR(5000) | Displays the statement parameters. |
| ERROR_CODE | INTEGER | Displays the error code. |
| ERROR_TEXT | NVARCHAR(5000) | Displays the error message. |
| LOCK_WAIT_COUNT | INTEGER | Displays the accumulated lock wait count. |
| LOCK_WAIT_DURATION | BIGINT | Displays the accumulated lock wait duration in microseconds. |
| ALLOC_MEM_SIZE_ROWSTORE | BIGINT | Deprecated, do not use. |
| ALLOC_MEM_SIZE_COLSTORE | BIGINT | Deprecated, do not use. |
| MEMORY_SIZE | BIGINT | Displays the peak memory usage in bytes during the execution of the statement. In cases where a query was executed in a scale-out system (i.e. the query was running distributed across multiple hosts), then MEMORY_SIZE is the highest peak memory usage across all involved hosts. So if host A had a peak usage of 2 GB and host B has a peak usage of 3 GB, then MEMORY_SIZE displays 3 GB.<br>This value is kept for cache reasons or released after the statement execution. |
| REUSED_MEMORY_SIZE | BIGINT | Displays the memory that is reused from cached data structures in bytes. The value is 0 if the cache is empty. |
| CPU_TIME | BIGINT | Displays the CPU time, in microseconds, consumed to compute the statement. |
| PASSPORT_ROOT_CONTEXT_ID | VARCHAR(32) | Displays the SAP EPP Passport GUID that identifies the source of the request. |
| PASSPORT_TRANSACTION_ID | VARCHAR(32) | Displays the SAP EPP Passport GUID that identifies the business transaction. |
| PASSPORT_CONNECTION_ID | VARCHAR(32) | Displays the SAP EPP Passport GUID that identifies the connection. |
| PASSPORT_CONNECTION_COUNTER | BIGINT | Displays the SAP EPP Passport connection counter. |
| STATEMENT_START_TIME | TIMESTAMP | Displays the time when the first operation of a statement execution starts. All operations of a statement execution (prepare, execute, fetch, or close) share the same statement start time. |
| APPLICATION_SOURCE | NVARCHAR(256) | Displays the application from which source file SAP HANA is called. Usage is determined by the application. The value is also displayed in M_PREPARED_STATEMENTS.APPLICATION_SOURCE. |
| APPLICATION_NAME | NVARCHAR(256) | Displays the name of the application. |
| NETWORK_MESSAGE_ID | BIGINT | Displays the client message ID on the physical server connection, also found in M_SQL_CLIENT_NETWORK_IO and MESSAGE_ID. |
| WORKLOAD_CLASS_NAME | NVARCHAR(256) | Displays the name of the effective work load class. |
| PRIORITY | INTEGER | Displays the effective statement priority. |
| STATEMENT_THREAD_LIMIT | INTEGER | Displays the effective statement thread limit. |
| STATEMENT_MEMORY_LIMIT | INTEGER | Displays the effective statement memory limit. |
| SESSION_VARIABLES | NCLOB | Displays the statement's session variables. |

## Additional Information

Allows you to monitor all statements that have an execution time longer than a predefined threshold (configurable in the [expensive_statement] section of the `global.ini` file), which may sometimes cause barriers.

The M_EXPENSIVE_STATEMENTS view provides convenient access to the most expensive statements that are executed on the system. A statement is considered expensive if its runtime exceeds a particular threshold.

The following types of operations are tracked:

- COMPILE: compiles the statement.
- FETCH: fetches the result set.
- CURSOR_CLOSE: the closing cursor.
- AGGREGATED_EXECUTION: calculates the overall execution time for SELECT queries, including compilation time in the case of non-prepared statements. For prepared statements, compilation time is not included in the AGGREGATED_EXECUTION of every prepared statement execution, since compilation usually occurs only once (except for recompilation at runtime). Adding compilation time to AGGREGATED_EXECUTION may exaggerate the overall execution time. For non-prepared statements, compilation time is included in the AGGREGATED_EXECUTION of every ad hoc statement execution since it is newly compiled or is attempting to look up a SQL plan cache every time within a single session request.

The following types of operations execute a DML statement:

- CALL
- DELETE
- DEQUEUE
- EXPLAIN_PLAN
- INSERT
- SELECT
- SELECT_FOR_UPDATE
- UPDATE
- EXECUTE_DML: represents the less common DML statements that are not listed above.

The following operations execute a DDL statement:

- CREATE_TABLE
- CREATE_VIEW
- EXECUTE_DDL: represents the less common DDL statements that are not listed above.

The following operations execute statements except DML and DDL:

- EXECUTE: represents the less common SQL statements.

Consider a query with 4 session requests from a client:

1. Prepare: 10 msec
2. Execute: 20 msec
3. Fetch: 15 msec
4. Close: 5 msec

Assuming that all operations are longer than the threshold, they are shown as: OPERATION DURATION COMPILE 10 SELECT 20 FETCH 15 CURSOR_CLOSE 5 AGGREGATED_EXECUTION 40 (20+15+5).

## Additional Information

Setting the value of the APPLICATION_SOURCE is only available via internal APIs of the SAP HANA database client interfaces (for more information see SAP Note 2873396).

## Related Information

[SAP Note 2873396 M_EXPENSIVE_STATEMENT_EXECUTION_LOCATION_STATISTICS System View](M_EXPENSIVE_STATEMENT_EXECUTION_LOCATION_STATISTICS-System.md)
