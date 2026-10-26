# 6.1.97 LCM_SOFTWARE_COMPONENTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1515–1516

Provides all installed software component versions.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| VENDOR_NAME | VARCHAR(30) | Displays the name of the vendor, for example, sap.com. |
| COMPONENT_NAME | VARCHAR(30) | Displays the technical name of the software component version. |
| VERSION | VARCHAR(30) | Displays the version of the delivery unit (=SWC), for example, 1. |
| VERSION_SP | VARCHAR(16) | Displays the number of the SP, for example, 3. |
| VERSION_PATCH | VARCHAR(16) | Displays the number of the patch, for example, 37. |
| PPMS_ID | VARCHAR(20) | Displays the technical ID of the software component version, for example, the one identifying it in PPMS. |
| COMPONENT_DESCRIPTION | VARCHAR(64) | Displays the human-readable name of the software component version. |
| SP_NAME | VARCHAR(30) | Displays the technical name of the support package, for example, SAPK-10000INATEST2 or SP000. |
| SP_DESCRIPTION | VARCHAR(64) | Displays the human-readable name of the support package. |
| SP_PPMS_ID | VARCHAR(20) | Displays the 20-digit PPMS number of the installed support package. |

## Related Information

LCM_PRODUCT_INSTANCES_INCLUDED System View [→](LCM_PRODUCT_INSTANCES_INCLUDED-System-View.md) LCM_PRODUCTS System View [→](LCM_PRODUCTS-System-View.md) LCM_PRODUCT_INSTANCES System View [→](LCM_PRODUCT_INSTANCES-System-View.md)

[LCM_SWID System View](LCM_SWID-System-View.md)
