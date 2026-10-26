# 6.1.27 AUTHORIZATION_TYPES System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, página 1432

Provides information about object types and subtypes used by authorization object IDs.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| TYPE_ID | BIGINT | Displays the ID of the authorization object type. |
| TYPE_NAME | NVARCHAR(256) | Displays the name of the authorization object type. |
| SUBTYPE_ID | BIGINT | Displays the ID of the authorization object subtype. |
| SUBTYPE_NAME | NVARCHAR(256) | Displays the name of the authorization object subtype. |

## Related Information

AUTHORIZATION_GRAPH System View [→](AUTHORIZATION_GRAPH-System-View.md) AUTHORIZATION_OBJECTS System View [→](AUTHORIZATION_OBJECTS-System-View.md)
