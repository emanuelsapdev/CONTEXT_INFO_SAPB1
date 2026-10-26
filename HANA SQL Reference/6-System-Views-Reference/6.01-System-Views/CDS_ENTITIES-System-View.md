# 6.1.32 CDS_ENTITIES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1436–1437

Provides information about CDS entities.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| ENTITY_NAME | NVARCHAR(127) | Displays the entity name. |
| EXTENSION_PACKAGE_NAME | NVARCHAR(127) | Displays the extension package name. |
| SERIES_KIND | VARCHAR(32) | Displays the kind of series: NO_SERIES, NOT_EQUIDISTANT, EQUIDISTANT, or EQUIDISTANT_PIECEWISE. |

## Related Information

CDS_ANNOTATION_ASSIGNMENTS System View [→](CDS_ANNOTATION_ASSIGNMENTS-System-View.md) CDS_ANNOTATION_VALUES System View [→](CDS_ANNOTATION_VALUES-System-View.md) CDS_ASSOCIATIONS System View [→](CDS_ASSOCIATIONS-System-View.md) CDS_ARTIFACT_NAMES System View [→](CDS_ARTIFACT_NAMES-System-View.md)

CDS_ENTITIES System View [→](CDS_ENTITIES-System-View.md) CDS_VIEWS System View [→](CDS_VIEWS-System-View.md)
