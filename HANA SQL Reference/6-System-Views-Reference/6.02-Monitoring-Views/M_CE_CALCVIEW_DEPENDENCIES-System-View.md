# 6.2.33 M_CE_CALCVIEW_DEPENDENCIES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1674

Provides all views that are referencing a CalculationScenario.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the column view. |
| VIEW_NAME | NVARCHAR(256) | Displays the column view name. |
| CALCNODE_NAME | NVARCHAR(256) | Displays the referenced calculation node name. |
| SCENARIO_NAME | NVARCHAR(256) | Displays the scenario name. |

## Related Information

M_CE_CALCSCENARIOS System View [→](M_CE_CALCSCENARIOS-System-View.md) M_CE_CALCSCENARIOS_OVERVIEW System View [→](M_CE_CALCSCENARIOS_OVERVIEW-System-View.md) M_CE_CALCSCENARIO_HINTS System View [→](M_CE_CALCSCENARIO_HINTS-System-View.md)
