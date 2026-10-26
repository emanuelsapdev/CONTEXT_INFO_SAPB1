# 6.2.114 M_FEATURES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1799–1800

Provides information about all supported features.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| COMPONENT_NAME | VARCHAR(32) | Displays the name of the component owning the feature. |
| FEATURE_NAME | VARCHAR(32) | Displays the name of the feature. |
| FEATURE_VERSION | BIGINT | Displays the version of the feature. |

## Related Information

[M_FEATURE_USAGE System View](M_FEATURE_USAGE-System-View.md)
