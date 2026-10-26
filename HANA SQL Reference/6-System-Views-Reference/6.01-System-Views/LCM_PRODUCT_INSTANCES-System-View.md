# 6.1.95 LCM_PRODUCT_INSTANCES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1513–1514

Provides information about all installed product instances.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| VENDOR_NAME | VARCHAR(30) | Displays the name of the vendor. For example, sap.com. |
| PRODUCT_NAME | VARCHAR(30) | Displays the technical name of the product. |
| INSTANCE_ID | VARCHAR(3) | Displays the instance key. |
| PPMS_ID | VARCHAR(20) | Displays the PPMS 2.0 PI number. |
| INSTANCE_DESCRIPTION | VARCHAR(64) | Displays the human-readable name of the product instance. |

## Related Information

LCM_PRODUCTS System View [→](LCM_PRODUCTS-System-View.md) LCM_PRODUCT_INSTANCES_INCLUDED System View [→](LCM_PRODUCT_INSTANCES_INCLUDED-System-View.md) LCM_SOFTWARE_COMPONENTS System View [→](LCM_SOFTWARE_COMPONENTS-System-View.md) LCM_SWID System View [→](LCM_SWID-System-View.md)
