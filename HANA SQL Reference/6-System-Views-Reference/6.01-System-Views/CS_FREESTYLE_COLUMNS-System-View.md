# 6.1.46 CS_FREESTYLE_COLUMNS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1450–1451

Provides freestyle search columns for column store join views.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| VIEW_NAME | NVARCHAR(256) | Displays the join view name. |
| COLUMN_NAME | NVARCHAR(256) | Displays the freestyle column name. |
| WEIGHT | REAL | Displays the freestyle weight. |
| IS_ALPHANUM_SEACH | VARCHAR(5) | Displays whether the freestyle search type lis alphanumeric: TRUE/FALSE. |

## Related Information

CS_ALL_COLUMNS System View [→](CS_ALL_COLUMNS-System-View.md) M_CS_ALL_COLUMNS System View [→](../6.02-Monitoring-Views/M_CS_ALL_COLUMNS-System-View.md) M_CS_ALL_COLUMN_STATISTICS System View [→](../6.02-Monitoring-Views/M_CS_ALL_COLUMN_STATISTICS-System-View.md) M_CS_COLUMNS System View [→](../6.02-Monitoring-Views/M_CS_COLUMNS-System-View.md) M_CS_COLUMNS_PERSISTENCE System View [→](../6.02-Monitoring-Views/M_CS_COLUMNS_PERSISTENCE-System-View.md) CS_BO_VIEWS System View [→](CS_BO_VIEWS-System-View.md) CS_CONCAT_COLUMNS System View [→](CS_CONCAT_COLUMNS-System-View.md) CS_JOIN_CONDITIONS System View [→](CS_JOIN_CONDITIONS-System-View.md) CS_JOIN_CONSTRAINTS System View [→](CS_JOIN_CONSTRAINTS-System-View.md) CS_JOIN_PATHS System View [→](CS_JOIN_PATHS-System-View.md) CS_JOIN_TABLES System View [→](CS_JOIN_TABLES-System-View.md) CS_KEY_FIGURES System View [→](CS_KEY_FIGURES-System-View.md) CS_VIEW_COLUMNS System View [→](CS_VIEW_COLUMNS-System-View.md) CS_VIEW_PARAMETERS System View [→](CS_VIEW_PARAMETERS-System-View.md)
