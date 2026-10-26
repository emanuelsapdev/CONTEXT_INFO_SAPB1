# 6.1.21 ASSOCIATIONS System View

> [↑ 6.1 System Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1422–1423

Provides information about associations.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the association owner schema name. |
| OBJECT_NAME | NVARCHAR(256) | Displays the association owner table or view name. |
| OBJECT_TYPE | VARCHAR(32) | Displays the association owner object type. |
| ASSOCIATION_NAME | NVARCHAR(256) | Displays the association name. |
| TARGET_SCHEMA_NAME | NVARCHAR(256) | Displays the target schema name that the association is associated with. |
| TARGET_OBJECT_NAME | NVARCHAR(256) | Displays the target table/view name that the association is associated with. |
| TARGET_OBJECT_TYPE | VARCHAR(32) | Displays the target object type that the association is associated with. |
| JOIN_CONDITION | NVARCHAR(5000) | Displays the join condition. |
| JOIN_CARDINALITY | VARCHAR(12) | Displays the join cardinality type. |
| DEFAULT_FILTER | NVARCHAR(5000) | Displays the default predicate filter for columns. |

## Related Information

[CDS_ASSOCIATIONS System View](CDS_ASSOCIATIONS-System-View.md)
