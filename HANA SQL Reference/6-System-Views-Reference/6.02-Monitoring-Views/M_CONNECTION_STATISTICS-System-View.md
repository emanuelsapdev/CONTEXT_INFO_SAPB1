# 6.2.46 M_CONNECTION_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1690–1695

Provides detailed statistics on each connection between an application and database.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| CONNECTION_ID | INTEGER | Displays the connection ID. |
| SELECT_EXECUTION_COUNT | BIGINT | Displays the total number of select statement executions. |
| SELECT_TOTAL_EXECUTION_TIME | BIGINT | Displays the total execution time of select statement executions. |
| SELECT_AVG_EXECUTION_TIME | REAL | Displays the average execution time of select statement executions. |
| SELECT_MAX_EXECUTION_TIME | BIGINT | Displays the maximum execution time of select statement executions. |
| SELECT_FOR_UPDATE_COUNT | BIGINT | Displays the total number of select for update executions. |
| SELECT_FOR_UPDATE_TOTAL_EXECUTION_TIME | BIGINT | Displays the total execution time of select for update executions. |
| SELECT_FOR_UPDATE_AVG_EXECUTION_TIME | REAL | Displays the average execution time of select for update executions. |
| SELECT_FOR_UPDATE_MAX_EXECUTION_TIME | BIGINT | Displays the maximum execution time of select for update execution. |
| SELECT_FOR_UPDATE_LOCK_WAIT_COUNT | BIGINT | Displays the number of lock waits during select for update. |
| SELECT_FOR_UPDATE_TOTAL_LOCK_WAIT_TIME | BIGINT | Displays the total lock wait time during select for update. |
| SELECT_FOR_UPDATE_AVG_LOCK_WAIT_TIME | REAL | Displays the average lock wait time during select for update. |
| SELECT_FOR_UPDATE_MAX_LOCK_WAIT_TIME | BIGINT | Displays the maximum lock wait time during select for update. |
| UPDATE_COUNT | BIGINT | Displays the total number of update statement and insert statement executions. |
| UPDATE_TOTAL_EXECUTION_TIME | BIGINT | Displays the total execution time of up date statement executions in microseconds. |
| UPDATE_AVG_EXECUTION_TIME | REAL | Displays the average execution time of update statement executions in microseconds. |
| UPDATE_MAX_EXECUTION_TIME | BIGINT | Displays the maximum execution time of update statement executions in microseconds. |
| UPDATE_LOCK_WAIT_COUNT | BIGINT | Displays the number of lock waits during update statement executions. |
| UPDATE_TOTAL_LOCK_WAIT_TIME | BIGINT | Displays the total lock wait execution time during update statement executions in microseconds. |
| UPDATE_AVG_LOCK_WAIT_TIME | REAL | Displays the average lock wait time during update statement executions in microseconds. |
| UPDATE_MAX_LOCK_WAIT_TIME | BIGINT | Displays the maximum lock wait time during update statement executions in microseconds. |
| READ_ONLY_TRANSACTION_COUNT | BIGINT | Displays the number of read only trans actions. |
| READ_ONLY_TRANSACTION_TOTAL_EXECUTION_TIME | BIGINT | Displays the total execution time of read only transactions in microseconds. |
| READ_ONLY_TRANSACTION_AVG_EXECUTION_TIME | REAL | Displays the average execution time of read only transactions in microseconds. |
| READ_ONLY_TRANSACTION_MAX_EXECUTION_TIME | BIGINT | Displays the maximum execution time of read only transactions. |
| UPDATE_TRANSACTION_COUNT | BIGINT | Displays the number of update transactions. |
| UPDATE_TRANSACTION_TOTAL_EXECUTION_TIME | BIGINT | Displays the total execution time of up date transactions. |
| UPDATE_TRANSACTION_AVG_EXECUTION_TIME | REAL | Displays the average execution time of update transactions. |
| UPDATE_TRANSACTION_MAX_EXECUTION_TIME | BIGINT | Displays the maximum execution time of update transactions. |
| ROLLBACK_COUNT | BIGINT | Displays the number of rolled backed transactions. |
| ROLLBACK_TOTAL_EXECUTION_TIME | BIGINT | Displays the total execution time of rollbacks. |
| ROLLBACK_AVG_EXECUTION_TIME | REAL | Displays the average execution time of rollbacks. |
| ROLLBACK_MAX_EXECUTION_TIME | BIGINT | Displays the maximum execution time of rollbacks. |
| OTHERS_COUNT | BIGINT | Displays the number of other statement executions including data definition statements and data control statements. |
| OTHERS_TOTAL_EXECUTION_TIME | BIGINT | Displays the total execution time of other statements. |
| OTHERS_AVG_EXECUTION_TIME | REAL | Displays the average execution time of other statements. |
| OTHERS_MAX_EXECUTION_TIME | BIGINT | Displays the maximum execution time of other statements. |
| OTHERS_LOCK_WAIT_COUNT | BIGINT | Displays the total lock wait count of other statements. |
| OTHERS_TOTAL_LOCK_WAIT_TIME | BIGINT | Displays the total lock wait time of other statements. |
| OTHERS_AVG_LOCK_WAIT_TIME | REAL | Displays the average lock wait time of other statements. |
| OTHERS_MAX_LOCK_WAIT_TIME | BIGINT | Displays the maximum lock wait time of other statements. |
| LAST_EXECUTED_TIME | TIMESTAMP | Displays the last execution timestamp with this connection. |
| AVG_EXECUTION_MEMORY_SIZE | BIGINT | Displays the average memory size used during each execution in bytes. |
| MAX_EXECUTION_MEMORY_SIZE | BIGINT | Displays the maximum memory size used during each execution in bytes. |
| MIN_EXECUTION_MEMORY_SIZE | BIGINT | Displays the minimum memory size used during each execution in bytes. |
| TOTAL_EXECUTION_MEMORY_SIZE | BIGINT | Displays the sum of the memory size used during each execution in bytes. |
| AVG_PREPARATION_TIME | BIGINT | Displays the average time of the statement preparation. |
| MAX_PREPARATION_TIME | BIGINT | Displays the maximum time of the statement preparation. |
| MIN_PREPARATION_TIME | BIGINT | Displays the minimum time of the statement preparation. |
| TOTAL_PREPARATION_TIME | BIGINT | Displays the total time of the statement preparation. |
| TOTAL_PREPARATION_COUNT | BIGINT | Displays the total count of statement preparation. |
| EXECUTION_COUNT_BY_ROUTING | BIGINT | Displays the execution count by the client routed connection in statement routing. |
| COMMIT_MAX_EXECUTION_TIME | BIGINT | Displays the maximum time of the commit execution. |
| COMMIT_AVG_EXECUTION_TIME | REAL | Displays the average time of the commit execution. |
| COMMIT_TOTAL_EXECUTION_TIME | BIGINT | Displays the total time of the commit duration. |
| COMMIT_COUNT | BIGINT | Displays the completed commit count. |
| END_TIME | TIMESTAMP | Displays the time when the connection is closed for history connections. |

## Related Information

M_CONNECTIONS System View [→](M_CONNECTIONS-System-View.md) CONNECT Statement (Session Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CONNECT-Statement-Session-Management.md)
