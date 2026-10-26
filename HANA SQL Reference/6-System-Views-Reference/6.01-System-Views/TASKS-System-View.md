# 6.1.168 TASKS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1597–1599

Provides information regarding table tasks.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| TASK_OID | BIGINT | Displays the unique identifier for the task. |
| TASK_NAME | NVARCHAR(256) | Displays the name of the task. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema that the task was created in. |
| OWNER_NAME | NVARCHAR(256) | Displays the owner of the task. |
| CREATE_TIME | TIMESTAMP | Displays the creation time. |
| MEMORY_SIZE | BIGINT | Displays the memory size of loaded task in bytes. |
| TASK_TYPE | NVARCHAR(64) | Displays the type of task derived from the task plan. |
| PLAN_VERSION | NVARCHAR(32) | Displays the version of the task plan. |
| PLAN | NCLOB | Displays the task plan used to define the task. This value is NULL if the task was created using a procedure. |
| COMMENTS | NVARCHAR(256) | Displays the description of the task from the task plan. |
| HAS_TABLE_TYPE_INPUT | VARCHAR(5) | Displays whether or not the task is modeled with a table type as input: TRUE/FALSE. If TRUE, this means that data would need to be pushed at execution time. |
| HAS_SDQ | VARCHAR(5) | Displays whether or not the task contains SDQ (Smart Data Quality) functionality: TRUE/FALSE. |
| IS_REALTIME_TASK | VARCHAR(5) | Displays whether or not the specified task is a realtime task. |
| IS_VALID | VARCHAR(5) | Displays whether or not the task is in a valid state: TRUE/FALSE. FALSE indicates that the task has been invalidated by a dependency. |
| IS_READ_ONLY | VARCHAR(5) | Displays whether or not the task is read only, meaning it has only table type out puts: TRUE/FALSE. FALSE indicates that the task writes to non-table-type outputs. |
| PROCEDURE_SCHEMA | NVARCHAR(256) | If the task was created with a procedure instead of a plan, contains the schema name of the stored procedure. |
| PROCEDURE_NAME | NVARCHAR(256) | If the task was created with a procedure instead of a plan, contains the name of the stored procedure. |
| INPUT_PARAMETER_COUNT | SMALLINT | Displays the number of input (tab leType) parameters. |
| OUTPUT_PARAMETER_COUNT | SMALLINT | Displays the number of output (tab leType) parameters. |
| SQL_SECURITY | VARCHAR(7) | Displays the security model for the task: DEFINER/INVOKER. |

## Related Information

TASK_PARAMETERS System View [→](TASK_PARAMETERS-System-View.md) M_TASKS System View [→](../6.02-Monitoring-Views/M_TASKS-System-View.md) START TASK Statement [Smart Data Integration]

CANCEL TASK Statement [Smart Data Integration] TASKS System View [Smart Data Integration] TASK_EXECUTIONS System View [Smart Data Integration]
