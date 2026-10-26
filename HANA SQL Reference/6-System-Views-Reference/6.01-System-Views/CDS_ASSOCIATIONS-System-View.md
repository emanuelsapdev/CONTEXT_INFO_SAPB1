# 6.1.31 CDS_ASSOCIATIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1435–1436

Provides definitions for CDS associations.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| ASSOCIATION_NAME | NVARCHAR(127) | Displays the association name. |
| ASSOCIATION_KIND | VARCHAR(32) | Displays the kind of association: FOR EIGN KEY EXPLICIT, FOREIGN KEY IM PLICIT, or UNMANAGED. |
| EXTENSION_PACKAGE_NAME | NVARCHAR(127) | Displays the extension package name. |
| TARGET_ARTIFACT_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the associated CDS artifact. |
| TARGET_ARTIFACT_NAME | NVARCHAR(127) | Displays the name of the associated CDS artifact. |
| TARGET_CARDINALITY_MIN | INTEGER | Displays the minimum cardinality of the association target. The default is 0. -1 represents unlimited. |
| TARGET_CARDINALITY_MAX | INTEGER | Displays the maximum cardinality of the association target. The default is 1. |
| JOIN_CONDITION | NCLOB | Displays the join condition for unmanaged associations (ASSOCIATION_KIND = UNMANAGED). |

## Additional Information

Association definitions are exposed as part of the CDS_ARTIFACT_DEFINITION result set, represented by the ARTIFACT_KIND association. Foreign key elements are also available from the ASSOCIATION_ELEMENT, which distinguishes them from regular elements.

## Related Information

CDS_ANNOTATION_ASSIGNMENTS System View [→](CDS_ANNOTATION_ASSIGNMENTS-System-View.md) CDS_ANNOTATION_VALUES System View [→](CDS_ANNOTATION_VALUES-System-View.md) CDS_ARTIFACT_NAMES System View [→](CDS_ARTIFACT_NAMES-System-View.md) CDS_ENTITIES System View [→](CDS_ENTITIES-System-View.md) CDS_VIEWS System View [→](CDS_VIEWS-System-View.md)
