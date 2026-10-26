# 6.2.209 M_PLE_SESSIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1935–1936

Lists all planning sessions on the system as well as their status and details.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| SESSION_NAME | NVARCHAR(256) | Displays the session name. |
| IS_VALID | VARCHAR(5) | Displays whether the session is valid: TRUE or FALSE. |
| SESSION_GROUP_NAME | NVARCHAR(256) | Displays the session group name. |
| LAST_ERROR | NVARCHAR(2000) | Displays the last error. |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SITE_ID | INTEGER | Displays the site ID of the secondary site. This value is -1 on a single instance. |

## Related Information

[M_PLE_RUNTIME_OBJECTS System View](M_PLE_RUNTIME_OBJECTS-System-View.md)
