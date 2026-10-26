# 6.1.169 TASK_PARAMETERS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1599–1600

Provides task parameter information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema that the task was created in. |
| TASK_NAME | NVARCHAR(256) | Displays the name of the task. |
| PARAMETER_NAME | NVARCHAR(256) | Displays the name of the parameter. |
| POSITION | INTEGER | Displays the position of the parameter. |
| TABLE_TYPE_SCHEMA | NVARCHAR(256) | Displays the schema that the table type was created in. |
| TABLE_TYPE_NAME | NVARCHAR(256) | Displays the name of the table type. |
| PARAMETER_TYPE | VARCHAR(7) | Displays the parameter type: IN/OUT. |

## Related Information

TASKS System View [→](TASKS-System-View.md) M_TASKS System View [→](../6.02-Monitoring-Views/M_TASKS-System-View.md) START TASK Statement [Smart Data Integration] CANCEL TASK Statement [Smart Data Integration] TASKS System View [Smart Data Integration] TASK_EXECUTIONS System View [Smart Data Integration]
