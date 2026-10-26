# 6.1.16 ANNOTATIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1417–1418

Provides information about annotations that have been added to SQL objects.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the object. |
| OBJECT_NAME | NVARCHAR(256) | Displays the name of the object. |
| OBJECT_TYPE | VARCHAR(32) | Displays the type of object, for example, a table. |
| SUBOBJECT_NAME | NVARCHAR(256) | Displays the name of the subobject, if applicable. |
| SUBOBJECT_TYPE | VARCHAR(9) | Displays the type of subobject, if applicable, for example, a table column. |
| KEY | NVARCHAR(256) | Displays the annotation key. |
| VALUE | NVARCHAR(256) | Displays the annotation key value. |

## Related Information

[ANNOTATE Statement (Data Definition)](../../4-SQL-Reference/4.10-SQL-Statements/4.10.01-Statements-A-Z/ANNOTATE-Statement-Data-Definition.md)
