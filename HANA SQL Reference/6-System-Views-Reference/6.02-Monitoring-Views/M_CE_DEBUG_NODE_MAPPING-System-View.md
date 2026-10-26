# 6.2.36 M_CE_DEBUG_NODE_MAPPING System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1676–1677

Provides information about node mapping between calculation nodes and Runtime nodes after execution.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| STATEMENT_ID | BIGINT | Displays the statement ID. |
| SCENARIO_NAME | NVARCHAR(256) | Displays the scenario name. |
| NODE_NAME | NVARCHAR(256) | Displays the calculation node name. |
| NODE_TYPE | VARCHAR(16) | Displays the calculation node type (ROOT, TEMPLATE, or CALC_DS). |
| SUCC_SCENARIO_NAME | NVARCHAR(256) | Displays the successor scenario name. |
| SUCC_NODE_NAME | NVARCHAR(256) | Displays the successor calculation node name. |
| RUNTIME_NODE_NAME | NVARCHAR(256) | Displays the runtime calculation node name. |
| RUNTIME_NODE_JSON | NCLOB | Displays the JSON string representing the calculation node. |
| EXECUTION_TIMESTAMP | TIMESTAMP | Displays the execution timestamp. |

## Related Information

M_CE_DEBUG_INFOS System View [→](M_CE_DEBUG_INFOS-System-View.md) M_CE_DEBUG_JSONS System View [→](M_CE_DEBUG_JSONS-System-View.md) M_DEBUG_SESSIONS System View [→](M_DEBUG_SESSIONS-System-View.md) M_DEBUG_CONNECTIONS System View [→](M_DEBUG_CONNECTIONS-System-View.md)
