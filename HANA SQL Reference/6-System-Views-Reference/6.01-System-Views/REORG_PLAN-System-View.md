# 6.1.135 REORG_PLAN System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1555–1556

Provides current plan information for landscape reorganization.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| STEP_ID | INTEGER | Displays the step ID. |
| STEP_GROUP | INTEGER | Displays the step group. |
| PRECONDITION | VARCHAR(1024) | Displays the precondition of the speci fied step. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the table name. |
| TABLE_NAME | NVARCHAR(256) | Displays the schema name. |
| NEW_PARTITION_SPEC | NCLOB | Displays the new partition specification. |
| OLD_PARTITION_SPEC | NCLOB | Displays the old partition specification. |
| PARTITION | INTEGER | Displays the partition ID. |
| NEW_HOST | VARCHAR(64) | Displays the host where the table/partition is moved to. |
| NEW_PORT | INTEGER | Displays the port where the table/partition is moved to. |
| OLD_HOST | VARCHAR(64) | Displays the host where the table/partition is located. |
| OLD_PORT | INTEGER | Displays the port where the table/partition is located. |

## Additional Information

This view contains the last table redistribution plan generated with this database connection. The contents of the session are stored temporarily and are deleted when the connection is closed.

## Related Information

REORG_GENERATE_OVERVIEW System View [→](REORG_GENERATE_OVERVIEW-System-View.md) REORG_OVERVIEW System View [→](REORG_OVERVIEW-System-View.md) REORG_PLAN_INFOS System View [→](REORG_PLAN_INFOS-System-View.md) REORG_STEPS System View [→](REORG_STEPS-System-View.md) M_REORG_ALGORITHMS System View [→](../6.02-Monitoring-Views/M_REORG_ALGORITHMS-System-View.md)
