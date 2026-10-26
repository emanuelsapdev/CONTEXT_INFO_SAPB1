# 6.1.116 PROCEDURE_ROUTES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1535–1536

Provides information about the procedure being routed. This view is for internal use only.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| PROCEDURE_SCHEMA | NVARCHAR(256) | Displays the schema name of the stored procedure. |
| PROCEDURE_NAME | NVARCHAR(256) | Displays the name of the stored procedure. |
| OBJECT_TYPE | VARCHAR(13) | Displays the object type: REMOTE_SOURCE, VOLUME, or TABLE. |
| OBJECT_SCHEMA | NVARCHAR(256) | Displays the schema of the object, if applicable. |
| OBJECT_NAME | NVARCHAR(256) | Displays the object name. |
| VOLUME_ID | INTEGER | Displays the volume ID. |

## Related Information

PROCEDURES System View [→](PROCEDURES-System-View.md) PROCEDURE_OBJECTS System View [→](PROCEDURE_OBJECTS-System-View.md) PROCEDURE_PARAMETERS System View [→](PROCEDURE_PARAMETERS-System-View.md) PROCEDURE_PARAMETER_COLUMNS System View [→](PROCEDURE_PARAMETER_COLUMNS-System-View.md)
