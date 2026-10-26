# 6.2.147 M_LICENSE_MEASUREMENTS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1850

Product usage measurements for licensing.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| GLAS_APPLICATION_ID | VARCHAR(6) | Displays the license ID for the software product. |
| MEASURE_TIME | TIMESTAMP | Displays the the measurement completion time. |
| VALUE | BIGINT | Displays the measured value in bytes. This value is NULLwhen the measurement fails. |
| SUCCESSFUL | VARCHAR(5) | Indicates whether or not the measurement was successful: TRUE/FALSE. |

## Related Information

M_LICENSE_MEASUREMENT_STATISTICS System View [→](M_LICENSE_MEASUREMENT_STATISTICS-System-View.md) M_LICENSE System View [→](M_LICENSE-System-View.md) M_LICENSES System View [→](M_LICENSES-System-View.md)
