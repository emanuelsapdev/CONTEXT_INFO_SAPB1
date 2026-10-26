# 6.1.33 CDS_VIEWS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1437–1438

Provides definitions for CDS views.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| VIEW_NAME | NVARCHAR(127) | Displays the view name. |
| EXTENSION_PACKAGE_NAME | NVARCHAR(127) | Displays the extension package name. |
| DEFINITION | NCLOB | Displays the original definition of the view, similar to how it is found in the CDS resource file, but with the relative names resolved to absolute names, and constant expressions resolved to concrete values. |

## Related Information

CDS_ANNOTATION_ASSIGNMENTS System View [→](CDS_ANNOTATION_ASSIGNMENTS-System-View.md) CDS_ANNOTATION_VALUES System View [→](CDS_ANNOTATION_VALUES-System-View.md) CDS_ARTIFACT_NAMES System View [→](CDS_ARTIFACT_NAMES-System-View.md) CDS_ASSOCIATIONS System View [→](CDS_ASSOCIATIONS-System-View.md) CDS_ENTITIES System View [→](CDS_ENTITIES-System-View.md)
