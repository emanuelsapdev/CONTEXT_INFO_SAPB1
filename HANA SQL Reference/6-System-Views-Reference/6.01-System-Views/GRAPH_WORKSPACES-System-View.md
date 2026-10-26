# 6.1.83 GRAPH_WORKSPACES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1503–1505

Provides information about graph workspaces in the database.

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR (256) | Displays the name of the schema the workspace resides in. |
| WORKSPACE_NAME | NVARCHAR (256) | Displays the workspace name. |
| CREATE_TIMESTAMP | TIMESTAMP | Displays the workspace creation time stamp. |
| USER_NAME | NVARCHAR (256) | Displays the workspace creator user name. |
| EDGE_SCHEMA_NAME | NVARCHAR (256) | Displays the schema name of work space edge table. |
| EDGE_TABLE_NAME | NVARCHAR (256) | Displays the workspace edge table name. |
| EDGE_SOURCE_COLUMN_NAME | NVARCHAR (256) | Displays the workspace source column name in the edge table. |
| EDGE_TARGET_COLUMN_NAME | NVARCHAR (256) | Displays the workspace target column name in the edge table. |
| EDGE_KEY_COLUMN_NAME | NVARCHAR (256) | Displays the workspace key column name in the edge table. |
| VERTEX_SCHEMA_NAME | NVARCHAR (256) | Displays the schema name of the work space vertex table. |
| VERTEX_TABLE_NAME | NVARCHAR (256) | Displays the workspace vertex table name. |
| VERTEX_KEY_COLUMN_NAME | NVARCHAR (256) | Displays the workspace key column name in the vertex table. |
| IS_VALID | VARCHAR (5) | Displays whether this workspace is valid: TRUE/FALSE. |

## Related Information

CREATE GRAPH WORKSPACE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/CREATE-GRAPH-WORKSPACE-Statement-Data-Definition.md) DROP GRAPH WORKSPACE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/DROP-GRAPH-WORKSPACE-Statement-Data-Definition.md)
