# 6.1.45 CS_CONCAT_COLUMNS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1449–1450

Provides information on concat columns in the database.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the table. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name. |
| TABLE_OID | BIGINT | Displays the object ID of the table. |
| CONCAT_COLUMN_NAME | NVARCHAR(256) | Displays the concat column name. |
| POSITION | INTEGER | Displays the position of the column. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |

## Related Information

CS_ALL_COLUMNS System View [→](CS_ALL_COLUMNS-System-View.md) M_CS_ALL_COLUMNS System View [→](../6.02-Monitoring-Views/M_CS_ALL_COLUMNS-System-View.md) M_CS_ALL_COLUMN_STATISTICS System View [→](../6.02-Monitoring-Views/M_CS_ALL_COLUMN_STATISTICS-System-View.md) M_CS_COLUMNS System View [→](../6.02-Monitoring-Views/M_CS_COLUMNS-System-View.md) M_CS_COLUMNS_PERSISTENCE System View [→](../6.02-Monitoring-Views/M_CS_COLUMNS_PERSISTENCE-System-View.md) CS_BO_VIEWS System View [→](CS_BO_VIEWS-System-View.md) CS_FREESTYLE_COLUMNS System View [→](CS_FREESTYLE_COLUMNS-System-View.md) CS_JOIN_CONDITIONS System View [→](CS_JOIN_CONDITIONS-System-View.md) CS_JOIN_CONSTRAINTS System View [→](CS_JOIN_CONSTRAINTS-System-View.md) CS_JOIN_PATHS System View [→](CS_JOIN_PATHS-System-View.md) CS_JOIN_TABLES System View [→](CS_JOIN_TABLES-System-View.md) CS_KEY_FIGURES System View [→](CS_KEY_FIGURES-System-View.md) CS_VIEW_COLUMNS System View [→](CS_VIEW_COLUMNS-System-View.md) CS_VIEW_PARAMETERS System View [→](CS_VIEW_PARAMETERS-System-View.md) CONCAT Function (String) [→](../../4-SQL-Reference/4.09-SQL-Functions/4.09.01-Functions-A-Z/CONCAT-Function-String.md)
