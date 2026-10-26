# 6.1.30 CDS_ARTIFACT_NAMES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1434–1435

Provides CDS artifact names.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| ARTIFACT_NAME | NVARCHAR(127) | Displays the artifact name. |
| ARTIFACT_KIND | VARCHAR(32) | Displays the kind of artifact: ANNOTA TION, ARRAY_TYPE, ASSOCIATION, CONTEXT, DERIVED_TYPE, ENTITY, ENUM, STRUCTURED_TYPE, or VIEW. |

## Related Information

CDS_ANNOTATION_ASSIGNMENTS System View [→](CDS_ANNOTATION_ASSIGNMENTS-System-View.md) CDS_ANNOTATION_VALUES System View [→](CDS_ANNOTATION_VALUES-System-View.md) CDS_ARTIFACT_NAMES System View [→](CDS_ARTIFACT_NAMES-System-View.md) CDS_ASSOCIATIONS System View [→](CDS_ASSOCIATIONS-System-View.md) CDS_ENTITIES System View [→](CDS_ENTITIES-System-View.md) CDS_VIEWS System View [→](CDS_VIEWS-System-View.md)
