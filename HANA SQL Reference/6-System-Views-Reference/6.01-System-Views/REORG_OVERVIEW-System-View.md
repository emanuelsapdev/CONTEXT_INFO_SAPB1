# 6.1.134 REORG_OVERVIEW System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1554–1555

Provides an overview of landscape redistributions.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| REORG_ID | INTEGER | Displays the unique identifier for the executed reorg plan. |
| STATUS | VARCHAR(32) | Displays the status of the plan execution:<br>• STARTED: The plan execution has started.<br>• FINISHED: The plan execution finished successfully.<br>• FAILED: The plan execution is treated as failed. |
| START_DATE | TIMESTAMP | Displays the UTC timestamp when the plan execution started. |
| END_DATE | TIMESTAMP | Displays the UTC timestamp when plan execution stopped. This field remains empty while the execution is running or in the case of reboots during plan execution. |
| USER | VARCHAR(256) | Displays the user that executed the table redistribution. |
| ALGORITHM_ID | INTEGER | Displays the ID of the algorithm for the table redistribution. |
| PARAMETERS | VARCHAR(1024) | Displays the parameters given for the table redistribution call. |

## Additional Information

This view contains information about table redistribution executions on this system and stores every call to the REORG_EXECUTE statement. You can use this view to determine execution durations and the status of each table redistribution on this system. Only executed plan information is stored and calls of REORG_GENERATE without REORG_EXECUTE are not displayed.

## Related Information

REORG_GENERATE_OVERVIEW System View [→](REORG_GENERATE_OVERVIEW-System-View.md) REORG_PLAN System View [→](REORG_PLAN-System-View.md) REORG_PLAN_INFOS System View [→](REORG_PLAN_INFOS-System-View.md) REORG_STEPS System View [→](REORG_STEPS-System-View.md) M_REORG_ALGORITHMS System View [→](../6.02-Monitoring-Views/M_REORG_ALGORITHMS-System-View.md)
