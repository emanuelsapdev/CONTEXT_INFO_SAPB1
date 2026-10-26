# 6.1.51 CS_KEY_FIGURES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1455–1457

Provides information about the key figures defined for column store join views.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| VIEW_NAME | NVARCHAR(256) | Displays the join view name. |
| KEY_FIGURE_NAME | NVARCHAR(256) | Displays the key figure name. |
| DEFAULT_AGGREGATION_TYPE | VARCHAR(32) | Displays the aggregation type: SUM, COUNT, MIN, MAX, and so on. |
| DESCRIPTION | NVARCHAR(5000) | Displays the description. |
| UNIT_CONVERSION_NAME | NVARCHAR(256) | Displays the name of the unit conversion. |
| TABLE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the table. |
| TABLE_NAME | NVARCHAR(256) | Table name of column. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| EXPRESSION_FLAGS | VARCHAR(32) | Displays the expression flags. |
| EXPRESSION | NVARCHAR(256) | Displays the expression. |

## Related Information

CS_VIEW_PARAMETERS System View [→](CS_VIEW_PARAMETERS-System-View.md) CS_VIEW_COLUMNS System View [→](CS_VIEW_COLUMNS-System-View.md) CS_FREESTYLE_COLUMNS System View [→](CS_FREESTYLE_COLUMNS-System-View.md) CS_JOIN_TABLES System View [→](CS_JOIN_TABLES-System-View.md) CS_JOIN_PATHS System View [→](CS_JOIN_PATHS-System-View.md) CS_JOIN_CONSTRAINTS System View [→](CS_JOIN_CONSTRAINTS-System-View.md) CS_JOIN_CONDITIONS System View [→](CS_JOIN_CONDITIONS-System-View.md) CS_CONCAT_COLUMNS System View [→](CS_CONCAT_COLUMNS-System-View.md) CS_BO_VIEWS System View [→](CS_BO_VIEWS-System-View.md) M_CS_COLUMNS_PERSISTENCE System View [→](../6.02-Monitoring-Views/M_CS_COLUMNS_PERSISTENCE-System-View.md) M_CS_COLUMNS System View [→](../6.02-Monitoring-Views/M_CS_COLUMNS-System-View.md) M_CS_ALL_COLUMN_STATISTICS System View [→](../6.02-Monitoring-Views/M_CS_ALL_COLUMN_STATISTICS-System-View.md) M_CS_ALL_COLUMNS System View [→](../6.02-Monitoring-Views/M_CS_ALL_COLUMNS-System-View.md) CS_ALL_COLUMNS System View [→](CS_ALL_COLUMNS-System-View.md)
