# 6.2.35 M_CE_DEBUG_JSONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1675–1676

Provides all available JSONS (original, instantiated, or optimized) of a scenario for a concrete query.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCENARIO_NAME | NVARCHAR(256) | Displays the scenario name. |
| STATEMENT_ID | BIGINT | Displays the statement ID. |
| TYPE | VARCHAR(16) | Displays the JSON type: original, instantiated, optimized, or extrace. |
| MODEL_JSON | NCLOB | Displays the JSON string representing the calculation scenario. |
| EXECUTION_TIMESTAMP | TIMESTAMP | Displays the execution timestamp. |

## Related Information

M_CE_DEBUG_INFOS System View [→](M_CE_DEBUG_INFOS-System-View.md) M_CE_DEBUG_NODE_MAPPING System View [→](M_CE_DEBUG_NODE_MAPPING-System-View.md) M_DEBUG_SESSIONS System View [→](M_DEBUG_SESSIONS-System-View.md) M_DEBUG_CONNECTIONS System View [→](M_DEBUG_CONNECTIONS-System-View.md)
