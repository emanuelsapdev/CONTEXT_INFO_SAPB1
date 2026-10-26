# 6.1.107 OWNERSHIP System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1525

Provides owner information for the objects available to the user who is querying the view.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name of the object. |
| OWNER_NAME | NVARCHAR(256) | Displays the name of the object owner. |
| OBJECT_NAME | NVARCHAR(256) | Displays the object name. |
| OBJECT_TYPE | VARCHAR(32) | Displays the object type. |
| OBJECT_OID | BIGINT | Displays the object ID. |
| APPLICATION_NAME | NVARCHAR(256) | Displays the name of the application used for object creation. |

## Related Information

[OBJECTS System View](OBJECTS-System-View.md)
