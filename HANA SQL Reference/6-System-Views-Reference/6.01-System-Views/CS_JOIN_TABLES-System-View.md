# 6.1.50 CS_JOIN_TABLES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1454–1455

Provides information about the physical tables referred to by column store join views.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| VIEW_NAME | NVARCHAR(256) | Displays the join view name. |
| TABLE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the physical table. |
| TABLE_NAME | NVARCHAR(256) | Displays the physical table name. |
| TABLE_TYPE | VARCHAR(32) | Displays the type of table: FACT_TABLE, D_TABLE, X_TABLE, Y_TABLE, TEMP_TABLE, S_TABLE, EXTERNAL_OBJECT, CONVERSION_TABLE, OLAP_TEXT_TABLE, or AUTHORIZATION_TABLE, HIERARCHY. |

## Related Information

CS_JOIN_PATHS System View [→](CS_JOIN_PATHS-System-View.md) CS_JOIN_CONSTRAINTS System View [→](CS_JOIN_CONSTRAINTS-System-View.md) CS_JOIN_CONDITIONS System View [→](CS_JOIN_CONDITIONS-System-View.md) M_TEMPORARY_JOIN_CONSTRAINTS System View [→](../6.02-Monitoring-Views/M_TEMPORARY_JOIN_CONSTRAINTS-System-View.md) CS_ALL_COLUMNS System View [→](CS_ALL_COLUMNS-System-View.md) CS_BO_VIEWS System View [→](CS_BO_VIEWS-System-View.md) CS_CONCAT_COLUMNS System View [→](CS_CONCAT_COLUMNS-System-View.md) CS_FREESTYLE_COLUMNS System View [→](CS_FREESTYLE_COLUMNS-System-View.md) CS_KEY_FIGURES System View [→](CS_KEY_FIGURES-System-View.md) CS_VIEW_COLUMNS System View [→](CS_VIEW_COLUMNS-System-View.md) CS_VIEW_PARAMETERS System View [→](CS_VIEW_PARAMETERS-System-View.md)
