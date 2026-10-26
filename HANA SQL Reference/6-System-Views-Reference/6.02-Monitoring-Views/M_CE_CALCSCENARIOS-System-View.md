# 6.2.30 M_CE_CALCSCENARIOS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1671–1672

Provides all available calculation scenarios.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| SCENARIO_NAME | NVARCHAR(256) | Displays the scenario name. |
| IS_PERSISTENT | VARCHAR(5) | Indicates if the calculation scenario is persistent or transient: TRUE or FALSE. |
| FLAGS | BIGINT | Displays the calculation scenario flags. |
| CREATE_TIME | TIMESTAMP | Displays the creation time. |
| MEMORY_SIZE | BIGINT | Displays the memory size of the loaded calculation scenario model in bytes. |
| COMPONENT | NVARCHAR(256) | Displays the component that created the calculation scenario. |
| SCENARIO_VERSION | NVARCHAR(256) | Displays the scenario version of the calculation scenario. |
| JSON | NCLOB | Displays the JSON string representing the calculation scenario. |

## Related Information

M_CE_CALCSCENARIOS_OVERVIEW System View [→](M_CE_CALCSCENARIOS_OVERVIEW-System-View.md) M_CE_CALCSCENARIO_HINTS System View [→](M_CE_CALCSCENARIO_HINTS-System-View.md) M_CE_CALCVIEW_DEPENDENCIES System View [→](M_CE_CALCVIEW_DEPENDENCIES-System-View.md)
