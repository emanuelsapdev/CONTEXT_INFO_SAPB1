# 6.1.28 CDS_ANNOTATION_ASSIGNMENTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1432–1433

Provides CDS annotation assignments.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| ARTIFACT_NAME | NVARCHAR(127) | Displays the artifact name. |
| COMPONENT_NAME | NVARCHAR(127) | Displays the component name. |
| ANNOTATION_NAME | NVARCHAR(127) | Displays the annotation name. |
| EXTENSION_PACKAGE_NAME | NVARCHAR(127) | Displays the extension package name. |
| FORMAT | NVARCHAR(127) | Displays the format of the annotation value. |
| VALUE | NCLOB(2147483647) | Displays the value. |
| VALIDATION_RESULT | NVARCHAR(127) | Displays the validation result of the an notation value. |
| DEFINITION_SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the annotation definition. |
| DEFINITION_NAME | NVARCHAR(127) | Displays the name of the annotation definition. |

## Related Information

ANNOTATIONS System View [→](ANNOTATIONS-System-View.md) CDS_ANNOTATION_VALUES System View [→](CDS_ANNOTATION_VALUES-System-View.md) ANNOTATE Statement (Data Definition) [→](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ANNOTATE-Statement-Data-Definition.md) CDS_ARTIFACT_NAMES System View [→](CDS_ARTIFACT_NAMES-System-View.md) CDS_ASSOCIATIONS System View [→](CDS_ASSOCIATIONS-System-View.md) CDS_ENTITIES System View [→](CDS_ENTITIES-System-View.md) CDS_VIEWS System View [→](CDS_VIEWS-System-View.md)
