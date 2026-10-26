# 6.2.34 M_CE_DEBUG_INFOS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1674–1675

Provides debug information after the execution of a calculation scenario.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port number. |
| SCENARIO_NAME | NVARCHAR(256) | Displays the scenario name. |
| NODE_NAME | NVARCHAR(256) | Displays the calculation node name. |
| STATEMENT_ID | BIGINT | Displays the statement ID. |
| DEBUG_TYPE_MASK | BIGINT | Displays the bit mask indicating the type of debug information. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name (temporary intermediate result table). |
| COLUMN_NAMES | CLOB | Displays the column names. |
| TABLE_SIZE | BIGINT | Displays the table size in bytes (temporary intermediate result table). |
| EXECUTION_TIMESTAMP | TIMESTAMP | Displays the execution timestamp. |
| APPLICATION_QUERY_ID | NVARCHAR(256) | Displays the application query ID. |

## Related Information

M_CE_DEBUG_JSONS System View [→](M_CE_DEBUG_JSONS-System-View.md) M_CE_DEBUG_NODE_MAPPING System View [→](M_CE_DEBUG_NODE_MAPPING-System-View.md) M_DEBUG_SESSIONS System View [→](M_DEBUG_SESSIONS-System-View.md) M_DEBUG_CONNECTIONS System View [→](M_DEBUG_CONNECTIONS-System-View.md)
