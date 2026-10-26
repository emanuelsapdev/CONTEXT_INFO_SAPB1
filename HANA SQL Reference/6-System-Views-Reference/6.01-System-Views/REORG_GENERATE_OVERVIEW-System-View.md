# 6.1.133 REORG_GENERATE_OVERVIEW System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1552–1554

Tracks automated and administrator calls to the REORG_GENERATE procedure.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| GENERATE_ID | BIGINT | Displays the generated ID. This is an increasing, unique number used to identify the call to the REORG_GENERATE procedure. |
| START_DATE | TIMESTAMP | Displays the UTC timestamp when the call reached the engine. |
| CONNECTION_ID | INTEGER | Displays the connection ID that initiates the call to the REORG_GENERATE procedure. |
| USER | NVARCHAR(256) | Displays the user name. |
| ALGORITHM_ID | INTEGER | Displays the table redistribution algorithm ID used the in the call. |
| REORG_ID | INTEGER | Displays the reorganization ID used to select the corresponding executed table redistribution plan. |
| PARAMETERS | NVARCHAR(4096) | Displays the table redistribution parameters that are used in the call. |
| DETAIL | NVARCHAR(1024) | Displays the detailed text for additional information. |

## Related Information

REORG_OVERVIEW System View [→](REORG_OVERVIEW-System-View.md) REORG_PLAN System View [→](REORG_PLAN-System-View.md) REORG_PLAN_INFOS System View [→](REORG_PLAN_INFOS-System-View.md) REORG_STEPS System View [→](REORG_STEPS-System-View.md) M_REORG_ALGORITHMS System View [→](../6.02-Monitoring-Views/M_REORG_ALGORITHMS-System-View.md) PROCEDURES System View [→](PROCEDURES-System-View.md)
