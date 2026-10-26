# 6.1.57 DEPENDENCY_RULE_COLUMNS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1467–1468

For internal use only. Provides a list dependency rule columns in the system.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| DEPENDENCY_RULE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the dependency rule. |
| DEPENDENCY_RULE_NAME | NVARCHAR(256) | Displays the name of the dependency rule. |
| OBJECT_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the table that contains the column. |
| OBJECT_NAME | NVARCHAR(256) | Displays the name of the table that contains the column |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |

## Related Information

[DEPENDENCY_RULES System View](DEPENDENCY_RULES-System-View.md)
