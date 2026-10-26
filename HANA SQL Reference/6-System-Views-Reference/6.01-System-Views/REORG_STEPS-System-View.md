# 6.1.137 REORG_STEPS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1557–1558

Contains the executed or to be executed table redistribution plan items.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| REORG_ID | INTEGER | Displays the reorg ID. |
| STEP_ID | INTEGER | Displays the step ID. |
| STEP_GROUP | INTEGER | Displays the ID of the table redistribution group of steps that the item belongs to. |
| PRECONDITION | VARCHAR(1024) | Indicates the preconditions that have to be fulfilled before the table redistribution step can be executed. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| NEW_PARTITION_SPEC | NCLOB | Returns the new partition specification. |
| OLD_PARTITION_SPEC | NCLOB | Returns the old partition specification. |
| PARTITION | INTEGER | Displays the partition ID. |
| NEW_HOST | VARCHAR(64) | Displays the host where the table/partition is moved to. |
| NEW_PORT | INTEGER | Displays the port where the table/partition is moved to. |
| OLD_HOST | VARCHAR(64) | Displays the host where the table/partition was located. |
| OLD_PORT | INTEGER | Displays the port where the table/partition was located. |
| STATUS | VARCHAR(32) | Displays the status message. |
| ERROR | VARCHAR(1024) | Displays the error message. |
| START_DATE | TIMESTAMP | Specifies the UTC timestamp when the plan execution started. |
| END_DATE | TIMESTAMP | Specifies the UTC timestamp when the plan execution stopped. |

## Related Information

REORG_GENERATE_OVERVIEW System View [→](REORG_GENERATE_OVERVIEW-System-View.md) REORG_OVERVIEW System View [→](REORG_OVERVIEW-System-View.md) REORG_PLAN System View [→](REORG_PLAN-System-View.md) REORG_PLAN_INFOS System View [→](REORG_PLAN_INFOS-System-View.md) M_REORG_ALGORITHMS System View [→](../6.02-Monitoring-Views/M_REORG_ALGORITHMS-System-View.md)
