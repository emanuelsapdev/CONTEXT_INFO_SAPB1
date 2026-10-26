# 6.1.82 GRAPH_WORKSPACE_COLUMNS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1503

Provides information on the constituent entities and columns of graph workspaces.

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | The workspace schema name. |
| WORKSPACE_NAME | NVARCHAR(256) | The workspace name. |
| ENTITY_TYPE | NVARCHAR(6) | The entity type (VERTEX or EDGE). |
| ENTITY_SCHEMA_NAME | NVARCHAR(256) | The entity object schema name. |
| ENTITY_TABLE_NAME | NVARCHAR(256) | The entity object table or view name. |
| ENTITY_COLUMN_NAME | NVARCHAR(256) | The entity object column name. |
| ENTITY_ROLE | NVARCHAR(6) | The role of column (KEY, SOURCE, or TARGET. NULL for vertex or edge properties). |
| ENTITY_ROLE_POSITION | INTEGER | The position of the column in a composite key, source, or target (otherwise NULL). |

## Related Information

CREATE GRAPH WORKSPACE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-GRAPH-WORKSPACE-Statement-Data-Definition.md) DROP GRAPH WORKSPACE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-GRAPH-WORKSPACE-Statement-Data-Definition.md)
