# 6.2.329 M_TEMPORARY_VIEWS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 2106–2107

Displays temporary views.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| VIEW_NAME | NVARCHAR(256) | Displays the view name. |
| VIEW_OID | BIGINT | Displays the object ID of the view. |
| IS_UNICODE | VARCHAR(5) | Displays whether the query string contains Unicode: TRUE/FALSE. |
| IS_READ_ONLY | VARCHAR(5) | Displays whether this view is a read-only or an updatable view: TRUE/ FALSE. |
| HAS_CHECK_OPTION | VARCHAR(5) | Displays whether this view has an updatable view condition: TRUE/FALSE. |
| HAS_COLUMN_ALIASES | VARCHAR(5) | Displays whether the view has a columns alias: TRUE/FALSE. |
| DEFINITION | NCLOB | Displays the definition of the view. |
| COMMENTS | NVARCHAR(5000) | Displays the description on the view. |
| IS_COLUMN_VIEW | VARCHAR(5) | Displays whether or not this view is a column view: TRUE/FALSE |
| VIEW_TYPE | VARCHAR(16) | Displays the type of view: ROW, OLAP, JOIN, HIERARCHY, or CALC. |
| IS_TENANT_SHARED | VARCHAR(5) | Displays whether the view metadata can be shared across tenants: TRUE/ FALSE. |
| HAS_STRUCTURED_PRIVILEGE_CHECK | VARCHAR(5) | Displays whether the view is registered for a structured privilege check: TRUE/ FALSE. |

## Related Information

M_TEMPORARY_VIEW_COLUMNS System View [→](M_TEMPORARY_VIEW_COLUMNS-System-View.md) VIEWS System View [→](../6.01-System-Views/VIEWS-System-View.md)
