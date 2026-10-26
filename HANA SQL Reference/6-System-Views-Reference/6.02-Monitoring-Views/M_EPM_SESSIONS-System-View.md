# 6.2.94 M_EPM_SESSIONS System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1770–1771

Provides all EPM sessions with detailed information.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| PORT | INTEGER | Displays the internal port. |
| SCHEMA_NAME | NVARCHAR(256) | Displays the schema name. |
| MODEL_NAME | NVARCHAR(256) | Displays the model name. |
| USER_NAME | NVARCHAR(256) | Displays the user name. |
| VERSION | INTEGER | Displays the version. |
| STATUS | VARCHAR(18) | Displays the status. |

## Related Information

EPM_QUERY_SOURCES System View [→](../6.01-System-Views/EPM_QUERY_SOURCES-System-View.md) EPM_MODELS System View [→](../6.01-System-Views/EPM_MODELS-System-View.md)
