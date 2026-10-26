# 6.2.265 M_SERVICE_TYPES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 2007

Provides information about service types.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SERVICE_NAME | VARCHAR(32) | Displays the service name. |
| INIFILE | VARCHAR(36) | Displays the configuration file name of service. |
| HAS_DETAIL | VARCHAR(5) | Displays whether the service shows details in M_SERVICE_STATISTICS: TRUE/FALSE. |

## Related Information

[M_SERVICE_STATISTICS System View](M_SERVICE_STATISTICS-System-View.md)
