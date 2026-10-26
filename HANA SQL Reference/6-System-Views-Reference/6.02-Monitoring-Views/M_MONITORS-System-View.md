# 6.2.181 M_MONITORS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1903–1904

Provides available monitoring view information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| VIEW_NAME | NVARCHAR(256) | Displays the name of the monitoring view. |
| DESCRIPTION | NVARCHAR(2000) | Displays the short description of the monitoring view. |
| RESETTABLE | VARCHAR(5) | Indicates whether or not the values of this view can be reset: TRUE/FALSE. |

## Additional Information

This view can be used in conjunction with the M_MONITOR_COLUMNS system view to get information about existing monitoring views.

## Related Information

M_MONITOR_COLUMNS System View [→](M_MONITOR_COLUMNS-System-View.md) ALTER SYSTEM RESET MONITORING VIEW Statement (System Management) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/4.10.01.19-ALTER-SYSTEM-Statements/ALTER-SYSTEM-RESET-MONITORING-VIEW-Statement-System.md)
