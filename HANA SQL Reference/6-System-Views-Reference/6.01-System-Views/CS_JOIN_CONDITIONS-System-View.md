# 6.1.47 CS_JOIN_CONDITIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1451–1452

Provides join conditions for column store join views.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| VIEW_NAME | NVARCHAR(256) | Displays the join view name. |
| JOIN_CONDITION_NAME | NVARCHAR(256) | Displays the join condition name. |
| JOIN_ORDER | BIGINT | Displays the join order number. |
| TABLE_SCHEMA_NAME1 | NVARCHAR(256) | Displays the schema name of column 1. |
| TABLE_NAME1 | NVARCHAR(256) | Displays the table name of COLUMN_NAME1. |
| COLUMN_NAME1 | NVARCHAR(256) | Displays the name of COLUMN_NAME1. |
| ALIAS_NUMBER1 | INTEGER | Displays the alias number of TABLE_NAME1. |
| TABLE_SCHEMA_NAME2 | NVARCHAR(256) | Displays the schema name of TABEL_NAME2. |
| TABLE_NAME2 | NVARCHAR(256) | Displays the table name of COLUMN_NAME2. |
| COLUMN_NAME2 | NVARCHAR(256) | Displays the name of COLUMN_NAME2. |
| ALIAS_NUMBER2 | INTEGER | Displays the alias number of TABLE_NAME2. |
| CONSTRAINTS | NVARCHAR(256) | Displays the join constraint name. |
| JOIN_TYPE | VARCHAR(5) | Displays the join type: INNER, LEFT, RIGHT, FULL. |
| CARDINALITY | VARCHAR(3) | Displays the join cardinality: 1:1, 1:n, n:1, n:n. |

## Related Information

M_TEMPORARY_JOIN_CONDITIONS System View [→](../6.02-Monitoring-Views/M_TEMPORARY_JOIN_CONDITIONS-System-View.md) CS_JOIN_CONSTRAINTS System View [→](CS_JOIN_CONSTRAINTS-System-View.md) CS_JOIN_PATHS System View [→](CS_JOIN_PATHS-System-View.md) CS_JOIN_TABLES System View [→](CS_JOIN_TABLES-System-View.md) CS_ALL_COLUMNS System View [→](CS_ALL_COLUMNS-System-View.md) M_CS_ALL_COLUMNS System View [→](../6.02-Monitoring-Views/M_CS_ALL_COLUMNS-System-View.md) M_CS_ALL_COLUMN_STATISTICS System View [→](../6.02-Monitoring-Views/M_CS_ALL_COLUMN_STATISTICS-System-View.md) M_CS_COLUMNS System View [→](../6.02-Monitoring-Views/M_CS_COLUMNS-System-View.md) M_CS_COLUMNS_PERSISTENCE System View [→](../6.02-Monitoring-Views/M_CS_COLUMNS_PERSISTENCE-System-View.md) CS_BO_VIEWS System View [→](CS_BO_VIEWS-System-View.md) CS_CONCAT_COLUMNS System View [→](CS_CONCAT_COLUMNS-System-View.md) CS_KEY_FIGURES System View [→](CS_KEY_FIGURES-System-View.md) CS_VIEW_COLUMNS System View [→](CS_VIEW_COLUMNS-System-View.md) CS_VIEW_PARAMETERS System View [→](CS_VIEW_PARAMETERS-System-View.md) SELECT Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.144-SELECT/README.md)
