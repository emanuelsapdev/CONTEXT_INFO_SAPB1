# 6.2.31 M_CE_CALCSCENARIOS_OVERVIEW System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1672–1673

Provides an overview of Calcscenarios without JSON representation.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCENARIO_NAME | NVARCHAR(256) | Displays the scenario name. |
| IS_PERSISTENT | VARCHAR(5) | Indicates if the calculation scenario is persistent or transient: TRUE/FALSE. |
| CREATE_TIME | TIMESTAMP | Displays the creation time. |
| MEMORY_SIZE | BIGINT | Displays the memory size of the loaded calculation scenario model in bytes. |
| COMPONENT | NVARCHAR(256) | Displays the component that create the calculation scenario. |

## Related Information

M_CE_CALCSCENARIOS System View [→](M_CE_CALCSCENARIOS-System-View.md) M_CE_CALCSCENARIO_HINTS System View [→](M_CE_CALCSCENARIO_HINTS-System-View.md) M_CE_CALCVIEW_DEPENDENCIES System View [→](M_CE_CALCVIEW_DEPENDENCIES-System-View.md)
