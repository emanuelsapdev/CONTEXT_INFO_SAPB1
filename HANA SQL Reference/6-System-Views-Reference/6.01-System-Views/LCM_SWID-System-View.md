# 6.1.98 LCM_SWID System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1516–1517

Provides all software ID tags for installed software.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SWID | VARCHAR(36) | Displays the SWID tag ID. |
| SWID_NAME | VARCHAR(64) | Displays the SWID name. |
| ENTITY_NAME | VARCHAR(64) | Displays the entity name (Vendor). |
| ENTITY_REGID | VARCHAR(64) | Displays the entity registration ID (Vendor). |
| ENTITY_ROLE | VARCHAR(64) | Displays the vendor roles. |
| ENTITLEMENT_REQUIRED | VARCHAR(5) | Displays whether the SWID for the PV is available with tag entitlementDataRe quired: TRUE/FALSE (default). |
| PRODUCT_NAME | VARCHAR(30) | Displays the link to technical name of the product (LCM_PRODUCTS). |

## Related Information

LCM_SOFTWARE_COMPONENTS System View [→](LCM_SOFTWARE_COMPONENTS-System-View.md) LCM_PRODUCT_INSTANCES_INCLUDED System View [→](LCM_PRODUCT_INSTANCES_INCLUDED-System-View.md) LCM_PRODUCTS System View [→](LCM_PRODUCTS-System-View.md) LCM_PRODUCT_INSTANCES System View [→](LCM_PRODUCT_INSTANCES-System-View.md)
