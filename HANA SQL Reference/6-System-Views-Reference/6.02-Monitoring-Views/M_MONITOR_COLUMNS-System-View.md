# 6.2.182 M_MONITOR_COLUMNS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1904–1906

All the columns in the monitoring views.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| VIEW_NAME | NVARCHAR(256) | Displays the name of the monitoring view. |
| VIEW_COLUMN_NAME | NVARCHAR(256) | Displays the name of the monitoring view column. |
| DATA_TYPE_ID | SMALLINT | Displays the column data type ID. |
| DATA_TYPE_NAME | VARCHAR(16) | Displays the column data type name. |
| POSITION | INTEGER | Displays the ordinal position of the column in a record. |
| DEFAULT_VALUE | NVARCHAR(5000) | Displays the default value. |
| UNIT | VARCHAR(16) | Displays the unit for the value. |
| COLLATION | NVARCHAR(256) | Displays the collation. |
| LENGTH | INTEGER | Displays the length. |
| SCALE | INTEGER | Displays the scale. |
| IS_NULLABLE | VARCHAR(5) | Indicates whether or not a NULL value is allowed: TRUE/FALSE. |
| DESCRIPTION | NVARCHAR(5000) | Displays the short description of the monitoring view column. |

## Additional Information

This view can be used in conjunction with the M_MONITORS system view to get information about existing monitoring views.

## Related Information

[M_MONITORS System View](M_MONITORS-System-View.md)
