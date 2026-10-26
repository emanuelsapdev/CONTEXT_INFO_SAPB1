# 6.1.49 CS_JOIN_PATHS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1453–1454

Provides join paths for column store join views.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| VIEW_NAME | NVARCHAR(256) | Displays the join view name. |
| JOIN_PATH_NAME | NVARCHAR(256) | Displays the join path name. |
| JOIN_CONDITIONS | NVARCHAR(5000) | Displays the comma separated list of join conditions. |
| JOIN_CONSTRAINTS | NVARCHAR(5000) | Displays the comma separated list of join constraints. |

## Related Information

CS_JOIN_CONSTRAINTS System View [→](CS_JOIN_CONSTRAINTS-System-View.md) CS_JOIN_CONDITIONS System View [→](CS_JOIN_CONDITIONS-System-View.md) CS_JOIN_TABLES System View [→](CS_JOIN_TABLES-System-View.md) M_TEMPORARY_JOIN_CONSTRAINTS System View [→](../6.02-Monitoring-Views/M_TEMPORARY_JOIN_CONSTRAINTS-System-View.md) CS_ALL_COLUMNS System View [→](CS_ALL_COLUMNS-System-View.md) CS_BO_VIEWS System View [→](CS_BO_VIEWS-System-View.md) CS_CONCAT_COLUMNS System View [→](CS_CONCAT_COLUMNS-System-View.md) CS_FREESTYLE_COLUMNS System View [→](CS_FREESTYLE_COLUMNS-System-View.md) CS_KEY_FIGURES System View [→](CS_KEY_FIGURES-System-View.md) CS_VIEW_COLUMNS System View [→](CS_VIEW_COLUMNS-System-View.md) CS_VIEW_PARAMETERS System View [→](CS_VIEW_PARAMETERS-System-View.md)
