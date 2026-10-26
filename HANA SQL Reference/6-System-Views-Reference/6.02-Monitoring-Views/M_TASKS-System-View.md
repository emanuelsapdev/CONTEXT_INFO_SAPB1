# 6.2.322 M_TASKS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2096–2098

Provides task monitoring information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name used in the task. |
| TASK_NAME | NVARCHAR(256) | Displays the name of the task. |
| CONNECTION_ID | INTEGER | Displays the connection identifier. |
| TRANSACTION_ID | INTEGER | Displays the transaction identifier used for the task execution. |
| TASK_EXECUTION_ID | BIGINT | Displays the unique identifier of the task execution. |
| PARENT_TASK_EXECUTION_ID | BIGINT | Displays the parent task identifier. |
| IS_ASYNC | VARCHAR(5) | Displays whether or not this is an asynchronous task: TRUE/FALSE. |
| PARAMETERS | NVARCHAR(5000) | Displays the input parameters for the task. |
| PROCEDURE_PARAMETERS | NVARCHAR(5000) | Displays the input procedure parameters for the task. |
| START_TIME | TIMESTAMP | Displays the start time of the task. |
| END_TIME | TIMESTAMP | Displays the end time of the task. |
| DURATION | BIGINT | Displays the execution time of the task in microseconds. |
| STATUS | VARCHAR(16) | Displays the status of the task: START ING, RUNNING, FAILED, or COM PLETED. |
| CURRENT_OPERATION | NVARCHAR(128) | Displays the operation of the task. |
| PROCESSED_RECORDS | BIGINT | Displays the total number of processed records. |
| PARTITION_COUNT | INTEGER | Displays the total number of task partitions for a task execution. This value is 1 if there is no task partitioning. |
| TOTAL_PROGRESS_PERCENT | DOUBLE | Displays the total task progress percentage. |
| USER_NAME | NVARCHAR(256) | Displays the user name. |
| APPLICATION_USER_NAME | NVARCHAR(256) | Displays the application user name. |
| HAS_SIDE_EFFECTS | VARCHAR(5) | Displays whether or not the task produces side effect data: TRUE/FALSE. |

## Related Information

TASKS System View [→](../6.01-System-Views/TASKS-System-View.md) TASK_PARAMETERS System View [→](../6.01-System-Views/TASK_PARAMETERS-System-View.md)
