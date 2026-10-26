# 6.2.148 M_LICENSE_MEASUREMENT_STATISTICS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1850–1851

Collects license measurement statistics from tenant databases.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| YEAR | INTEGER | Displays the year. |
| MONTH | INTEGER | Displays the month. |
| GLAS_APPLICATION_ID | VARCHAR(6) | Displays the license ID for the software product. |
| PEAK_VALUE | BIGINT | Displays the peak value of the application for the given month and year in bytes. |

## Related Information

M_LICENSE_MEASUREMENTS System View [→](M_LICENSE_MEASUREMENTS-System-View.md) M_LICENSE_USAGE_HISTORY System View [→](M_LICENSE_USAGE_HISTORY-System-View.md) M_LICENSE System View [→](M_LICENSE-System-View.md) M_LICENSES System View [→](M_LICENSES-System-View.md)
