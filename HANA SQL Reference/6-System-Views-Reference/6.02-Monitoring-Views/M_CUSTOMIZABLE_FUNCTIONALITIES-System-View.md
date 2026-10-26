# 6.2.70 M_CUSTOMIZABLE_FUNCTIONALITIES System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1736

Provides information about the enablement status of restricted features in databases. The full content of this view is only accessible from the system database.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| NAME | VARCHAR (64) | Displays the customizable functionality name. |
| DESCRIPTION | VARCHAR (256) | Displays the customizable functionality description. |
| IS_ENABLED | VARCHAR (5) | Indicates whether the customizable functionality is enabled: TRUE/FALSE. |

## Related Information

M_FEATURES System View [→](M_FEATURES-System-View.md) M_FEATURE_USAGE System View [→](M_FEATURE_USAGE-System-View.md)
