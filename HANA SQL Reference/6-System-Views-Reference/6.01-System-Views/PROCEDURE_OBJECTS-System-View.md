# 6.1.113 PROCEDURE_OBJECTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1532–1533

Contains the results of the system procedure GET_PROCEDURE_OBJECTS.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(128) | Displays the schema name of the stored procedure. |
| PROCEDURE_NAME | NVARCHAR(128) | Displays the procedure name of the stored procedure. |
| OBJECT_SCHEMA | NVARCHAR(128) | Displays the schema name of the object in the stored procedure code. |
| OBJECT_NAME | NVARCHAR(128) | Displays the object name of the object in the stored procedure code. |
| OBJECT_TYPE_ID | INTEGER | Displays the type ID of the object in the stored procedure code. |
| OBJECT_TYPE | VARCHAR(32) | Displays the type of the object in the stored procedure code. |
| START_POSITION | INTEGER | Displays the start position of the object in the stored procedure code. |
| END_POSITION | INTEGER | Displays the end position of the object in the stored procedure code. |

## Related Information

PROCEDURES System View [→](PROCEDURES-System-View.md) PROCEDURE_PARAMETERS System View [→](PROCEDURE_PARAMETERS-System-View.md) PROCEDURE_PARAMETER_COLUMNS System View [→](PROCEDURE_PARAMETER_COLUMNS-System-View.md) PROCEDURE_ROUTES System View [→](PROCEDURE_ROUTES-System-View.md)
