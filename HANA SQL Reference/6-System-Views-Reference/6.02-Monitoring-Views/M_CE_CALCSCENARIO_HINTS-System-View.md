# 6.2.32 M_CE_CALCSCENARIO_HINTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1673–1674

Exposes all hints that are defined in a calculation scenario.

| **Column** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| SCENARIO_NAME | NVARCHAR(256) | Displays the scenario name. |
| HINT_TYPE | VARCHAR(32) | Displays the hint name. For example, qo_pop_hints. |
| HINT_VALUE | NVARCHAR(256) | Displays the hint value. For example, USE_OLAP_PLAN. |

## Related Information

M_CE_CALCSCENARIOS System View [→](M_CE_CALCSCENARIOS-System-View.md) M_CE_CALCSCENARIOS_OVERVIEW System View [→](M_CE_CALCSCENARIOS_OVERVIEW-System-View.md) M_CE_CALCVIEW_DEPENDENCIES System View [→](M_CE_CALCVIEW_DEPENDENCIES-System-View.md)
