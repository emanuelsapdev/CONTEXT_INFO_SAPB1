# 6.1.94 LCM_PRODUCTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1512–1513

Provides information about all installed product versions.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| VENDOR_NAME | VARCHAR(30) | Dispalys the vendor name, for example, sap.com. |
| PRODUCT_NAME | VARCHAR(30) | Displays the technical name of the product. |
| VERSION | VARCHAR(30) | Displays the version number of the PPMS product version, for example, 1.0. |
| PPMS_ID | VARCHAR(30) | Displays the technical ID of the product version, for example, the version one identifying it in PPMS. |
| PRODUCT_DESCRIPTION | VARCHAR(30) | Displays the human-readable name of the product. |
| SP_STACK_ID | VARCHAR(30) | Displays the SP stack ID of the PPMS product version. |
| SP_STACK_DESCRIPTION | VARCHAR(30) | Displasy the human-readable name or description of the SP stack. |

## Related Information

LCM_PRODUCT_INSTANCES System View [→](LCM_PRODUCT_INSTANCES-System-View.md) LCM_PRODUCT_INSTANCES_INCLUDED System View [→](LCM_PRODUCT_INSTANCES_INCLUDED-System-View.md) LCM_SOFTWARE_COMPONENTS System View [→](LCM_SOFTWARE_COMPONENTS-System-View.md) LCM_SWID System View [→](LCM_SWID-System-View.md)
