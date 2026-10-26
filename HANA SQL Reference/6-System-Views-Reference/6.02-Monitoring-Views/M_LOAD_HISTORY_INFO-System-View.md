# 6.2.161 M_LOAD_HISTORY_INFO System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1873–1874

Load history KPI description.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| VIEW_NAME | NVARCHAR(256) | Displays the view name where the KPI can be found. |
| COLUMN_NAME | NVARCHAR(256) | Displays the column name where the KPI can be found. |
| IS_CUMULATIVE | VARCHAR(5) | Displays the cumulative KPIs that re turn a relative value since the previous sample. Noncumulative KPIs return an absolute value for the current point in time. |
| SQL_SOURCE | VARCHAR(256) | Displays the equivalent SQL statement. |
| DESCRIPTION | VARCHAR(256) | Displays the KPI description. |
| SAMPLE_UNIT | VARCHAR(16) | Displays the sample unit. |
| DISPLAY_HIERARCHY | VARCHAR(8) | Displays the recommended display hierarchy/sorting criteria. |
| DISPLAY_NAME | VARCHAR(32) | Displays the recommended display name. |
| DISPLAY_UNIT | VARCHAR(16) | Displays the recommended display unit. |
| DISPLAY_LINE_COLOR | INTEGER | Displays the recommended display line color as RGB. |
| DISPLAY_LINE_STYLE | TINYINT | Displays the recommended display line style: 1=solid, 2=dotted, or 3=dashed. |
| DISPLAY_DIVIDER | INTEGER | Displays the divider to convert SAMPLE_UNIT in DISPLAY_UNIT. |
| DISPLAY_Y_SCALE | TINYINT | Indicates that the KPIs with the same value should be shown with the same Y scale in a chart. Special value 1 is used for CPU KPIs with a fixed Y scale of 100. |

## Related Information

M_LOAD_HISTORY_HOST System View [→](M_LOAD_HISTORY_HOST-System-View.md) M_LOAD_HISTORY_SERVICE System View [→](M_LOAD_HISTORY_SERVICE-System-View.md) LOAD Statement (Data Manipulation) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/LOAD-Statement-Data-Manipulation.md) PERSISTENCE_HISTORY System View [→](../6.01-System-Views/PERSISTENCE_HISTORY-System-View.md)
