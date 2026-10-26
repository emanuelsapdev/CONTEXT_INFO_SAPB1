# 6.1.26 AUTHORIZATION_OBJECTS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1431–1432

Provides information regarding authorization objects.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| TYPE_ID | BIGINT | Displays the ID of the authorization object. |
| SUBTYPE_ID | INTEGER | Displays the ID of the authorization object subtype. |
| OBJECT_ID | BIGINT | Displays the ID of the object. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the name of the schema. |
| OBJECT_NAME | NVARCHAR(256) | Displays the name of the object. |
| OWNER_OID | BIGINT | Displays the owner of the object ID. |
| OWNER_NAME | NVARCHAR(256) | Displays the name of the object owner. |
| READONLY | INTEGER | Displays whether or not the object is read only. |

## Related Information

AUTHORIZATION_GRAPH System View [→](AUTHORIZATION_GRAPH-System-View.md) AUTHORIZATION_TYPES System View [→](AUTHORIZATION_TYPES-System-View.md)
