# 6.2.325 M_TEMPORARY_KEY_FIGURES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2100–2101

Provides information about temporary key figures.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| VIEW_NAME | NVARCHAR(256) | Displays the join view name. |
| KEY_FIGURE_NAME | NVARCHAR(256) | Displays the key figure name. |
| DEFAULT_AGGREGATION_TYPE | VARCHAR(32) | Displays the aggregation type. |
| DESCRIPTION | NVARCHAR(5000) | Displays the description. |
| UNIT_CONVERSION_NAME | NVARCHAR(256) | Displays the name of the unit conversion. |
| TABLE_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the column. |
| TABLE_NAME | NVARCHAR(256) | Displays the table name of the column. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name. |
| EXPRESSION_FLAGS | VARCHAR(32) | Displays the expression flags. |
| EXPRESSION | NVARCHAR(256) | Displays the expression. |

## Related Information

[CS_KEY_FIGURES System View](../6.01-System-Views/CS_KEY_FIGURES-System-View.md)
