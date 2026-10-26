# 6.1.86 HIERARCHY_OBJECTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1505–1506

Provides the list of objects that hierarchy navigation functions can be run on.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name for the hierarchy. |
| OBJECT_NAME | NVARCHAR(256) | Displays the name of the hierarchy. |
| OBJECT_TYPE | VARCHAR(32) | Displays the object type of the hierarchy: TABLE, VIEW, or FUNCTION. |
| OBJECT_OID | BIGINT | Dispalys the object ID of the hierarchy. |

## Related Information

[Hierarchy Functions](../../4-SQL-Reference/4.09-SQL-Functions/4.09.07-Hierarchy-Functions.md)
