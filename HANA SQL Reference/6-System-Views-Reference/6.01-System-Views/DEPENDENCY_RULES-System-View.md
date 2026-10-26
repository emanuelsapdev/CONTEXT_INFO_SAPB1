# 6.1.56 DEPENDENCY_RULES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1466–1467

For internal use only. Provides a list of dependency rules in the system.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| DEPENDENCY_RULE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of dependency rule. |
| DEPENDENCY_RULE_NAME | NVARCHAR(256) | Displays the name of dependency rule. |
| DEPENDENCY_RULE_TYPE | VARCHAR(6) | Displays the type of dependency rule. |
| DEFINITION | NVARCHAR(5000) | Definition of dependency rule |

## Related Information

[DEPENDENCY_RULE_COLUMNS System View](DEPENDENCY_RULE_COLUMNS-System-View.md)
