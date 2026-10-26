# 6.1.29 CDS_ANNOTATION_VALUES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1433–1434

Provides CDS annotation values.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| ARTIFACT_NAME | NVARCHAR(127) | Displays the artifact name. |
| ELEMENT_NAME | NVARCHAR(127) | Displays the element name. |
| ANNOTATION_SCHEMA_NAME | NVARCHAR(256) | Displays the annotation schema name. |
| ANNOTATION_NAME | NVARCHAR(127) | Displays the annotation name. |
| EXTENSION_PACKAGE_NAME | NVARCHAR(127) | Displays the extension package name. |
| VALUE | NCLOB | Displays the value of the annotation. |

## Related Information

CDS_ANNOTATION_ASSIGNMENTS System View [→](CDS_ANNOTATION_ASSIGNMENTS-System-View.md) ANNOTATIONS System View [→](ANNOTATIONS-System-View.md) ANNOTATE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ANNOTATE-Statement-Data-Definition.md) CDS_ARTIFACT_NAMES System View [→](CDS_ARTIFACT_NAMES-System-View.md) CDS_ASSOCIATIONS System View [→](CDS_ASSOCIATIONS-System-View.md) CDS_ENTITIES System View [→](CDS_ENTITIES-System-View.md) CDS_VIEWS System View [→](CDS_VIEWS-System-View.md)
