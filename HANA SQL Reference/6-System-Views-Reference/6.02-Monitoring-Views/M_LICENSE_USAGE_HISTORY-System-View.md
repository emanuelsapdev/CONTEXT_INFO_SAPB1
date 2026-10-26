# 6.2.149 M_LICENSE_USAGE_HISTORY System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1851–1852

Information on the maximum resource consumption per time period, used for validity check of license installed on this system (if any).

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| PRODUCT_USAGE | BIGINT | Displays the maximum utilized amount of main memory used in this period in bytes. |
| PERIOD_START_TIME | TIMESTAMP | Displays the start time of the period that the maximum was used in. |
| PERIOD_END_TIME | TIMESTAMP | Displays the end time of the period the maximum was used in. |
| NUM_FAILED_MEASUREMENTS | INTEGER | Displays the number of failed measurements. |

## Related Information

M_LICENSE System View [→](M_LICENSE-System-View.md) M_LICENSES System View [→](M_LICENSES-System-View.md) M_LICENSE_MEASUREMENTS System View [→](M_LICENSE_MEASUREMENTS-System-View.md) M_LICENSE_MEASUREMENT_STATISTICS System View [→](M_LICENSE_MEASUREMENT_STATISTICS-System-View.md)
