# 6.2.138 M_JOB_HISTORY_INFO System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1832–1833

Provides a history of long running system operations.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| JOB_NAME | NVARCHAR(128) | Displays the type of operation. |
| DESCRIPTION | VARCHAR(256) | Displays the job description. |
| DISPLAY_NAME | VARCHAR(128) | Displays the recommended display name. |
| DISPLAY_LINE_COLOR | INTEGER(10) | Displays the recommended display line color as RGB. |
| DISPLAY_LINE_STYLE | TINYINT(3) | Displays the recommended display line style: 1=solid, 2=dotted, 3=dashed. |

## Related Information

[M_JOB_PROGRESS System View](M_JOB_PROGRESS-System-View.md)
