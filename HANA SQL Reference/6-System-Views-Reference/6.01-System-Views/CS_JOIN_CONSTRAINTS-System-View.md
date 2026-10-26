# 6.1.48 CS_JOIN_CONSTRAINTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1452–1453

Provides join constraints for column store join views.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| VIEW_NAME | NVARCHAR(256) | Displays the join view name. |
| JOIN_CONSTRAINT_NAME | NVARCHAR(256) | Displays the join constraint name. |
| CONSTRAINT_TYPE | VARCHAR(32) | Displays the type of constraint owner. |
| LOCATION | NVARCHAR(256) | Displays the name of constraint owner. |
| TABLE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the table. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name of the column. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| OPERATOR | NVARCHAR(256) | Displays the operator. |
| VALUE | NVARCHAR(5000) | Displays the value. |

## Related Information

CS_JOIN_CONDITIONS System View [→](CS_JOIN_CONDITIONS-System-View.md) CS_JOIN_PATHS System View [→](CS_JOIN_PATHS-System-View.md) CS_JOIN_TABLES System View [→](CS_JOIN_TABLES-System-View.md) M_TEMPORARY_JOIN_CONSTRAINTS System View [→](../6.02-Monitoring-Views/M_TEMPORARY_JOIN_CONSTRAINTS-System-View.md) CONSTRAINTS System View [→](CONSTRAINTS-System-View.md) REFERENTIAL_CONSTRAINTS System View [→](REFERENTIAL_CONSTRAINTS-System-View.md) System Limitations [→](../../4-SQL-Reference/4.11-System-Limitations.md) CS_ALL_COLUMNS System View [→](CS_ALL_COLUMNS-System-View.md) CS_BO_VIEWS System View [→](CS_BO_VIEWS-System-View.md) CS_CONCAT_COLUMNS System View [→](CS_CONCAT_COLUMNS-System-View.md) CS_FREESTYLE_COLUMNS System View [→](CS_FREESTYLE_COLUMNS-System-View.md) CS_KEY_FIGURES System View [→](CS_KEY_FIGURES-System-View.md) CS_VIEW_COLUMNS System View [→](CS_VIEW_COLUMNS-System-View.md) CS_VIEW_PARAMETERS System View [→](CS_VIEW_PARAMETERS-System-View.md)
