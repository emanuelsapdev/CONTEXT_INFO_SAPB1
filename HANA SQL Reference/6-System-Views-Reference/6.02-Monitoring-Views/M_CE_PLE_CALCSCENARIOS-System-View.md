# 6.2.37 M_CE_PLE_CALCSCENARIOS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1677–1678

Provides all available calculation scenarios created by the PlanningEngine.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of calculation scenario. |
| SCENARIO_NAME | NVARCHAR(256) | Displays the calculation scenario name. |

## Related Information

M_CE_CALCSCENARIOS System View [→](M_CE_CALCSCENARIOS-System-View.md) M_CE_CALCSCENARIOS_OVERVIEW System View [→](M_CE_CALCSCENARIOS_OVERVIEW-System-View.md) M_CE_CALCSCENARIO_HINTS System View [→](M_CE_CALCSCENARIO_HINTS-System-View.md)
