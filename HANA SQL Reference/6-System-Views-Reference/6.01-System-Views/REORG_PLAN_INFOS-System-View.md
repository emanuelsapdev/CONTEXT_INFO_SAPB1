# 6.1.136 REORG_PLAN_INFOS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1556–1557

Provides additional information about the current landscape reorganization plan.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| KEY | VARCHAR(256) | Displays the key. |
| VALUE | VARCHAR(1024) | Displays the value. |

## Additional Information

This view contains information about the last table redistribution plan generation with this database connection. The contents are stored for the current session and are deleted when the connection is closed. The following list describes the contents of the individual lines of this view (`VALUE`), as identified by `KEY`:

**MOVE_PHYSICAL** Indicates that all move operations during plan execution are executed as physical moves. Possible values are 0 or 1.

**ALGORITHM_ID** Displays the ID of the reorg algorithm that is used for generating the corresponding table redistribution plan.

**PARAMETERS** Displays the parameter information of the last table redistribution plan generation call.

## Related Information

REORG_GENERATE_OVERVIEW System View [→](REORG_GENERATE_OVERVIEW-System-View.md) REORG_OVERVIEW System View [→](REORG_OVERVIEW-System-View.md) REORG_PLAN System View [→](REORG_PLAN-System-View.md) REORG_STEPS System View [→](REORG_STEPS-System-View.md) M_REORG_ALGORITHMS System View [→](../6.02-Monitoring-Views/M_REORG_ALGORITHMS-System-View.md)
